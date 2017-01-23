```

void preOrder2(BinTree *root)     //非递归前序遍历 
{
    stack<BinTree*> s;
    BinTree *p=root;
    while(p!=NULL||!s.empty())
    {
        while(p!=NULL)
        {
            cout<<p->data<<" ";
            s.push(p);
            p=p->lchild;
        }
        if(!s.empty())
        {
            p=s.top();
            s.pop();
            p=p->rchild;
        }
    }
}



void inOrder2(BinTree *root)      //非递归中序遍历
{
    stack<BinTree*> s;
    BinTree *p=root;
    while(p!=NULL||!s.empty())
    {
        while(p!=NULL)
        {
            s.push(p);
            p=p->lchild;
        }
        if(!s.empty())
        {
            p=s.top();
            cout<<p->data<<" ";
            s.pop();
            p=p->rchild;
        }
    }    
} 




void postOrder2(BinTree *root)    //非递归后序遍历
{
    stack<BTNode*> s;
    BinTree *p=root;
    BTNode *temp;
    while(p!=NULL||!s.empty())
    {
        while(p!=NULL)              //沿左子树一直往下搜索，直至出现没有左子树的结点 
        {
            BTNode *btn=(BTNode *)malloc(sizeof(BTNode));
            btn->btnode=p;
            btn->isFirst=true;
            s.push(btn);
            p=p->lchild;
        }
        if(!s.empty())
        {
            temp=s.top();
            s.pop();
            if(temp->isFirst==true)     //表示是第一次出现在栈顶 
             {
                temp->isFirst=false;
                s.push(temp);
                p=temp->btnode->rchild;    
            }
            else                        //第二次出现在栈顶 
             {
                cout<<temp->btnode->data<<" ";
                p=NULL;
            }
        }
    }    
} 

```



```javascript
//
//  CTree.cpp
//  Lesson3
//
//  Created by ShenJun on 2017/1/19.
//  Copyright © 2017年 ShenJun. All rights reserved.
//


    typedef struct TreeNode
    {
        TreeNode() : lch(0), rch(0), data('\0'){}
        TreeNode* lch;
        TreeNode* rch;
        char data;
    } *Node;



#include "CTree.hpp"


void CreatTree(Node& T)  // 从根节点开始实现
{
    T = new TreeNode();
    
    std::cout << "Enter the Number :" ;
    std::cin >> T->data;
    
    if(T->data == '#')
    {
        delete T;
        T = 0;
    }
    else
    {
        CreatTree(T->lch);
        CreatTree(T->rch);
    }
}

// 递归前序遍历
void preOrder(Node& T)
{
    if(T != NULL)
    {
        printf("%c", T->data);
        preOrder(T->lch);
        preOrder(T->rch);
    }
}

void inOrder(Node& T)
{
    if(T != NULL)
    {
        inOrder(T->lch);
        printf("%c", T->data);
        inOrder(T->rch);
    }
}

void postOrder(Node& T)
{
    if(T != NULL)
    {
        postOrder(T->lch);
        postOrder(T->rch);
        printf("%c", T->data);
    }
}



void pre_order(Node& T)
{
    std::stack<Node>* m_pStack = new std::stack<Node>();
    while (T != NULL || !m_pStack->empty()) {
        if(T != NULL)
        {
            printf("%c", T->data);
            m_pStack->push(T->rch);
            T = T->lch;
        }
        else
        {
            T = m_pStack->top();
            m_pStack->pop();
        }
    }
    delete m_pStack;
    m_pStack = NULL;
}

// 非递归中序遍历
void in_order(Node& T)
{
    std::stack<Node>* m_pStack = new std::stack<Node>();
    while (T != NULL || !m_pStack->empty()) {
        if(T != NULL)
        {
            m_pStack->push(T);
            T = T->lch;
        }
        else
        {
            T = m_pStack->top();
            printf("%c", T->data);
            m_pStack->pop();
            T = T->rch;
        }
    }
    delete m_pStack;
    m_pStack = NULL;
}

// 删除
void ClearTree(Node& T)
{
    ClearTree(T->lch);
    ClearTree(T->rch);
    delete T;
}

void TreeMain()
{
    
    TreeNode *pRoot = new TreeNode();
    CreatTree(pRoot);
//  preOrder(pRoot);
//  pre_order(pRoot);
    in_order(pRoot);
}
```


