---
description: Обновляет область этого Иконтекстноде.
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'Метод Иконтекстноде:: SetLocation (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701605"
---
# <a name="icontextnodesetlocation-method"></a><span data-ttu-id="84f1a-103">Метод Иконтекстноде:: SetLocation</span><span class="sxs-lookup"><span data-stu-id="84f1a-103">IContextNode::SetLocation method</span></span>

<span data-ttu-id="84f1a-104">Обновляет область этого [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="84f1a-104">Updates the area of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="84f1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84f1a-105">Syntax</span></span>


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="84f1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84f1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f1a-107">*пианалисисрегион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84f1a-107">*pIAnalysisRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f1a-108">[**Ианалисисрегион**](ianalysisregion.md) , описывающий область, в которую задается расположение объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="84f1a-108">The [**IAnalysisRegion**](ianalysisregion.md) describing the area to which to set the [**IContextNode**](icontextnode.md) object's location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f1a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84f1a-109">Return value</span></span>

<span data-ttu-id="84f1a-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="84f1a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="84f1a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84f1a-111">Remarks</span></span>

<span data-ttu-id="84f1a-112">Используйте этот метод для обновления расположения узла контекста (см. раздел [**иконтекстноде:: OnLocation**](icontextnode-getlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="84f1a-112">Use this method to update the context node's location (see [**IContextNode::GetLocation**](icontextnode-getlocation.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="84f1a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="84f1a-113">Requirements</span></span>



| <span data-ttu-id="84f1a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="84f1a-114">Requirement</span></span> | <span data-ttu-id="84f1a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="84f1a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f1a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84f1a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="84f1a-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="84f1a-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="84f1a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84f1a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="84f1a-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="84f1a-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="84f1a-120">Header</span><span class="sxs-lookup"><span data-stu-id="84f1a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="84f1a-121"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="84f1a-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="84f1a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="84f1a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f1a-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84f1a-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="84f1a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84f1a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f1a-125">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="84f1a-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="84f1a-126">**ианалисисрегион**</span><span class="sxs-lookup"><span data-stu-id="84f1a-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="84f1a-127">**Иконтекстноде:: OnLocation**</span><span class="sxs-lookup"><span data-stu-id="84f1a-127">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
</dt> <dt>

[<span data-ttu-id="84f1a-128">**Иконтекстноде:: Жетпартиаллипопулатед**</span><span class="sxs-lookup"><span data-stu-id="84f1a-128">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="84f1a-129">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="84f1a-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




