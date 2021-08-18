---
description: Указывает максимальную скорость потока звука для приемника мультимедиа Digital живая Network Alliance (DLNA).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: Атрибут MF_MP2DLNA_AUDIO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed622a2f826e061dc4b909eec09490974fe83a7ac850cd0fcdfcede0abd578b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104770"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a>\_ \_ \_ Атрибут скорости звукового бита MP2DLNA \_ MF

Указывает максимальную скорость потока звука для приемника мультимедиа Digital живая Network Alliance (DLNA).

## <a name="data-type"></a>Тип данных

**UINT32**

Значение является целевой максимальной скоростью потока для закодированного аудиопотока в битах в секунду. Значение должно быть одной из битовых ставок, допустимых для звука MPEG-2 уровня 2 для DLNA. Значение по умолчанию — 192000 (192 кбит/с).

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarks

Чтобы задать этот атрибут для приемника мультимедиа DLNA, запросите приемник мультимедиа для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Задайте атрибут перед началом потоковой передачи.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




