---
description: Очищает данные пакета обводки от Иинканализер.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'Метод Иинканализер:: Клеарстрокедата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 823ceaa825b454af851fab43e233526285445c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497565"
---
# <a name="iinkanalyzerclearstrokedata-method"></a><span data-ttu-id="cd353-103">Метод Иинканализер:: Клеарстрокедата</span><span class="sxs-lookup"><span data-stu-id="cd353-103">IInkAnalyzer::ClearStrokeData method</span></span>

<span data-ttu-id="cd353-104">Очищает данные пакета обводки от [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="cd353-104">Clears stroke packet data from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd353-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd353-105">Syntax</span></span>


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="cd353-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd353-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd353-107">*лстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd353-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd353-108">Идентификатор штриха, для которого очищаются данные пакета.</span><span class="sxs-lookup"><span data-stu-id="cd353-108">The identifier of the stroke for which the packet data is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd353-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd353-109">Return value</span></span>

<span data-ttu-id="cd353-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cd353-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd353-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd353-111">Remarks</span></span>

<span data-ttu-id="cd353-112">Используйте этот метод при изменении данных пакета для штриха, например при перемещении или преобразовании штриха.</span><span class="sxs-lookup"><span data-stu-id="cd353-112">Use this method when packet data for a stroke changes, such as when a stroke is moved or otherwise transformed.</span></span> <span data-ttu-id="cd353-113">[**Иинканализер**](iinkanalyzer.md) вызывает событие [**\_ ианалисисевентс:: упдатестрокескаче**](-ianalysisevents-updatestrokescache.md) , когда ему требуются данные пакета Stroke из штриха, для которого были удалены данные пакета.</span><span class="sxs-lookup"><span data-stu-id="cd353-113">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event when it needs stroke packet data from a stroke for which the packet data has been cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd353-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cd353-114">Requirements</span></span>



| <span data-ttu-id="cd353-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cd353-115">Requirement</span></span> | <span data-ttu-id="cd353-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cd353-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd353-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd353-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd353-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cd353-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cd353-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd353-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd353-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cd353-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cd353-121">Header</span><span class="sxs-lookup"><span data-stu-id="cd353-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd353-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cd353-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cd353-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cd353-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd353-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd353-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cd353-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd353-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd353-126">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="cd353-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cd353-127">**Метод Иинканализер:: Упдатестрокесдата**</span><span class="sxs-lookup"><span data-stu-id="cd353-127">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="cd353-128">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="cd353-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




