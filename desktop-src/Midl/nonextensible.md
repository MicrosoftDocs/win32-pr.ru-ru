---
title: Атрибут nonextensible
description: Атрибут \ "\ нерасширяемый \" указывает, что реализация IDispatch включает только свойства и методы, перечисленные в описании интерфейса, и не может быть расширена с помощью дополнительных элементов во время выполнения.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- нерасширяемый атрибут MIDL
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650330"
---
# <a name="nonextensible-attribute"></a><span data-ttu-id="18c82-104">Атрибут nonextensible</span><span class="sxs-lookup"><span data-stu-id="18c82-104">nonextensible attribute</span></span>

<span data-ttu-id="18c82-105">**\[ Нерасширяемый \]** атрибут указывает, что реализация [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) включает только свойства и методы, перечисленные в описании интерфейса, и не может быть расширена с помощью дополнительных элементов во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="18c82-105">The **\[nonextensible\]** attribute specifies that the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) implementation includes only the properties and methods listed in the interface description and cannot be extended with additional members at run time.</span></span> <span data-ttu-id="18c82-106">(По умолчанию Автоматизация предполагает, что интерфейсы могут добавлять членов во время выполнения, то есть предполагается, что они являются расширяемыми.)</span><span class="sxs-lookup"><span data-stu-id="18c82-106">(By default, Automation assumes that interfaces may add members at run time; that is, it assumes they are extensible.)</span></span>

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="18c82-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="18c82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18c82-108">*UUID — номер*</span><span class="sxs-lookup"><span data-stu-id="18c82-108">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="18c82-109">Задает универсальный уникальный идентификационный номер для [**интерфейса**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="18c82-109">Specifies a universally unique identification number for the [**interface**](interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c82-110">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="18c82-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="18c82-111">Указывает список атрибутов интерфейса MIDL, отданных от нуля или более.</span><span class="sxs-lookup"><span data-stu-id="18c82-111">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="18c82-112">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="18c82-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="18c82-113">Указывает имя [**интерфейса**](interface.md) или [**DISP**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="18c82-113">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c82-114">*определение интерфейса*</span><span class="sxs-lookup"><span data-stu-id="18c82-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="18c82-115">Задает инструкции IDL, которые формируют определение интерфейса или [**DISP**](dispinterface.md)- [**интерфейсов**](interface.md) .</span><span class="sxs-lookup"><span data-stu-id="18c82-115">Specifies IDL statements that form the definition of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18c82-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18c82-116">Remarks</span></span>

<span data-ttu-id="18c82-117">**\[ Нерасширяемый \]** атрибут можно применить как к интерфейсу, так и к диспетчеру интерфейса.</span><span class="sxs-lookup"><span data-stu-id="18c82-117">You can apply the **\[nonextensible\]** attribute to either an interface or a dispinterface.</span></span> <span data-ttu-id="18c82-118">Однако интерфейс также должен иметь **\[** [**сдвоенные**](dual.md) **\]** и **\[** [**oleautomation**](oleautomation.md) **\]** атрибуты.</span><span class="sxs-lookup"><span data-stu-id="18c82-118">However, an interface must also have the **\[**[**dual**](dual.md)**\]** and **\[**[**oleautomation**](oleautomation.md)**\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="18c82-119">Флаги</span><span class="sxs-lookup"><span data-stu-id="18c82-119">Flags</span></span>

<span data-ttu-id="18c82-120">ТИПЕФЛАГ \_ фнонекстенсибле</span><span class="sxs-lookup"><span data-stu-id="18c82-120">TYPEFLAG\_FNONEXTENSIBLE</span></span>

## <a name="examples"></a><span data-ttu-id="18c82-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="18c82-121">Examples</span></span>

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a><span data-ttu-id="18c82-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18c82-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c82-123">Содержимое библиотеки типов</span><span class="sxs-lookup"><span data-stu-id="18c82-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="18c82-124">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="18c82-124">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="18c82-125">**двойной**</span><span class="sxs-lookup"><span data-stu-id="18c82-125">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="18c82-126">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="18c82-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="18c82-127">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="18c82-127">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="18c82-128">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="18c82-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="18c82-129">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="18c82-129">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="18c82-130">**типефлагс**</span><span class="sxs-lookup"><span data-stu-id="18c82-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 