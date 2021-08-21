---
description: Позволяет подсистеме захвата использовать декодер с ограничениями на использование полей.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: Атрибут MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690f586325f883595e1336ed946611850b3c51d5443dbd9f6e68830502284a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061077"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a>\_ \_ \_ \_ \_ Фиелдофусе \_ разблокирование \_ атрибута MFT для декодера ядра записи MF

Позволяет подсистеме захвата использовать декодер с ограничениями на использование полей.

## <a name="data-type"></a>Тип данных

**IUnknown\***

## <a name="remarks"></a>Remarks

Значением этого атрибута является указатель на интерфейс [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , реализованный вызывающим объектом. Реализация этого интерфейса в вызывающем объекте должна выполнять подтверждение с помощью декодера, как описано в разделе [ограничения использования](field-of-use-restrictions.md). Microsoft Media Foundation не определяет подтверждение, как правило, это влечет за собой некоторый вид криптографических обменов.

На внутреннем уровне подсистема отслеживания устанавливает указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) на декодер, установив атрибут [ \_ \_ \_ атрибута MFT фиелдофусе Unlock](mft-fieldofuse-unlock-attribute.md) для декодера.

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

 

 




