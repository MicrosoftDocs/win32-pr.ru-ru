---
description: Указывает, отфильтровывает ли приемник файлов MPEG-4 набор параметров последовательности (SPS) и набор параметров изображения (PPS) Налус.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: Атрибут MF_MPEG4SINK_SPSPPS_PASSTHROUGH (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811855"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>\_ \_ \_ Атрибут транзитного MPEG4SINK спсппс MF

Указывает, отфильтровывает ли [**приемник файлов MPEG-4**](mpeg-4-file-sink.md) набор параметров последовательности (SPS) и набор параметров изображения (PPS) налус.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="applies-to"></a>Применяется к

[**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Комментарии

[**Приемник файлов MPEG-4**](mpeg-4-file-sink.md) записывает параметры SPS и PPS в поле Описание образца файла MP4. По умолчанию он фильтрует Налус SPS и PPS из видеопотока. Чтобы переопределить это поведение, присвойте \_ \_ \_ атрибуту passthrough MPEG4SINK Спсппс транзита **значение true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




