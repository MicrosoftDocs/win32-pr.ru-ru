---
description: Отключает преобразование частоты кадров в MFT обработчика видео.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: Атрибут MF_XVP_DISABLE_FRC (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e82c60438a91111ffce6cc80c71fa76231b8e00d85644f4f56f1b496202d62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940334"
---
# <a name="mf_xvp_disable_frc-attribute"></a>MF \_ ксвп \_ Отключить \_ атрибут ФРК

Отключает преобразование частоты кадров в [**MFT обработчика видео**](video-processor-mft.md).

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Remarks

Если этот атрибут имеет **значение true**, обработчик видео не будет выполнять преобразование кадров. По умолчанию обработчик видео преобразует частоту кадров в соответствии с выходным типом носителя.

Чтобы задать этот атрибут, сделайте следующее:

1.  Вызовите [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в обработчике видео.
2.  Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Задайте атрибут перед началом потоковой передачи.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




