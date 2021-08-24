---
description: Задает диспетчер устройств в механизме мультимедиа Microsoft DirectX Graphics Framework (DXGI).
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: Атрибут MF_MEDIA_ENGINE_DXGI_MANAGER (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c454041f83a58cdb5b3c1e340d63908386546090eb52811e0c876e5d8bed0bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723057"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a>\_ \_ \_ Атрибут диспетчера DXGI для модуля передачи мультимедиа MF \_

Задает диспетчер устройств в механизме мультимедиа Microsoft DirectX Graphics Framework (DXGI).

## <a name="data-type"></a>Тип данных

**Имфдксгидевицеманажер \* *_ хранится как _* IUnknown\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Remarks

Значение этого атрибута является указателем на интерфейс [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

В режиме «Frame-Server» этот атрибут позволяет подсистеме мультимедиа использовать аппаратное ускорение при декодировании и обработке видео. Если атрибут не задан, подсистема мультимедиа использует программное декодирование и обработку.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Мфмедиаенгине. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




