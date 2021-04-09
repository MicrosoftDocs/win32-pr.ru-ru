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
# <a name="default-pointer-types"></a>Типы указателей по умолчанию

Указатели не обязательно должны иметь явное описание атрибута. Если явный атрибут не указан, компилятор MIDL использует атрибут указателя по умолчанию.

По умолчанию для указателей без атрибутов используются следующие варианты:

-   Указатели верхнего уровня, которые отображаются в списке параметров, по умолчанию имеют \[ [**Ссылочные**](/windows/desktop/Midl/ref) \] указатели.
-   Все остальные указатели по умолчанию имеют тип, заданный \[ атрибутом [**указателя \_ по умолчанию**](/windows/desktop/Midl/pointer-default) \] . Если не \[ указан атрибут **указателя \_ по умолчанию** \] , эти указатели по умолчанию \[ имеют [**уникальный**](/windows/desktop/Midl/unique) \] атрибут, если компилятор MIDL находится в режиме [расширений Майкрософт](microsoft-rpc-binding-handle-extensions.md) , или \[ атрибут [**ptr**](/windows/desktop/Midl/ptr) , \] Если компилятор MIDL находится в режиме совместимости с DCE.

Если удаленная процедура возвращает указатель, возвращаемое значение должно быть \[ [**уникальным**](/windows/desktop/Midl/unique) \] или полным указателем ( \[ [**ptr**](/windows/desktop/Midl/ptr) \] ).

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

### <a name="remarks"></a>Комментарии

Чтобы обеспечить однозначное поведение указателя-атрибута, при определении указателя всегда используйте явные атрибуты указателя.

Рекомендуется **\[** использовать PTR только в **\]** том случае, если требуется псевдоним указателя.

 

 