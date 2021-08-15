---
description: Определяет компонент, создавший событие записи.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: Атрибут MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88efff7cea540c1fae2c14d44dd7676c4f523b562a66a4c4f4bc4dffea59d5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474472"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a>\_ \_ \_ \_ Атрибут GUID генератора событий ядра записи MF \_

Определяет компонент, создавший событие записи.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Remarks

Этот атрибут отображается для некоторых событий в подсистеме захвата. Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) GetObject в объекте события. Объект события передается в приложение через метод [**имфкаптурингинеоневенткаллбакк:: oneven**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .

Значение представляет собой идентификатор интерфейса для компонента, создавшего событие. Например, значение **IID \_ имфкаптурепревиевсинк** указывает на приемник предварительной версии ([**имфкаптурепревиевсинк**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)). Не все события захвата содержат этот атрибут.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




