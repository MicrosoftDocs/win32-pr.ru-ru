---
description: Содержит указатель на диспетчер устройств DXGI для модуля записи приемника.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Атрибут MF_SINK_WRITER_D3D_MANAGER (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712857"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>\_ \_ \_ Атрибут диспетчера D3D модуля записи MF SINK \_

Содержит указатель на диспетчер устройств DXGI для [модуля записи приемника](sink-writer.md).

## <a name="data-type"></a>Тип данных

**Имфдксгидевицеманажер \** _ хранится как _*IUnknown \**_

## <a name="remarks"></a>Комментарии

Значение этого атрибута является указателем на интерфейс [_ *имфдксгидевицеманажер* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

Используйте этот атрибут, чтобы предоставить устройство Direct3D для любых видеокодировщиков или приемников мультимедиа, загруженных модулем записи приемника.

Используйте этот атрибут со следующими функциями:

-   [**мфкреатесинквритерфроммедиасинк**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**мфкреатесинквритерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфреадврите. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Модуль записи приемников](sink-writer.md)
</dt> </dl>

 

 




