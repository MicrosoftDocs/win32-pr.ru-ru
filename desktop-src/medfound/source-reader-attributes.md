---
description: Атрибуты модуля чтения исходного кода
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: Атрибуты модуля чтения исходного кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7bd9c5b3c5a71fb1b91515400fb0cf3670bd3b73b6635c811dcc79bd05e74f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238332"
---
# <a name="source-reader-attributes"></a>Атрибуты модуля чтения исходного кода

Для инициализации [модуля чтения исходного кода](source-reader.md)можно использовать следующие атрибуты.



| attribute                                                                                                            | Описание                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ низкая \_ Задержка](mf-low-latency.md)                                                                               | Включает обработку с низкой задержкой.                                                                                                                                                                                                    |
| [\_ \_ запретить \_ конвертеры MF ReadWrite](mf-readwrite-disable-converters.md)                                            | Включает или отключает преобразование форматов модулем чтения исходного кода.                                                                                                                                                                       |
| [MF. \_ Чтение с \_ включением \_ аппаратных \_ преобразований](mf-readwrite-enable-hardware-transforms.md)                           | Позволяет модулю чтения исходного кода использовать преобразования Media Foundation на основе оборудования (МФТС).                                                                                                                                                |
| [\_ \_ \_ асинхронный обратный вызов для СЧИТЫВАТЕЛя источника MF \_](mf-source-reader-async-callback.md)                                           | Содержит указатель на интерфейс обратного вызова приложения для модуля чтения исходного кода.                                                                                                                                                  |
| [\_ \_ \_ Диспетчер D3D чтения источника \_ MF](mf-source-reader-d3d-manager.md)                                                 | Содержит указатель на [Диспетчер устройств Microsoft Direct3D](direct3d-device-manager.md).                                                                                                                                        |
| [\_чтение источника \_ MF \_ Отключить \_ дксва](mf-source-reader-disable-dxva.md)                                               | Указывает, включает ли модуль чтения исходного экрана ускорение видео DirectX (ДКСВА) для видеодекодера.                                                                                                                                |
| [MF \_ source \_ Reader \_ отключение \_ медиасаурце \_ при \_ завершении работы](mf-source-reader-disconnect-mediasource-on-shutdown.md) | Указывает, завершает ли модуль чтения источника носитель.<br/> Применяется только в том случае, если приложение создает модуль чтения исходного кода из существующего объекта источника мультимедиа.<br/>                                           |
| [канал MF, \_ \_ считыватель источников, \_ включить \_ расширенную \_ \_ обработку видео](mf-source-reader-enable-advanced-video-processing.md)     | Включает расширенную обработку видео [модулем чтения исходного кода](source-reader.md), включая преобразование цветового пространства, дечередование, изменение размера видео и преобразование кадрового потока.                                                           |
| [канал MF, \_ \_ считыватель источников, \_ включить \_ \_ обработку видео](mf-source-reader-enable-video-processing.md)                        | Включает ограниченную обработку видео модулем чтения исходного кода.                                                                                                                                                                             |
| [\_ \_ \_ файл конфигурации медиасаурце чтения с источника MF \_](mf-source-reader-mediasource-config.md)                                   | Содержит свойства конфигурации для источника мультимедиа.                                                                                                                                                                            |
| [\_Атрибут MFT фиелдофусе \_ Unlock \_](mft-fieldofuse-unlock-attribute.md)                                            | Содержит указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , который используется для разблокировки MFT с ограничениями на использование полей. Дополнительные сведения см. в разделе [ограничения использования](field-of-use-restrictions.md). |



 

Используйте эти атрибуты со следующими методами и функциями:

-   [**Имфреадвритеклассфактори:: Креатеинстанцефромобжект**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**Имфреадвритеклассфактори:: Креатеинстанцефромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**мфкреатесаурцереадерфромбитестреам**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**мфкреатесаурцереадерфроммедиасаурце**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Чтобы использовать любой из этих атрибутов, сначала вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать новое хранилище атрибутов. Затем используйте интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , чтобы задать необходимые атрибуты в хранилище атрибутов. Передайте указатель **имфаттрибутес** в параметр *паттрибутес* любого из указанных выше методов или функций.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Модуль чтения исходного кода](source-reader.md)
</dt> <dt>

[**имфсаурцереадер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




