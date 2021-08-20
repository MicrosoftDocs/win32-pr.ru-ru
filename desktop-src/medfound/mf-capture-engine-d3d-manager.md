---
description: Задает указатель на диспетчер устройств DXGI в подсистеме записи.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: Атрибут MF_CAPTURE_ENGINE_D3D_MANAGER (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd8db74da2a55bba4eb0a50f48d80a31d3f75514f5f20b5d0d1329a63b71a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061157"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a>\_ \_ \_ Атрибут диспетчера D3D ядра записи MF \_

Задает указатель на диспетчер устройств DXGI в подсистеме записи.

## <a name="data-type"></a>Тип данных

**IUnknown\***

## <a name="remarks"></a>Remarks

Значение этого атрибута является указателем на интерфейс [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . Этот атрибут позволяет подсистеме захвата выделять видеоматериалы с помощью поверхностей DXGI и использовать аппаратное ускорение для обработки декодирования и видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                         |
| Заголовок<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




