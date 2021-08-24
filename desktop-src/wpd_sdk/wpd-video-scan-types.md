---
description: '\_ \_ Тип перечисления WPD Video Scan \_ types описывает, как кодируются поля в файле видео.'
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: Перечисление WPD_VIDEO_SCAN_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5f2c6f8a5707780bae6c8a135e3ca940fb4a77408c3df835b321b5b190644fcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703724"
---
# <a name="wpd_video_scan_types-enumeration"></a>\_ \_ Перечисление типов сканирования видеороликов WPD \_

Тип перечисления **WPD \_ Video \_ Scan \_** Types описывает, как кодируются поля в файле видео.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_Тип сканирования видеороликов WPD не \_ \_ \_ используется**
</dt> <dd>

Тип сканирования не определен для этого видеофайла или неприменим.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**\_Тип сканирования видеороликов WPD \_ \_ \_ прогрессивный**
</dt> <dd>

Видеофайл последовательной проверки.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**\_ \_ тип проверки видео WPD поле с \_ \_ \_ чередованием \_ сверху \_**
</dt> <dd>

Сначала выводится файл с чередованием, в котором находятся альтернативные поля и верхнее поле (со строкой 1). Дополнительные сведения см. в разделе "Замечания".

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**\_поле "тип сканирования видеороликов" (WPD) с \_ \_ \_ \_ чередованием \_ снизу \_**
</dt> <dd>

Сначала выводится файл с чередованием, в котором находятся альтернативные поля и нижнее поле (со строкой 2). Дополнительные сведения см. в разделе Примечания.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**\_Тип сканирования видеороликов WPD \_ \_ \_ \_ \_ первое поле сверху \_**
</dt> <dd>

Видеофайл с чередованием, в котором поля отправляются как смежные примеры, а верхнее поле (строка 1) рисуется первыми. Дополнительные сведения см. в разделе Примечания.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**\_ \_ поле типа сканирования видеороликов WPD \_ \_ \_ \_ \_ сначала**
</dt> <dd>

Видеофайл с чередованием, в котором поля отправляются как смежные примеры, а в первую очередь отправляется нижнее поле (строка 2).

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**\_тип проверки видео WPD — \_ \_ \_ смешанная \_ развертка**
</dt> <dd>

Видеофайл с смесью режимов чередования.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**\_Тип сканирования видеороликов WPD \_ \_ \_ смешанные \_ \_ и \_ прогрессивные развертки**
</dt> <dd>

Видеофайл с сочетанием чередующихся и прогрессивных режимов.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это перечисление используется свойством " [ \_ \_ \_ тип видеосканирования WPD](properties-and-attributes.md) ".

Существует два типа файлов с чередованием, которые задаются этим перечислением. **WPD \_ \_Поле типа СКАНИРОВАНИЯ видео с \_ \_ \_ чередованием** относится к формату файла, в котором кадры доставляются по мере того, как они были проверены, а данные помещаются построчно, как показано ниже:

**Кадр 1**

Поле 1. строка 1

Поле 2. строка 1

Поле 1. строка 2

Поле 2. строка 2

Поле 1. строка 3

Поле 2. строка 3

...

**WPD \_ \_ \_ Поле типа сканирования \_ видео \_ Single** ссылается на формат файла, где каждое поле хранится в одном блоке строк сканирования, а поля хранятся последовательно, как показано ниже:

**Кадр 1**

Поле 1. строка 1

Поле 1. строка 2

Поле 1. строка 3

...

За которым следует

Поле 2. строка 1

Поле 2. строка 2

Поле 2. строка 3

...

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




