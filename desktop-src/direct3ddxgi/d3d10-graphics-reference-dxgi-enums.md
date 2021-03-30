---
description: В этом разделе содержатся сведения о перечислениях, предоставляемых DXGI.
ms.assetid: c4574c89-dee2-4841-9318-5383cf417111
title: Перечисления DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49f8309552662d0edd9833ce037a256c3c09c48
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805596"
---
# <a name="dxgi-enumerations"></a>Перечисления DXGI

В этом разделе содержатся сведения о перечислениях, предоставляемых DXGI.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                         | Описание                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_флаг адаптера \_ DXGI**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag)<br/>                                          | Определяет тип адаптера DXGI.<br/>                                                                                                                                   |
| [**\_FLAG3 адаптера \_ DXGI**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)<br/>                                        | Определяет тип адаптера DXGI.<br/>                                                                                                                                   |
| [**\_режим альфа-канала DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)<br/>                                                       | Определяет альфа-значение, режим прозрачности поверхности.<br/>                                                                                                       |
| [**\_тип цветового \_ пространства DXGI \_**](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)<br/>                                          | Задает типы цветового пространства.<br/>                                                                                                                                           |
| [**\_гранулярность вычислений среды DXGI \_ \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity)<br/>              | Определяет гранулярность, с которой графический процессор (GPU) может быть вытеснен из выполнения текущей вычислительной задачи.<br/>                                      |
| [**\_ \_ Флаги РЛО отладки DXGI \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_debug_rlo_flags)<br/>                                            | Флаги, используемые с параметром [**репортливеобжектс**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgidebug-reportliveobjects) для указания объема сведений о времени существования объекта. <br/>                         |
| [**\_функция DXGI**](/windows/desktop/api/DXGI1_5/ne-dxgi1_5-dxgi_feature)<br/>                                                              | Указывает ряд аппаратных компонентов, которые будут использоваться при проверке поддержки компонентов.<br/>                                                                                  |
| [**\_Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br/>                                                       | Форматы данных ресурсов, включая полностью типизированные и нетипизированные форматы. Список модификаторов в нижней части страницы более полно описывает каждый тип формата. <br/>               |
| [**\_ \_ режим презентации кадра \_ DXGI**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode)<br/>                            | Указывает параметры для представления кадров в цепочке буферов. <br/>                                                                                                            |
| [**\_настройки GPU для DXGI \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)<br/>                                               | Предпочтение GPU для запуска приложения.<br/>                                                                                                                           |
| [**\_ \_ гранулярность вытеснения графики \_ DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity)<br/>            | Определяет гранулярность, с которой GPU может быть вытеснен из выполнения текущей задачи отрисовки графики.<br/>                                                      |
| [**\_ \_ \_ Флаги поддержки композиции АППАРАТного обеспечения DXGI \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)<br/>     | Описывает, какие уровни аппаратного содержимого поддерживаются.<br/>                                                                                                          |
| [**\_ \_ тип метаданных HDR для DXGI \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type)<br/>                                        | Указывает тип метаданных заголовка.<br/>                                                                                                                                    |
| [**\_ \_ \_ Категория сообщения очереди сообщений о DXGI \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_category)<br/>                   | Значения, указывающие категории сообщений отладки.<br/>                                                                                                                      |
| [**\_ \_ \_ серьезность сообщения очереди сообщений о DXGI \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_severity)<br/>                   | Значения, задающих уровни серьезности сообщения отладки для информационной очереди.<br/>                                                                                            |
| [**\_ \_ Группа сегментов памяти \_ DXGI**](/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)<br/>                                  | Указывает используемую группу сегментов памяти.<br/>                                                                                                                             |
| [**\_вращение в режиме DXGI \_**](/previous-versions/windows/desktop/legacy/bb173065(v=vs.85))<br/>                                        | Флаги, указывающие способ вращения задних буферов в соответствии с физическим поворотом монитора.<br/>                                                                  |
| [**\_масштабирование в режиме DXGI \_**](/previous-versions/windows/desktop/legacy/bb173066(v=vs.85))<br/>                                          | Флаги, указывающие, как изображение растягивается в соответствии с разрешением данного монитора.<br/>                                                                                        |
| [**\_ \_ порядок сканлине в режиме DXGI \_**](/previous-versions/windows/desktop/legacy/bb173067(v=vs.85))<br/>                           | Флаги, указывающие метод, используемый растровым изображением для создания изображения на поверхности.<br/>                                                                                           |
| [**\_Флаги икбкр МНОГОпланового \_ наложения для DXGI \_ \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags)<br/>             | Параметры для цветового пространства цепочки подкачки.<br/>                                                                                                                                    |
| [**\_ \_ флаги ресурсов предложения DXGI \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags)<br/>                                  | Задает флаги для метода [**OfferResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) .<br/>                                                                                |
| [**\_ \_ приоритет ресурсов для предложения DXGI \_**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority)<br/>                           | Определяет важность содержимого ресурса при вызове метода [**IDXGIDevice2:: офферресаурцес**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) для предоставления ресурса. <br/> |
| [**\_ \_ \_ Тип фигуры указателя аутдупл \_ DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type)<br/>                     | Определяет тип фигуры указателя.<br/>                                                                                                                                  |
| [**\_ \_ \_ \_ флаг поддержки цветового пространства наложения DXGI \_**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag)<br/>        | Задает поддержку цветового пространства оверлея.<br/>                                                                                                                             |
| [**\_флаг поддержки наложения DXGI \_ \_**](/windows/desktop/api/DXGI1_3/ne-dxgi1_3-dxgi_overlay_support_flag)<br/>                                  | Задает поддержку наложения для проверки в вызове [**IDXGIOutput3:: чекковерлайсуппорт**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgioutput3-checkoverlaysupport).<br/>                                     |
| [**\_ \_ результаты освобождения ресурсов \_ DXGI**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results)<br/>                          | Задает флаги результата для метода [**ReclaimResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) .<br/>                                                                     |
| [**\_местонахождение DXGI**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency)<br/>                                                 | Флаги, указывающие расположение памяти ресурса.<br/>                                                                                                                    |
| [**\_масштабирование DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling)<br/>                                                              | Определяет поведение при изменении размера, если размер заднего буфера не соответствует размеру целевого результата.<br/>                                                                     |
| [**\_ \_ \_ флаг поддержки цветового \_ пространства ЦЕПОЧКи \_ подкачки DXGI \_**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag)<br/> | Задает поддержку цветового пространства для цепочки буферов.<br/>                                                                                                                      |
| [**\_ \_ флаг цепочки переключения DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)<br/>                                   | Параметры для поведения цепочки подкачки.<br/>                                                                                                                                       |
| [**\_воздействие переключения на DXGI \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)<br/>                                                     | Параметры обработки пикселов в отображаемой поверхности после вызова [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). <br/>                                         |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

