---
description: Содержит указатель на диспетчер устройств DXGI для модуля записи приемника.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Атрибут MF_SINK_WRITER_D3D_MANAGER (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706287b6001ba52c8bf5ba8a19326948afcf4f7f7569c606507115f484c46f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714314"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>\_ \_ \_ Атрибут диспетчера D3D модуля записи MF SINK \_

Содержит указатель на диспетчер устройств DXGI для [модуля записи приемника](sink-writer.md).

## <a name="data-type"></a>Тип данных

**Имфдксгидевицеманажер \* *_ хранится как _* IUnknown\***

## <a name="remarks"></a>Remarks

Значение этого атрибута является указателем на интерфейс [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

Используйте этот атрибут, чтобы предоставить устройство Direct3D для любых видеокодировщиков или приемников мультимедиа, загруженных модулем записи приемника.

Используйте этот атрибут со следующими функциями:

-   [**мфкреатесинквритерфроммедиасинк**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**мфкреатесинквритерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфреадврите. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Модуль записи приемников](sink-writer.md)
</dt> </dl>

 

 




