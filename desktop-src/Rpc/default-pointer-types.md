---
title: Типы указателей по умолчанию
description: Указатели не обязательно должны иметь явное описание атрибута. Если явный атрибут не указан, компилятор MIDL использует атрибут указателя по умолчанию.
ms.assetid: b90619c3-70b4-44f0-ba37-293595281031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c565fe8019567fd1fe319d7b34287d9729bbe1d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070319"
---
# <a name="default-pointer-types"></a><span data-ttu-id="cd71b-104">Типы указателей по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cd71b-104">Default Pointer Types</span></span>

<span data-ttu-id="cd71b-105">Указатели не обязательно должны иметь явное описание атрибута.</span><span class="sxs-lookup"><span data-stu-id="cd71b-105">Pointers are not required to have an explicit attribute description.</span></span> <span data-ttu-id="cd71b-106">Если явный атрибут не указан, компилятор MIDL использует атрибут указателя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cd71b-106">When an explicit attribute is not provided, the MIDL Compiler uses a default pointer attribute.</span></span>

<span data-ttu-id="cd71b-107">По умолчанию для указателей без атрибутов используются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="cd71b-107">The default cases for unattributed pointers are the following:</span></span>

-   <span data-ttu-id="cd71b-108">Указатели верхнего уровня, которые отображаются в списке параметров, по умолчанию имеют \[ [**Ссылочные**](/windows/desktop/Midl/ref) \] указатели.</span><span class="sxs-lookup"><span data-stu-id="cd71b-108">Top-level pointers that appear in parameter lists default to \[[**ref**](/windows/desktop/Midl/ref)\] pointers.</span></span>
-   <span data-ttu-id="cd71b-109">Все остальные указатели по умолчанию имеют тип, заданный \[ атрибутом [**указателя \_ по умолчанию**](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="cd71b-109">All other pointers default to the type specified by the \[[**pointer\_default**](/windows/desktop/Midl/pointer-default)\] attribute.</span></span> <span data-ttu-id="cd71b-110">Если не \[ указан атрибут **указателя \_ по умолчанию** \] , эти указатели по умолчанию \[ имеют [**уникальный**](/windows/desktop/Midl/unique) \] атрибут, если компилятор MIDL находится в режиме [расширений Майкрософт](microsoft-rpc-binding-handle-extensions.md) , или \[ атрибут [**ptr**](/windows/desktop/Midl/ptr) , \] Если компилятор MIDL находится в режиме совместимости с DCE.</span><span class="sxs-lookup"><span data-stu-id="cd71b-110">When no \[**pointer\_default**\] attribute is supplied, these pointers default to the \[ [**unique**](/windows/desktop/Midl/unique) \] attribute when the MIDL compiler is in [Microsoft Extensions](microsoft-rpc-binding-handle-extensions.md) mode or the \[[**ptr**](/windows/desktop/Midl/ptr)\] attribute when the MIDL compiler is in DCE-compatible mode.</span></span>

<span data-ttu-id="cd71b-111">Если удаленная процедура возвращает указатель, возвращаемое значение должно быть \[ [**уникальным**](/windows/desktop/Midl/unique) \] или полным указателем ( \[ [**ptr**](/windows/desktop/Midl/ptr) \] ).</span><span class="sxs-lookup"><span data-stu-id="cd71b-111">When a remote procedure returns a pointer, the return value must be a \[ [**unique**](/windows/desktop/Midl/unique) \] or full (\[ [**ptr**](/windows/desktop/Midl/ptr) \]) pointer.</span></span>

``` syntax
/* IDL file compiled without /osf */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0),
  pointer_default(ptr)
]
interface MyInterface
{
    typedef long *PLONG;
  
    struct MyCircularList {
        struct MyCircularList *pRight;
        struct MyCircularList *pLeft;
        long Data;
    };

    void Foo1( [in] PLONG p );                   // p is ref
 
    void Foo2( [in] struct MyCircularList *p );  // p is ref, p->pRight and p->pLeft is ptr

    struct MyCircularList *Foo3( void );         // returned pointer is ptr.    
}

[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea46),
  version(1.0)
]
interface MyInterface2
{
    struct MySingleList
       {
       struct MySingleList *pNext;
       long Data;
       };
    void Foo4( [in] struct MySingleList *p );  // p is ref, p->pNext is unique

    struct MySingleList *Foo5( void );         // returned pointer is unique.    
}
```

### <a name="remarks"></a><span data-ttu-id="cd71b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd71b-112">Remarks</span></span>

<span data-ttu-id="cd71b-113">Чтобы обеспечить однозначное поведение указателя-атрибута, при определении указателя всегда используйте явные атрибуты указателя.</span><span class="sxs-lookup"><span data-stu-id="cd71b-113">To ensure unambiguous pointer-attribute behavior, always use explicit pointer attributes when defining a pointer.</span></span>

<span data-ttu-id="cd71b-114">Рекомендуется **\[** использовать PTR только в **\]** том случае, если требуется псевдоним указателя.</span><span class="sxs-lookup"><span data-stu-id="cd71b-114">It is recommended that **\[** ptr **\]** is used only when pointer aliasing is required.</span></span>

 

 