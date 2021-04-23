---
description: Добавляет часть данных для конкретного приложения.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'Метод Иконтекстноде:: Аддпропертидата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed318520b8ac83acbc8ed615002fababe2a4b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145538"
---
# <a name="icontextnodeaddpropertydata-method"></a><span data-ttu-id="5babb-103">Метод Иконтекстноде:: Аддпропертидата</span><span class="sxs-lookup"><span data-stu-id="5babb-103">IContextNode::AddPropertyData method</span></span>

<span data-ttu-id="5babb-104">Добавляет часть данных для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="5babb-104">Adds a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5babb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5babb-105">Syntax</span></span>


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="5babb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5babb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5babb-107">*ппропертидатаид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5babb-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5babb-108">Глобальный уникальный идентификатор (GUID), используемый для идентификации типа данных.</span><span class="sxs-lookup"><span data-stu-id="5babb-108">A globally unique identifier (GUID) that is used to identify the type of data.</span></span>

</dd> <dt>

<span data-ttu-id="5babb-109">*улпропертидатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5babb-109">*ulPropertyDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5babb-110">Размер данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="5babb-110">The size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5babb-111">*пбпропертиесдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5babb-111">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5babb-112">\[в, Size \_ имеет размер (улпропертидатасизе)\]</span><span class="sxs-lookup"><span data-stu-id="5babb-112">\[in, size\_is(ulPropertyDataSize)\]</span></span>

<span data-ttu-id="5babb-113">Массив 8-битовых целых чисел без знака, содержащий добавляемые сведения о свойстве.</span><span class="sxs-lookup"><span data-stu-id="5babb-113">An 8-bit unsigned integer array containing the property information to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5babb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5babb-114">Return value</span></span>

<span data-ttu-id="5babb-115">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5babb-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5babb-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5babb-116">Remarks</span></span>

<span data-ttu-id="5babb-117">Используйте **иконтекстноде:: аддпропертидата** , чтобы связать данные с узлом контекста.</span><span class="sxs-lookup"><span data-stu-id="5babb-117">Use **IContextNode::AddPropertyData** to associate data with a context node.</span></span> <span data-ttu-id="5babb-118">Чтобы получить данные позже, используйте [**иконтекстноде:: жетпропертидата**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="5babb-118">To retrieve the data later, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

<span data-ttu-id="5babb-119">Анализатор рукописного ввода может удалить узел как часть анализа рукописного ввода, если только узел контекста не будет подтвержден (см. раздел [**иконтекстноде:: Confirm**](icontextnode-confirm.md)).</span><span class="sxs-lookup"><span data-stu-id="5babb-119">The ink analyzer may delete the node as part of ink analysis, unless the context node is confirmed (see [**IContextNode::Confirm**](icontextnode-confirm.md)).</span></span> <span data-ttu-id="5babb-120">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5babb-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5babb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5babb-121">Requirements</span></span>



| <span data-ttu-id="5babb-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5babb-122">Requirement</span></span> | <span data-ttu-id="5babb-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5babb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5babb-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5babb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5babb-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5babb-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5babb-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5babb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5babb-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5babb-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5babb-128">Header</span><span class="sxs-lookup"><span data-stu-id="5babb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5babb-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5babb-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5babb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5babb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5babb-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5babb-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5babb-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5babb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5babb-133">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="5babb-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="5babb-134">**Иконтекстноде:: Жетпропертидата**</span><span class="sxs-lookup"><span data-stu-id="5babb-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="5babb-135">**Иконтекстноде:: Жетпропертидатаидс**</span><span class="sxs-lookup"><span data-stu-id="5babb-135">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="5babb-136">**Иконтекстноде:: Контаинспропертидата**</span><span class="sxs-lookup"><span data-stu-id="5babb-136">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="5babb-137">**Иконтекстноде:: Лоадпропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="5babb-137">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="5babb-138">**Иконтекстноде:: Ремовепропертидата**</span><span class="sxs-lookup"><span data-stu-id="5babb-138">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="5babb-139">**Иконтекстноде:: Савепропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="5babb-139">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




