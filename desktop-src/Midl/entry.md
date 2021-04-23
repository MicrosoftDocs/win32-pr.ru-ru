---
title: entry - атрибут
description: Атрибут \ Entry \ указывает экспортированную функцию или константу в модуле, определяя точку входа в библиотеке DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- элемент атрибута MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336953"
---
# <a name="entry-attribute"></a><span data-ttu-id="dc002-104">entry - атрибут</span><span class="sxs-lookup"><span data-stu-id="dc002-104">entry attribute</span></span>

<span data-ttu-id="dc002-105">Атрибут **\[ entry \]** указывает экспортированную функцию или константу в модуле, определяя точку входа в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="dc002-105">The **\[entry\]** attribute specifies an exported function or constant in a module by identifying the entry point in the DLL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="dc002-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc002-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc002-107">*UUID — номер*</span><span class="sxs-lookup"><span data-stu-id="dc002-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="dc002-108">Задает универсальный уникальный идентификационный номер для [**модуля**](module.md).</span><span class="sxs-lookup"><span data-stu-id="dc002-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc002-109">*Идентификатор записи*</span><span class="sxs-lookup"><span data-stu-id="dc002-109">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="dc002-110">Указывает имя функции точки входа модуля или целочисленный идентификационный номер.</span><span class="sxs-lookup"><span data-stu-id="dc002-110">Specifies the module entry point function name or integer identification number.</span></span>

</dd> <dt>

<span data-ttu-id="dc002-111">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="dc002-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dc002-112">Указывает ноль или более атрибутов для применения компилятора MIDL к [**модулю**](module.md).</span><span class="sxs-lookup"><span data-stu-id="dc002-112">Specifies zero or more attributes for the MIDL compiler to apply to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc002-113">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="dc002-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="dc002-114">Указывает имя, используемое другими компонентами программного обеспечения для обозначения [**модуля**](module.md).</span><span class="sxs-lookup"><span data-stu-id="dc002-114">Specifies the name other software components use to denote the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc002-115">*елементлист*</span><span class="sxs-lookup"><span data-stu-id="dc002-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="dc002-116">Указывает одну или несколько инструкций определения элемента модуля.</span><span class="sxs-lookup"><span data-stu-id="dc002-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc002-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc002-117">Remarks</span></span>

<span data-ttu-id="dc002-118">Если переменная *EntryID* атрибута **\[ entry \]** является строкой, это именованная точка входа.</span><span class="sxs-lookup"><span data-stu-id="dc002-118">If the *entryid* variable of the **\[entry\]** attribute is a string, this is a named entry point.</span></span> <span data-ttu-id="dc002-119">Если идентификатор *EntryID* является числом, точка входа определяется порядковым номером.</span><span class="sxs-lookup"><span data-stu-id="dc002-119">If *entryid* is a number, the entry point is defined by an ordinal.</span></span> <span data-ttu-id="dc002-120">Этот атрибут предоставляет способ получения адреса функции в модуле.</span><span class="sxs-lookup"><span data-stu-id="dc002-120">This attribute provides a way to obtain the address of a function in a module.</span></span>

## <a name="examples"></a><span data-ttu-id="dc002-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="dc002-121">Examples</span></span>

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a><span data-ttu-id="dc002-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc002-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc002-123">**dllname**</span><span class="sxs-lookup"><span data-stu-id="dc002-123">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="dc002-124">**модуль**</span><span class="sxs-lookup"><span data-stu-id="dc002-124">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="dc002-125">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="dc002-125">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="dc002-126">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="dc002-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="dc002-127">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="dc002-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 