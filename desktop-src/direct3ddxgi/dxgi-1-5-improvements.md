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
# <a name="dxgi-15-improvements"></a>Усовершенствования DXGI 1,5

В графическую инфраструктуру Microsoft DirectX (DXGI) 1,5 добавлены следующие функциональные возможности для поддержки более гибкого указания и дублирования форматов выходных данных.

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Высокий динамический диапазон и широкий спектр цветов

См. статью [Использование DirectX с высоким динамическим диапазоном отображения и расширенным цветом](../direct3darticles/high-dynamic-range.md).

## <a name="variable-refresh-rate-displays"></a>Отображение частоты обновления переменных

См. [Отображение частоты обновления переменных](variable-refresh-rate-displays.md).

## <a name="duplicating-output"></a>Дублирование выходных данных

В DXGI 1,5 добавлен один интерфейс [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5)с одним методом [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), обеспечивающий более гибкую и более эффективную версию исходного метода [**дупликатеаутпут**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) . **DuplicateOutput1** позволяет указать список поддерживаемых форматов для полноэкранных поверхностей, которые могут быть возвращены объектом [**идксгиаутпутдупликатион**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) , и включает запись содержимого HDR и ВКГ.

## <a name="offering-and-reclaiming-resources"></a>Предложение и освобождение ресурсов

Обновленные методы [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) и [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) были добавлены в новый интерфейс [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), чтобы можно было отменить фиксацию памяти в дополнение к удалению ресурсов. Включение в новый [**\_ флаг ресурсов для DXGI предлагает флаг \_ \_ \_ \_ дефиксации**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) означает, что новые результаты повторного утверждения должны обрабатываться правильно.

## <a name="related-topics"></a>См. также

[Руководством по программированию для DXGI](dx-graphics-dxgi-overviews.md)
