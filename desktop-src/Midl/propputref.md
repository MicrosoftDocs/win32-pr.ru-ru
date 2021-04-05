---
title: propputref - атрибут
description: Атрибут \ propputref \ указывает функцию настройки свойства, которая использует ссылку вместо значения.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- атрибут propputref MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987386"
---
# <a name="propputref-attribute"></a><span data-ttu-id="e4d06-104">propputref - атрибут</span><span class="sxs-lookup"><span data-stu-id="e4d06-104">propputref attribute</span></span>

<span data-ttu-id="e4d06-105">Атрибут **\[ propputref \]** указывает функцию настройки свойства, которая использует ссылку вместо значения.</span><span class="sxs-lookup"><span data-stu-id="e4d06-105">The **\[propputref\]** attribute specifies a property-setting function that uses a reference instead of a value.</span></span>

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="e4d06-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4d06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4d06-107">*атрибуты необязательного свойства*</span><span class="sxs-lookup"><span data-stu-id="e4d06-107">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d06-108">Ноль или более атрибутов свойств.</span><span class="sxs-lookup"><span data-stu-id="e4d06-108">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="e4d06-109">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="e4d06-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d06-110">Тип данных, возвращаемых удаленной процедурой.</span><span class="sxs-lookup"><span data-stu-id="e4d06-110">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e4d06-111">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="e4d06-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d06-112">Имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="e4d06-112">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e4d06-113">*parameters*</span><span class="sxs-lookup"><span data-stu-id="e4d06-113">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d06-114">Ноль или более параметров для удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="e4d06-114">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4d06-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4d06-115">Remarks</span></span>

<span data-ttu-id="e4d06-116">Функция с атрибутом **\[ propputref \]** также должна иметь в качестве последнего параметра указатель, имеющий **\[** атрибут [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e4d06-116">A function that has the **\[propputref\]** attribute must also have, as its last parameter, a pointer that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="e4d06-117">Свойство должно иметь то же имя, что и функция.</span><span class="sxs-lookup"><span data-stu-id="e4d06-117">The property must have the same name as the function.</span></span> <span data-ttu-id="e4d06-118">**\[** [](propget.md) **\]** Для функции можно указать только один из атрибутов propget, **\[** [**propput**](propput.md) **\]** и **\[ \] propputref** .</span><span class="sxs-lookup"><span data-stu-id="e4d06-118">At most, one of **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]** and **\[propputref\]** attributes can be specified for a function.</span></span>

### <a name="flags"></a><span data-ttu-id="e4d06-119">Флаги</span><span class="sxs-lookup"><span data-stu-id="e4d06-119">Flags</span></span>

<span data-ttu-id="e4d06-120">ВЫЗВАТЬ \_ пропертипутреф</span><span class="sxs-lookup"><span data-stu-id="e4d06-120">INVOKE\_PROPERTYPUTREF</span></span>

## <a name="examples"></a><span data-ttu-id="e4d06-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="e4d06-121">Examples</span></span>

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a><span data-ttu-id="e4d06-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4d06-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d06-123">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="e4d06-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="e4d06-124">**окне**</span><span class="sxs-lookup"><span data-stu-id="e4d06-124">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="e4d06-125">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="e4d06-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="e4d06-126">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="e4d06-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e4d06-127">**propget**</span><span class="sxs-lookup"><span data-stu-id="e4d06-127">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="e4d06-128">**propput**</span><span class="sxs-lookup"><span data-stu-id="e4d06-128">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="e4d06-129">**типефлагс**</span><span class="sxs-lookup"><span data-stu-id="e4d06-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 