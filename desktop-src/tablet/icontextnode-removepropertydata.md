---
description: Удаляет часть данных, зависящих от приложения.
ms.assetid: 41077c2f-39e3-4069-ac05-97f1785e37b7
title: 'Метод Иконтекстноде:: Ремовепропертидата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.RemovePropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4c2fd5924b206ee296c066a908d2a59b02019f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542047"
---
# <a name="icontextnoderemovepropertydata-method"></a><span data-ttu-id="9edbd-103">Метод Иконтекстноде:: Ремовепропертидата</span><span class="sxs-lookup"><span data-stu-id="9edbd-103">IContextNode::RemovePropertyData method</span></span>

<span data-ttu-id="9edbd-104">Удаляет часть данных, зависящих от приложения.</span><span class="sxs-lookup"><span data-stu-id="9edbd-104">Removes a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9edbd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9edbd-105">Syntax</span></span>


```C++
HRESULT RemovePropertyData(
  [in] const GUID *pPropertyDataId
);
```



## <a name="parameters"></a><span data-ttu-id="9edbd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9edbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9edbd-107">*ппропертидатаид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9edbd-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9edbd-108">Идентификатор удаляемых данных.</span><span class="sxs-lookup"><span data-stu-id="9edbd-108">The identifier of the data to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9edbd-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9edbd-109">Return value</span></span>

<span data-ttu-id="9edbd-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9edbd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9edbd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9edbd-111">Remarks</span></span>

<span data-ttu-id="9edbd-112">**Д \_ INVALIDARG** возвращается, если параметр *ппропертидатаид* является одной из констант [свойств узла контекста](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="9edbd-112">**E\_INVALIDARG** is returned if the *pPropertyDataId* parameter is one of the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="9edbd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9edbd-113">Requirements</span></span>



| <span data-ttu-id="9edbd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9edbd-114">Requirement</span></span> | <span data-ttu-id="9edbd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9edbd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9edbd-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9edbd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9edbd-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9edbd-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9edbd-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9edbd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9edbd-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9edbd-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9edbd-120">Header</span><span class="sxs-lookup"><span data-stu-id="9edbd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9edbd-121"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9edbd-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9edbd-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9edbd-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9edbd-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9edbd-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9edbd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9edbd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9edbd-125">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="9edbd-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9edbd-126">**Иконтекстноде:: Аддпропертидата**</span><span class="sxs-lookup"><span data-stu-id="9edbd-126">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="9edbd-127">**Иконтекстноде:: Контаинспропертидата**</span><span class="sxs-lookup"><span data-stu-id="9edbd-127">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="9edbd-128">**Иконтекстноде:: Жетпропертидата**</span><span class="sxs-lookup"><span data-stu-id="9edbd-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="9edbd-129">**Иконтекстноде:: Жетпропертидатаидс**</span><span class="sxs-lookup"><span data-stu-id="9edbd-129">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="9edbd-130">**Иконтекстноде:: Лоадпропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="9edbd-130">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="9edbd-131">**Иконтекстноде:: Савепропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="9edbd-131">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="9edbd-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9edbd-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




