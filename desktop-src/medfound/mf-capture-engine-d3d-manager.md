---
description: Задает указатель на диспетчер устройств DXGI в подсистеме записи.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: Атрибут MF_CAPTURE_ENGINE_D3D_MANAGER (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154646"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a>\_ \_ \_ Атрибут диспетчера D3D ядра записи MF \_

Задает указатель на диспетчер устройств DXGI в подсистеме записи.

## <a name="data-type"></a>Тип данных

**IUnknown \** _

## <a name="remarks"></a>Комментарии

Значение этого атрибута является указателем на интерфейс [_ *имфдксгидевицеманажер* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . Этот атрибут позволяет подсистеме захвата выделять видеоматериалы с помощью поверхностей DXGI и использовать аппаратное ускорение для обработки декодирования и видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




