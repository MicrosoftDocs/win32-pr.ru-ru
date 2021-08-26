---
description: Позволяет подсистеме захвата использовать кодировщик с ограничениями на использование полей.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: Атрибут MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f2fb9d85c68adbc726fa4b36f2ea960a33e68c4dff836fac0370c8e9e4e3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060824"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a>\_Запись о \_ кодировщике модуля записи MF \_ \_ \_ фиелдофусе \_ разблокировать \_ атрибут атрибута

Позволяет подсистеме захвата использовать кодировщик с ограничениями на использование полей.

## <a name="data-type"></a>Тип данных

**IUnknown\***

## <a name="remarks"></a>Remarks

Значением этого атрибута является указатель на интерфейс [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , реализованный вызывающим объектом. Реализация этого интерфейса в вызывающем объекте должна выполнять подтверждение с кодировщиком, как описано в разделе [ограничения использования](field-of-use-restrictions.md). Microsoft Media Foundation не определяет подтверждение, как правило, это влечет за собой некоторый вид криптографических обменов.

На внутреннем уровне подсистема отслеживания задает указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) на кодировщике, задавая атрибут [ \_ Фиелдофусе \_ Unlock \_](mft-fieldofuse-unlock-attribute.md) в файле MFT для кодировщика.

## <a name="requirements"></a>Requirements (Требования)



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

 

 




