---
description: Указывает, отфильтровывает ли приемник файлов MPEG-4 набор параметров последовательности (SPS) и набор параметров изображения (PPS) Налус.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: Атрибут MF_MPEG4SINK_SPSPPS_PASSTHROUGH (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b939302999fc7e095abbc97aed5910976972c860440a2c865248949e0f052aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104630"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>\_ \_ \_ Атрибут транзитного MPEG4SINK спсппс MF

Указывает, отфильтровывает ли [**приемник файлов MPEG-4**](mpeg-4-file-sink.md) набор параметров последовательности (SPS) и набор параметров изображения (PPS) налус.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="applies-to"></a>Применяется к

[**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Remarks

[**Приемник файлов MPEG-4**](mpeg-4-file-sink.md) записывает параметры SPS и PPS в поле Описание образца файла MP4. По умолчанию он фильтрует Налус SPS и PPS из видеопотока. Чтобы переопределить это поведение, присвойте \_ \_ \_ атрибуту passthrough MPEG4SINK Спсппс транзита **значение true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




