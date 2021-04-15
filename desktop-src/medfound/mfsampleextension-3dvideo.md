---
description: Указывает, содержит ли образец носителя трехмерный видеокадр.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: Атрибут MFSampleExtension_3DVideo (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701807"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>Мфсампликстенсион \_ 3DVideo, атрибут

Указывает, содержит ли образец носителя трехмерный видеокадр.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Комментарии

Если этот атрибут имеет **значение true**, пример носителя содержит видеокадр с двумя или более стереоскопик представлениями. Значение по умолчанию — **false**.

Компонент, создающий трехмерные видеокадры, должен установить для этого атрибута **значение true** на каждом образце носителя, содержащем трехмерный кадр.

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

[Мфсампликстенсион \_ 3DVideo \_ самплеформат](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




