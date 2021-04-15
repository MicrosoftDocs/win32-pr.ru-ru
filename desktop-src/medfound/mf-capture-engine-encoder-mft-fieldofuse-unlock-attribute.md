---
description: Позволяет подсистеме захвата использовать кодировщик с ограничениями на использование полей.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: Атрибут MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a9466162ff5551ee155343800d938276823ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263635"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a>\_Запись о \_ кодировщике модуля записи MF \_ \_ \_ фиелдофусе \_ разблокировать \_ атрибут атрибута

Позволяет подсистеме захвата использовать кодировщик с ограничениями на использование полей.

## <a name="data-type"></a>Тип данных

**IUnknown \** _

## <a name="remarks"></a>Комментарии

Значением этого атрибута является указатель на интерфейс [_ *имффиелдофусемфтунлокк* *](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , реализованный вызывающим объектом. Реализация этого интерфейса в вызывающем объекте должна выполнять подтверждение с кодировщиком, как описано в разделе [ограничения использования](field-of-use-restrictions.md). Microsoft Media Foundation не определяет подтверждение, как правило, это влечет за собой некоторый вид криптографических обменов.

На внутреннем уровне подсистема отслеживания задает указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) на кодировщике, задавая атрибут [ \_ Фиелдофусе \_ Unlock \_](mft-fieldofuse-unlock-attribute.md) в файле MFT для кодировщика.

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

 

 




