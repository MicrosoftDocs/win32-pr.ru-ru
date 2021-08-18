---
description: Атрибуты модуля записи приемника
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Атрибуты модуля записи приемника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bf64dd4279ef2e35ed86f50c4444412b3cc70205f6aad52adac8a41895af11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012373"
---
# <a name="sink-writer-attributes"></a>Атрибуты модуля записи приемника

Для инициализации модуля записи приемника можно использовать следующие атрибуты.



| attribute                                                                                  | Описание                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ низкая \_ Задержка](mf-low-latency.md)                                                     | Включает обработку с низкой задержкой.                                                                                                                                                                                                    |
| [\_ \_ запретить \_ конвертеры MF ReadWrite](mf-readwrite-disable-converters.md)                  | Включает или отключает преобразование формата модулем записи приемника.                                                                                                                                                                         |
| [MF. \_ Чтение с \_ включением \_ аппаратных \_ преобразований](mf-readwrite-enable-hardware-transforms.md) | Позволяет модулю записи приемника использовать Media Foundation преобразования на основе оборудования (МФТС).                                                                                                                                                  |
| [\_ \_ \_ асинхронный обратный вызов для модуля записи MF SINK \_](mf-sink-writer-async-callback.md)                     | Содержит указатель на интерфейс обратного вызова приложения для модуля записи приемника.                                                                                                                                                    |
| [Программа \_ записи приемника MF \_ \_ отключает \_ регулирование](mf-sink-writer-disable-throttling.md)             | Указывает, ограничивает ли модуль записи приемника скорость входящих данных.                                                                                                                                                                |
| [MF \_ \_ контаинертипе](mf-transcode-containertype.md)                             | Указывает тип контейнера выходного файла.                                                                                                                                                                                   |
| [\_Атрибут MFT фиелдофусе \_ Unlock \_](mft-fieldofuse-unlock-attribute.md)                  | Содержит указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , который используется для разблокировки MFT с ограничениями на использование полей. Дополнительные сведения см. в разделе [ограничения использования](field-of-use-restrictions.md). |
| [\_ \_ Диспетчер D3D модуля записи MF SINK \_ \_](mf-sink-writer-d3d-manager.md)                           | Используйте этот атрибут, чтобы предоставить устройство Direct3D для любых видеокодировщиков или приемников мультимедиа, загруженных модулем записи приемника.                                                                                                                   |



 

Используйте эти атрибуты со следующими методами и функциями:

-   [**Имфреадвритеклассфактори:: Креатеинстанцефромобжект**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**Имфреадвритеклассфактори:: Креатеинстанцефромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**мфкреатесинквритерфроммедиасинк**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**мфкреатесинквритерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Чтобы использовать любой из этих атрибутов, сначала вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать новое хранилище атрибутов. Затем используйте интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , чтобы задать необходимые атрибуты в хранилище атрибутов. Передайте указатель **имфаттрибутес** в параметр *паттрибутес* любого из указанных выше методов или функций.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**имфсинквритер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



