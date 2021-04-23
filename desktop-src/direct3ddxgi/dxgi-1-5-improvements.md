---
description: В графическую инфраструктуру Microsoft DirectX (DXGI) 1,5 добавлены следующие функциональные возможности для поддержки более гибкого указания и дублирования форматов выходных данных.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: Усовершенствования DXGI 1,5
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 58df3ef78781437ee033530a2ed2179bb9a132d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351925"
---
# <a name="dxgi-15-improvements"></a><span data-ttu-id="60c4f-103">Усовершенствования DXGI 1,5</span><span class="sxs-lookup"><span data-stu-id="60c4f-103">DXGI 1.5 Improvements</span></span>

<span data-ttu-id="60c4f-104">В графическую инфраструктуру Microsoft DirectX (DXGI) 1,5 добавлены следующие функциональные возможности для поддержки более гибкого указания и дублирования форматов выходных данных.</span><span class="sxs-lookup"><span data-stu-id="60c4f-104">The following functionality has been added to Microsoft DirectX Graphics Infrastructure (DXGI) 1.5, to support more flexible specifying and duplication of output formats.</span></span>

## <a name="high-dynamic-range-and-wide-color-gamut"></a><span data-ttu-id="60c4f-105">Высокий динамический диапазон и широкий спектр цветов</span><span class="sxs-lookup"><span data-stu-id="60c4f-105">High Dynamic Range and Wide Color Gamut</span></span>

<span data-ttu-id="60c4f-106">См. статью [Использование DirectX с высоким динамическим диапазоном отображения и расширенным цветом](../direct3darticles/high-dynamic-range.md).</span><span class="sxs-lookup"><span data-stu-id="60c4f-106">Refer to [Using DirectX with high dynamic range displays and advanced color](../direct3darticles/high-dynamic-range.md).</span></span>

## <a name="variable-refresh-rate-displays"></a><span data-ttu-id="60c4f-107">Отображение частоты обновления переменных</span><span class="sxs-lookup"><span data-stu-id="60c4f-107">Variable refresh rate displays</span></span>

<span data-ttu-id="60c4f-108">См. [Отображение частоты обновления переменных](variable-refresh-rate-displays.md).</span><span class="sxs-lookup"><span data-stu-id="60c4f-108">Refer to [Variable refresh rate displays](variable-refresh-rate-displays.md).</span></span>

## <a name="duplicating-output"></a><span data-ttu-id="60c4f-109">Дублирование выходных данных</span><span class="sxs-lookup"><span data-stu-id="60c4f-109">Duplicating output</span></span>

<span data-ttu-id="60c4f-110">В DXGI 1,5 добавлен один интерфейс [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5)с одним методом [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), обеспечивающий более гибкую и более эффективную версию исходного метода [**дупликатеаутпут**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) .</span><span class="sxs-lookup"><span data-stu-id="60c4f-110">A single interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), with a single method, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), has been added to DXGI 1.5 to provide a more flexible and higher performance version of the original [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) method.</span></span> <span data-ttu-id="60c4f-111">**DuplicateOutput1** позволяет указать список поддерживаемых форматов для полноэкранных поверхностей, которые могут быть возвращены объектом [**идксгиаутпутдупликатион**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) , и включает запись содержимого HDR и ВКГ.</span><span class="sxs-lookup"><span data-stu-id="60c4f-111">**DuplicateOutput1** allows specifying a list of supported formats for fullscreen surfaces that can be returned by the [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) object, and enables capturing HDR and WCG content.</span></span>

## <a name="offering-and-reclaiming-resources"></a><span data-ttu-id="60c4f-112">Предложение и освобождение ресурсов</span><span class="sxs-lookup"><span data-stu-id="60c4f-112">Offering and Reclaiming Resources</span></span>

<span data-ttu-id="60c4f-113">Обновленные методы [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) и [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) были добавлены в новый интерфейс [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), чтобы можно было отменить фиксацию памяти в дополнение к удалению ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60c4f-113">Updated methods [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) and [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) have been added to a new interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), to allow de-committing of memory in addition to discarding resources.</span></span> <span data-ttu-id="60c4f-114">Включение в новый [**\_ флаг ресурсов для DXGI предлагает флаг \_ \_ \_ \_ дефиксации**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) означает, что новые результаты повторного утверждения должны обрабатываться правильно.</span><span class="sxs-lookup"><span data-stu-id="60c4f-114">Opting in to the new [**DXGI\_OFFER\_RESOURCE\_FLAG\_ALLOW\_DECOMMIT**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) flag means the new reclaim results must be properly handled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60c4f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="60c4f-115">Related topics</span></span>

[<span data-ttu-id="60c4f-116">Руководством по программированию для DXGI</span><span class="sxs-lookup"><span data-stu-id="60c4f-116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
