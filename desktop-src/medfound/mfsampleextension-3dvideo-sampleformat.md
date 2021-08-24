---
description: Указывает, как трехмерный видеокадр хранится в примере носителя.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: Атрибут MFSampleExtension_3DVideo_SampleFormat (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6529a08c14846fb1d06cd9b3ed0827a43d1b1ba75310c0379efddadebecdaeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722874"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>Мфсампликстенсион \_ 3DVideo \_ самплеформат, атрибут

Указывает, как трехмерный видеокадр хранится в примере носителя.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Значение этого атрибута является членом перечисления [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .

Компонент, создающий трехмерные видеокадры, должен установить для этого атрибута **значение true** на каждом образце носителя, содержащем трехмерный кадр. Атрибут игнорируется, если атрибут [мфсампликстенсион \_ 3DVideo](mfsampleextension-3dvideo.md) имеет **значение false** или не задан.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Мфсампликстенсион \_ 3DVideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




