---
description: Указывает, как трехмерный видеокадр хранится в примере носителя.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: Атрибут MFSampleExtension_3DVideo_SampleFormat (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155974"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>Мфсампликстенсион \_ 3DVideo \_ самплеформат, атрибут

Указывает, как трехмерный видеокадр хранится в примере носителя.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Значение этого атрибута является членом перечисления [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .

Компонент, создающий трехмерные видеокадры, должен установить для этого атрибута **значение true** на каждом образце носителя, содержащем трехмерный кадр. Атрибут игнорируется, если атрибут [мфсампликстенсион \_ 3DVideo](mfsampleextension-3dvideo.md) имеет **значение false** или не задан.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Мфсампликстенсион \_ 3DVideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




