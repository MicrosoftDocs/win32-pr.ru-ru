---
title: noncreatable - атрибут
description: Атрибут \ "\ несоздаваемый \" определяет объект, который не может быть создан самим по себе.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- несоздаваемый атрибут MIDL
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337041"
---
# <a name="noncreatable-attribute"></a><span data-ttu-id="02527-104">noncreatable - атрибут</span><span class="sxs-lookup"><span data-stu-id="02527-104">noncreatable attribute</span></span>

<span data-ttu-id="02527-105">**\[ Несоздаваемый \]** атрибут определяет объект, который не может быть создан самим по себе.</span><span class="sxs-lookup"><span data-stu-id="02527-105">The **\[noncreatable\]** attribute defines an object that cannot be instantiated by itself.</span></span>

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="02527-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="02527-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02527-107">*Список атрибутов coclass*</span><span class="sxs-lookup"><span data-stu-id="02527-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02527-108">Другие атрибуты, которые применяются к классу.</span><span class="sxs-lookup"><span data-stu-id="02527-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="02527-109">*имя класса*</span><span class="sxs-lookup"><span data-stu-id="02527-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="02527-110">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="02527-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="02527-111">*coclass-интерфейс-список*</span><span class="sxs-lookup"><span data-stu-id="02527-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02527-112">Список интерфейсов для класса.</span><span class="sxs-lookup"><span data-stu-id="02527-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02527-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02527-113">Remarks</span></span>

<span data-ttu-id="02527-114">Используйте **\[ несоздаваемый \]** атрибут в операторе [**coclass**](coclass.md) , чтобы указать пользователям, что они не могут создать новый объект этого класса на верхнем уровне, то есть путем вызова **CreateInstance** **или CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="02527-114">Use the **\[noncreatable\]** attribute on a [**coclass**](coclass.md) statement to indicate to users that they cannot create a new object of this class at the top level—that is, by calling **CreateInstance** or **CoCreateInstance**.</span></span> <span data-ttu-id="02527-115">Для создания экземпляра объекта этого класса требуется вызов метода другого объекта.</span><span class="sxs-lookup"><span data-stu-id="02527-115">Instantiation of an object of this class requires a method call to another object.</span></span> <span data-ttu-id="02527-116">Например, в Microsoft Excel объект Cell является несоздаваемым и должен быть получен из объекта листа Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="02527-116">For example, in Microsoft Excel, the "Cell" object is noncreatable and must be obtained from a Microsoft Excel Worksheet object.</span></span>

<span data-ttu-id="02527-117">Методы, возвращающие экземпляры несоздаваемых классов, должны возвращать точный тип объекта, а не типы **Variant** или **IDispatch** \* .</span><span class="sxs-lookup"><span data-stu-id="02527-117">Methods that return instances of noncreatable classes should return the exact type of the object, rather than **VARIANT** or **IDispatch**\* types.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="02527-118">Типефлаг:</span><span class="sxs-lookup"><span data-stu-id="02527-118">Typeflag Representation:</span></span>

<span data-ttu-id="02527-119">Отсутствие ТИПЕФЛАГ \_ фканкреате.</span><span class="sxs-lookup"><span data-stu-id="02527-119">The absence of TYPEFLAG\_FCANCREATE.</span></span>

## <a name="examples"></a><span data-ttu-id="02527-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="02527-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="02527-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02527-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02527-122">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="02527-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="02527-123">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="02527-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="02527-124">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="02527-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="02527-125">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="02527-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 