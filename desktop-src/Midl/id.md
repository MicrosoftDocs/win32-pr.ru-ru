---
title: Атрибут идентификатора
description: Атрибут \ ID \ указывает идентификатор DISPID для функции-члена (свойства или метода в интерфейсе или DISP).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- атрибут ID MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412820"
---
# <a name="id-attribute"></a><span data-ttu-id="4f45a-104">Атрибут идентификатора</span><span class="sxs-lookup"><span data-stu-id="4f45a-104">id attribute</span></span>

<span data-ttu-id="4f45a-105">Атрибут **\[ ID \]** задает DISPID для функции-члена (свойства или метода в интерфейсе или DISP).</span><span class="sxs-lookup"><span data-stu-id="4f45a-105">The **\[id\]** attribute specifies a DISPID for a member function (either a property or a method, in an interface or dispinterface).</span></span>

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="4f45a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f45a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f45a-107">*ID-num*</span><span class="sxs-lookup"><span data-stu-id="4f45a-107">*id-num*</span></span> 
</dt> <dd>

<span data-ttu-id="4f45a-108">DISPID для функции.</span><span class="sxs-lookup"><span data-stu-id="4f45a-108">DISPID for the function.</span></span>

</dd> <dt>

<span data-ttu-id="4f45a-109">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="4f45a-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4f45a-110">Указывает список атрибутов интерфейса MIDL, отданных от нуля или более.</span><span class="sxs-lookup"><span data-stu-id="4f45a-110">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="4f45a-111">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="4f45a-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4f45a-112">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="4f45a-112">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="4f45a-113">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="4f45a-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4f45a-114">Указывает имя функции в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="4f45a-114">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="4f45a-115">*список необязательных параметров*</span><span class="sxs-lookup"><span data-stu-id="4f45a-115">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4f45a-116">Ноль или более параметров функции.</span><span class="sxs-lookup"><span data-stu-id="4f45a-116">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f45a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f45a-117">Remarks</span></span>

<span data-ttu-id="4f45a-118">Используйте атрибут **\[ ID \]** , если необходимо назначить стандартный идентификатор DISPID (например \_ , значение DISPID, DISPID \_ NEWENUM и т. д.) в метод или свойство или при реализации собственного **интерфейса IDispatch:: Invoke** вместо делегирования в **диспинвоке** / **ITypeInfo:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="4f45a-118">Use the **\[id\]** attribute when you want to assign a standard DISPID (like DISPID\_VALUE, DISPID\_NEWENUM etc.) to a method or property, or when you implement your own **IDispatch::Invoke** instead of delegating to **DispInvoke**/**ITypeInfo::Invoke**.</span></span>

<span data-ttu-id="4f45a-119">Если атрибут **\[ ID \]** не используется в интерфейсе, компилятор MIDL присвоит вам идентификатор DISPID.</span><span class="sxs-lookup"><span data-stu-id="4f45a-119">If you do not use the **\[id\]** attribute on an interface, the MIDL compiler will assign a DISPID for you.</span></span> <span data-ttu-id="4f45a-120">Однако при указании disp-интерфейса с помощью свойств и методов необходимо указать DISPID для каждого свойства и метода.</span><span class="sxs-lookup"><span data-stu-id="4f45a-120">However, when you specify a dispinterface by using properties and methods, you must specify a DISPID for every property and method.</span></span>

<span data-ttu-id="4f45a-121">*ID-num* — это 32-разрядное положительное целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="4f45a-121">The *id-num* is a 32-bit positive integral value.</span></span> <span data-ttu-id="4f45a-122">Отрицательные идентификаторы зарезервированы для использования службой автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4f45a-122">Negative IDs are reserved for use by Automation.</span></span>

## <a name="examples"></a><span data-ttu-id="4f45a-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="4f45a-123">Examples</span></span>

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a><span data-ttu-id="4f45a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f45a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f45a-125">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="4f45a-125">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="4f45a-126">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="4f45a-126">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="4f45a-127">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="4f45a-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4f45a-128">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="4f45a-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4f45a-129">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="4f45a-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 