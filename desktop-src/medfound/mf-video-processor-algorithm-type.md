---
description: Определяет алгоритмы для обработчика видео, используемого \_ \_ алгоритмом обработчика видео MF \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: Перечисление MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 885c3e9c34fa787a6877fd37eef81f470be395225594b90b2f5516a8e773eb88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244142"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a>\_ \_ \_ Перечисление типов алгоритмов ВИДЕОпроцессора MF \_

Определяет алгоритмы для обработчика видео, используемого [ \_ \_ \_ алгоритмом обработчика видео MF](mf-video-processor-algorithm.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**\_ \_ алгоритм процессора видео \_ MF \_ по умолчанию**
</dt> <dd>

режим по умолчанию подходит к балансу качества и скорости

</dd> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_ \_ Алгоритм видеопроцессора MF \_ \_ МРФ \_ КРФ \_ 444**
</dt> <dd>

Обработчик видео всегда будет внутренне обрабатывать в АЙУВ и использовать фильтры высокого качества.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                              |
| IDL<br/>                      | <dl> <dt>Мфидл. idl</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Перечисления Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




