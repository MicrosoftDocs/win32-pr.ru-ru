---
description: Этот атрибут указывает дополнительную защиту, предлагаемую центром доверенного видео (OTA), если соединитель не поддерживает выходную защиту.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: Атрибут MFPROTECTION_CONSTRICTVIDEO_NOOPM (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72d1d7cd858ec9cf254cca1dffc5fef4e24fbb5a3a288975a9f70c9ae118dde3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713744"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a>МФПРОТЕКТИОН \_ констриктвидео \_ нупм, атрибут

Этот атрибут указывает дополнительную защиту, предлагаемую центром доверенного видео (OTA), если соединитель не поддерживает выходную защиту.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Remarks

Это дополнительная защита, предоставляемая беспроводным центром управления видео (OTA), если соединитель не поддерживает выходную защиту (см.[**имфаутпуттрустаусорити**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)). В этом случае OTA может предложить такую защиту, которая действует так же, как и защита [мфпротектион \_ констриктвидео](mfprotection-constrictvideo.md) . Это определено, чтобы избежать путаницы с предыдущими вызовами [**имфаутпутполици:: женератерекуиредсчемас**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) взаимодействия, в которых \_ для определения псевдо-соединителя диспетчера окон настольных систем используется защита мфпротектион констриктвидео.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




