---
description: Обновляет данные пакета для указанных штрихов.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'Метод Иинканализер:: Упдатестрокесдата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701599"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a><span data-ttu-id="04ba7-103">Метод Иинканализер:: Упдатестрокесдата</span><span class="sxs-lookup"><span data-stu-id="04ba7-103">IInkAnalyzer::UpdateStrokesData method</span></span>

<span data-ttu-id="04ba7-104">Обновляет данные пакета для указанных штрихов.</span><span class="sxs-lookup"><span data-stu-id="04ba7-104">Updates the packet data for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ba7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04ba7-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="04ba7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04ba7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04ba7-107">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04ba7-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ba7-108">Число штрихов для обновления.</span><span class="sxs-lookup"><span data-stu-id="04ba7-108">The number of strokes to update.</span></span>

</dd> <dt>

<span data-ttu-id="04ba7-109">*плстрокеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04ba7-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ba7-110">Массив, содержащий идентификаторы штрихов.</span><span class="sxs-lookup"><span data-stu-id="04ba7-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="04ba7-111">*улстрокепаккетдескриптионкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04ba7-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ba7-112">Число свойств в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="04ba7-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="04ba7-113">*пстрокепаккетдескриптионгуидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04ba7-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ba7-114">Массив, содержащий идентификаторы свойств пакета.</span><span class="sxs-lookup"><span data-stu-id="04ba7-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="04ba7-115">*пулпаккетдатакаунтперстроке* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04ba7-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ba7-116">Массив, содержащий количество пакетов в каждом штрихе.</span><span class="sxs-lookup"><span data-stu-id="04ba7-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="04ba7-117">*плстрокепаккетдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04ba7-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ba7-118">Массив, содержащий данные пакета для штрихов.</span><span class="sxs-lookup"><span data-stu-id="04ba7-118">An array containing the packet data for the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04ba7-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04ba7-119">Return value</span></span>

<span data-ttu-id="04ba7-120">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="04ba7-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04ba7-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04ba7-121">Remarks</span></span>

<span data-ttu-id="04ba7-122">параметр *плстрокепаккетдата* содержит данные пакетов для всех штрихов.</span><span class="sxs-lookup"><span data-stu-id="04ba7-122">the *plStrokePacketData* parameter contains packet data for all of the strokes.</span></span> <span data-ttu-id="04ba7-123">Параметр *пстрокепаккетдескриптионгуидс* содержит глобальные уникальные идентификаторы (GUID), которые описывают типы данных пакетов, включаемые для каждой точки в каждом штрихе.</span><span class="sxs-lookup"><span data-stu-id="04ba7-123">The *pStrokePacketDescriptionGuids* parameter contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="04ba7-124">Полный список доступных свойств пакетов см. в разделе [константы паккетпропертигуидс](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="04ba7-124">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="04ba7-125">Только штрихи с одинаковыми описаниями пакетов могут быть обновлены в одном вызове **метода иинканализер:: упдатестрокесдата**.</span><span class="sxs-lookup"><span data-stu-id="04ba7-125">Only strokes with the same packet descriptions can be updated in a single call to **IInkAnalyzer::UpdateStrokesData Method**.</span></span>

<span data-ttu-id="04ba7-126">Этот метод не обновляет «грязную» область анализатора рукописного ввода (см. раздел [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="04ba7-126">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="04ba7-127">Если указанный штрих не связан с [**иинканализер**](iinkanalyzer.md), этот метод игнорирует идентификатор.</span><span class="sxs-lookup"><span data-stu-id="04ba7-127">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="04ba7-128">Если ни один из указанных штрихов не определяет штрих, связанный с [**иинканализер**](iinkanalyzer.md), этот метод возвращает значение без обновления **иинканализер**.</span><span class="sxs-lookup"><span data-stu-id="04ba7-128">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="04ba7-129">Этот метод возвращает код ошибки, если *плстрокеидс* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="04ba7-129">This method returns an error code when *plStrokeIds* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ba7-130">Требования</span><span class="sxs-lookup"><span data-stu-id="04ba7-130">Requirements</span></span>



| <span data-ttu-id="04ba7-131">Требование</span><span class="sxs-lookup"><span data-stu-id="04ba7-131">Requirement</span></span> | <span data-ttu-id="04ba7-132">Значение</span><span class="sxs-lookup"><span data-stu-id="04ba7-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04ba7-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04ba7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="04ba7-134">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="04ba7-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="04ba7-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04ba7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="04ba7-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="04ba7-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="04ba7-137">Header</span><span class="sxs-lookup"><span data-stu-id="04ba7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="04ba7-138"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="04ba7-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="04ba7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="04ba7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04ba7-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04ba7-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="04ba7-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04ba7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ba7-142">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="04ba7-142">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="04ba7-143">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="04ba7-143">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="04ba7-144">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="04ba7-144">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="04ba7-145">**Метод Иинканализер:: Аддстрокетокустомрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="04ba7-145">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="04ba7-146">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="04ba7-146">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="04ba7-147">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="04ba7-147">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="04ba7-148">**Метод Иинканализер:: Аддстрокестокустомрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="04ba7-148">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="04ba7-149">**Метод Иинканализер:: Клеарстрокедата**</span><span class="sxs-lookup"><span data-stu-id="04ba7-149">**IInkAnalyzer::ClearStrokeData Method**</span></span>](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[<span data-ttu-id="04ba7-150">**\_Ианалисисевентс:: Упдатестрокескаче**</span><span class="sxs-lookup"><span data-stu-id="04ba7-150">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="04ba7-151">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="04ba7-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




