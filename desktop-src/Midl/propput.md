---
title: propput - атрибут
description: Атрибут \ propput \ задает функцию настройки свойства. Свойство должно иметь то же имя, что и функция.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- атрибут propput MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133735"
---
# <a name="propput-attribute"></a><span data-ttu-id="dc4fe-105">propput - атрибут</span><span class="sxs-lookup"><span data-stu-id="dc4fe-105">propput attribute</span></span>

<span data-ttu-id="dc4fe-106">Атрибут **\[ propput \]** указывает функцию настройки свойства.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-106">The **\[propput\]** attribute specifies a property-setting function.</span></span> <span data-ttu-id="dc4fe-107">Свойство должно иметь то же имя, что и функция *.*</span><span class="sxs-lookup"><span data-stu-id="dc4fe-107">The property must have the same name as the function *.*</span></span>

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="dc4fe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc4fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc4fe-109">*атрибуты необязательного свойства*</span><span class="sxs-lookup"><span data-stu-id="dc4fe-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="dc4fe-110">Ноль или более атрибутов свойств.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="dc4fe-111">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="dc4fe-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="dc4fe-112">Тип данных, возвращаемых удаленной процедурой.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="dc4fe-113">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="dc4fe-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dc4fe-114">Имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="dc4fe-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="dc4fe-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="dc4fe-116">Ноль или более параметров для удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc4fe-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc4fe-117">Remarks</span></span>

<span data-ttu-id="dc4fe-118">Функция, имеющая атрибут **\[ propput \]** , должна также иметь в качестве последнего параметра параметр с **\[** [](in.md) **\]** атрибутом in.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-118">A function that has the **\[propput\]** attribute must also have, as its last parameter, a parameter that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="dc4fe-119">**\[** [](propget.md) **\]** Для функции можно указать не более одного параметра propget, **\[ propput \]** и **\[** [**propputref**](propputref.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="dc4fe-119">At most, one of **\[**[**propget**](propget.md)**\]**, **\[propput\]** and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="dc4fe-120">Если атрибут **\[** [**LCID**](lcid.md) **\]** используется в списке параметров функции, содержащей параметр с атрибутом **\[ propput \]** , то параметр **\[ LCID \]** должен находиться в секундах до последней.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-120">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[propput\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="dc4fe-121">Флаги</span><span class="sxs-lookup"><span data-stu-id="dc4fe-121">Flags</span></span>

<span data-ttu-id="dc4fe-122">ВЫЗВАТЬ \_ пропертипут</span><span class="sxs-lookup"><span data-stu-id="dc4fe-122">INVOKE\_PROPERTYPUT</span></span>

## <a name="examples"></a><span data-ttu-id="dc4fe-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="dc4fe-123">Examples</span></span>

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a><span data-ttu-id="dc4fe-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc4fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4fe-125">Различия между MIDL и MKTYPLIB</span><span class="sxs-lookup"><span data-stu-id="dc4fe-125">Differences Between MIDL and MKTYPLIB</span></span>](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[<span data-ttu-id="dc4fe-126">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="dc4fe-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="dc4fe-127">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="dc4fe-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="dc4fe-128">**propget**</span><span class="sxs-lookup"><span data-stu-id="dc4fe-128">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="dc4fe-129">**propputref**</span><span class="sxs-lookup"><span data-stu-id="dc4fe-129">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="dc4fe-130">**типефлагс**</span><span class="sxs-lookup"><span data-stu-id="dc4fe-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 