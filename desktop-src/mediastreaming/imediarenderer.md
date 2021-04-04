---
title: Интерфейс Имедиарендерер
description: Инкапсулирует методы и события, необходимые для представления устройства визуализации цифрового мультимедиа DLNA (ДМР).
ms.assetid: FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB
keywords:
- API потоковой передачи мультимедиа интерфейса Имедиарендерер
- API потоковой передачи мультимедиа интерфейса Имедиарендерер, описание
topic_type:
- apiref
api_name:
- IMediaRenderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 363db88b67d29d92b1e79516056f5fa8e78ca22e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987464"
---
# <a name="imediarenderer-interface"></a>Интерфейс Имедиарендерер

Инкапсулирует методы и события, необходимые для представления устройства визуализации цифрового мультимедиа DLNA (ДМР).

## <a name="members"></a>Элементы

Интерфейс **имедиарендерер** наследует от [**ибасикдевице**](ibasicdevice.md). **Имедиарендерер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **имедиарендерер** содержит следующие методы.



| Метод                                                                                        | Описание                                                                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**актионинформатион**](imediarenderer-actioninformation.md)                                 | Извлекает сведения о том, какие методы в данный момент можно вызывать в ДМР.<br/>                                                                                                                                                                                                                                                                                    |
| [**добавить \_ рендерингпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate)        | Регистрирует обработчик событий для события [**рендерингпараметерсупдате**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                          |
| [**добавить \_ транспортпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate)        | Регистрирует обработчик событий для события [**транспортпараметерсупдате**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                          |
| [**жетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)                                           | Асинхронно запрашивает ДМР, чтобы определить, не отключен ли звук.<br/>                                                                                                                                                                                                                                                                               |
| [**жетпоситионинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync)             | Асинхронно запрашивает ДМР для получения сведений о положении.<br/>                                                                                                                                                                                                                                                                                                  |
| [**жеттранспортинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)           | Асинхронно запрашивает ДМР для получения сведений о транспорте.<br/>                                                                                                                                                                                                                                                                                                 |
| [**жетволумеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)                                       | Асинхронно запрашивает ДМР для текущего уровня громкости звука.<br/>                                                                                                                                                                                                                                                                                                |
| [**исаудиосуппортед**](imediarenderer-isaudiosupported.md)                                   | Получает значение, указывающее, способен ли ДМР воспроизведение звукового содержимого.<br/>                                                                                                                                                                                                                                                                             |
| [**исимажесуппортед**](imediarenderer-isimagesupported.md)                                   | Получает значение, указывающее, поддерживает ли ДМР отображение изображений.<br/>                                                                                                                                                                                                                                                                                 |
| [**исвидеосуппортед**](imediarenderer-isvideosupported.md)                                   | Получает значение, указывающее, поддерживает ли ДМР воспроизведение видеосодержимого.<br/>                                                                                                                                                                                                                                                                             |
| [**паусеасинк**](imediarenderer-pauseasync.md)                                               | Указывает ДМР асинхронно приостановить воспроизведение текущего содержимого.<br/>                                                                                                                                                                                                                                                                                            |
| [**плайасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync)                                                 | Указывает ДМР асинхронно воспроизводить содержимое, указанное при вызове метода [**сетсаурцефромуриасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromuriasync), [**сетсаурцефромстреамасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromstreamasync)или [**сетсаурцефроммедиасаурцеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefrommediasourceasync) .<br/>                       |
| [**плайатспидасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync)                                   | Указывает ДМР асинхронно воспроизводить содержимое, указанное путем вызова метода [**сетсаурцефромуриасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromuriasync), [**сетсаурцефромстреамасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromstreamasync)или [**сетсаурцефроммедиасаурцеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefrommediasourceasync) с указанной скоростью.<br/> |
| [**удалить \_ рендерингпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate)  | Отменяет регистрацию обработчика событий для события [**рендерингпараметерсупдате**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                        |
| [**удалить \_ транспортпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate)  | Отменяет регистрацию обработчика событий для события [**транспортпараметерсупдате**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                        |
| [**сикасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync)                                                 | Указывает ДМР асинхронно искать определенное смещение времени.<br/>                                                                                                                                                                                                                                                                                             |
| [**сетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setmuteasync)                                           | Указывает ДМР асинхронно включить или отключить звук. <br/>                                                                                                                                                                                                                                                                                             |
| [**сетнекстсаурцефроммедиасаурцеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) | Указывает ДМР асинхронно подготовить указанное содержимое для воспроизведения после завершения воспроизведения текущего содержимого.<br/>                                                                                                                                                                                                                                      |
| [**сетнекстсаурцефромстреамасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync)           | Указывает ДМР асинхронно подготовить указанный поток мультимедиа для воспроизведения после завершения воспроизведения текущего содержимого.<br/>                                                                                                                                                                                                                                 |
| [**сетнекстсаурцефромуриасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync)                 | Указывает ДМР асинхронно подготовить содержимое, определяемое указанным URI, для воспроизведения после завершения воспроизведения текущего содержимого.<br/>                                                                                                                                                                                                                |
| [**сетсаурцефроммедиасаурцеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefrommediasourceasync)         | Указывает ДМР асинхронно подготовить указанное содержимое для воспроизведения.<br/>                                                                                                                                                                                                                                                                                    |
| [**сетсаурцефромстреамасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromstreamasync)                   | Указывает ДМР асинхронно подготовить указанный поток мультимедиа для воспроизведения.<br/>                                                                                                                                                                                                                                                                               |
| [**сетсаурцефромуриасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromuriasync)                         | Указывает ДМР асинхронно подготовить содержимое, определяемое указанным URI для воспроизведения.<br/>                                                                                                                                                                                                                                                              |
| [**сетволумеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setvolumeasync)                                       | Задает уровень громкости звука в ДМР асинхронно до указанного значения.<br/>                                                                                                                                                                                                                                                                                     |
| [**StopAsync**](imediarenderer-stopasync.md)                                                 | Указывает ДМР асинхронно закончить воспроизведение текущего содержимого.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибасикдевице**](ibasicdevice.md)
</dt> </dl>

 

