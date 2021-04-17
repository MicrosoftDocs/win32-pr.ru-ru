---
description: Задает диспетчер устройств в механизме мультимедиа Microsoft DirectX Graphics Framework (DXGI).
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: Атрибут MF_MEDIA_ENGINE_DXGI_MANAGER (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703435"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a>\_ \_ \_ Атрибут диспетчера DXGI для модуля передачи мультимедиа MF \_

Задает диспетчер устройств в механизме мультимедиа Microsoft DirectX Graphics Framework (DXGI).

## <a name="data-type"></a>Тип данных

**Имфдксгидевицеманажер \* *_ хранится как _* IUnknown\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Комментарии

Значение этого атрибута является указателем на интерфейс [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

В режиме «Frame-Server» этот атрибут позволяет подсистеме мультимедиа использовать аппаратное ускорение при декодировании и обработке видео. Если атрибут не задан, подсистема мультимедиа использует программное декодирование и обработку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                                |
| Header<br/>                   | <dl> <dt>Мфмедиаенгине. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




