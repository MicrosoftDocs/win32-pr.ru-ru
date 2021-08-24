---
description: Указывает, содержит ли образец носителя трехмерный видеокадр.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: Атрибут MFSampleExtension_3DVideo (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb959accfb3326e90068a26247eeab25e9aeaddacb720a0dfd64aa6e5b237a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722804"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>Мфсампликстенсион \_ 3DVideo, атрибут

Указывает, содержит ли образец носителя трехмерный видеокадр.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Remarks

Если этот атрибут имеет **значение true**, пример носителя содержит видеокадр с двумя или более стереоскопик представлениями. Значение по умолчанию — **FALSE**.

Компонент, создающий трехмерные видеокадры, должен установить для этого атрибута **значение true** на каждом образце носителя, содержащем трехмерный кадр.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Мфсампликстенсион \_ 3DVideo \_ самплеформат](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




