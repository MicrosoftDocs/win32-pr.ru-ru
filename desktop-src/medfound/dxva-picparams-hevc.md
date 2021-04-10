---
description: Предоставляет параметры уровня изображения сжатого изображения для HEVCного декодирования видео.
ms.assetid: F73AE9CD-5BBC-4A9F-8D05-707AD5E2E92A
title: Структура DXVA_PicParams_HEVC (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicParams_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: cafcbf31a7d4b7fee84e6c695f1d0f0a1e0302ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143123"
---
# <a name="dxva_picparams_hevc-structure"></a>\_ \_ Структура HEVC пикпарамс дксва

Предоставляет параметры уровня изображения сжатого изображения для HEVCного декодирования видео.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DXVA_PicParams_HEVC {
  USHORT             PicWidthInMinCbsY;
  USHORT             PicHeightInMinCbsY;
  union {
    struct {
      USHORT chroma_format_idc  :2;
      USHORT separate_colour_plane_flag   :1;
      USHORT bit_depth_luma_minus8   :3;
      USHORT bit_depth_chroma_minus8  :3;
      USHORT log2_max_pic_order_cnt_lsb_minus4  :4;
      USHORT NoPicReorderingFlag   :1;
      USHORT  NoBiPredFlag   :1;
      USHORT ReservedBits1     :1;
    };
    USHORT  wFormatAndSequenceInfoFlags;
  };
  DXVA_PicEntry_HEVC CurrPic;
  UCHAR              sps_max_dec_pic_buffering_minus1;
  UCHAR              log2_min_luma_coding_block_size_minus3;
  UCHAR              log2_diff_max_min_luma_coding_block_size;
  UCHAR              log2_min_transform_block_size_minus2;
  UCHAR              log2_diff_max_min_transform_block_size;
  UCHAR              max_transform_hierarchy_depth_inter;
  UCHAR              max_transform_hierarchy_depth_intra;
  UCHAR              num_short_term_ref_pic_sets;
  UCHAR              num_long_term_ref_pics_sps;
  UCHAR              num_ref_idx_l0_default_active_minus1;
  UCHAR              num_ref_idx_l1_default_active_minus1;
  CHAR               init_qp_minus26;
  UCHAR              ucNumDeltaPocsOfRefRpsIdx;
  USHORT             wNumBitsForShortTermRPSInSlice;
  USHORT             ReservedBits2;
  union {
    struct {
      UINT32 scaling_list_enabled_flag  :1;
      UINT32 amp_enabled_flag  :1;
      UINT32 sample_adaptive_offset_enabled_flag  :1;
      UINT32 pcm_enabled_flag   :1;
      UINT32 pcm_sample_bit_depth_luma_minus1   :4;
      UINT32 pcm_sample_bit_depth_chroma_minus1     :4;
      UINT32 log2_min_pcm_luma_coding_block_size_minus3    :2;
      UINT32 log2_diff_max_min_pcm_luma_coding_block_size  :2;
      UINT32 pcm_loop_filter_disabled_flag  :1;
      UINT32 long_term_ref_pics_present_flag   :1;
      UINT32 sps_temporal_mvp_enabled_flag  :1;
      UINT32 strong_intra_smoothing_enabled_flag   :1;
      UINT32 dependent_slice_segments_enabled_flag    :1;
      UINT32 output_flag_present_flag   :1;
      UINT32 num_extra_slice_header_bits    :3;
      UINT32 sign_data_hiding_enabled_flag  :1;
      UINT32 cabac_init_present_flag  :1;
      UINT32 ReservedBits3    :5;
    };
    UINT32             dwCodingParamToolFlags;
    union {
      struct {
        UINT32 constrained_intra_pred_flag  :1;
        UINT32 transform_skip_enabled_flag  :1;
        UINT32 cu_qp_delta_enabled_flag  :1;
        UINT32 pps_slice_chroma_qp_offsets_present_flag  :1;
        UINT32 weighted_pred_flag  :1;
        UINT32 weighted_bipred_flag  :1;
        UINT32 transquant_bypass_enabled_flag  :1;
        UINT32 tiles_enabled_flag   :1;
        UINT32 entropy_coding_sync_enabled_flag   :1;
        UINT32 uniform_spacing_flag    :1;
        UINT32 loop_filter_across_tiles_enabled_flag   :1;
        UINT32 pps_loop_filter_across_slices_enabled_flag  :1;
        UINT32 deblocking_filter_override_enabled_flag  :1;
        UINT32 pps_deblocking_filter_disabled_flag  :1;
        UINT32 lists_modification_present_flag  :1;
        UINT32 slice_segment_header_extension_present_flag  :1;
        UINT32 IrapPicFlag  :1;
        UINT32 IdrPicFlag     :1;
        UINT32 IntraPicFlag   :1;
        UINT32 ReservedBits4     :13;
      };
      UINT32   dwCodingSettingPicturePropertyFlags;
    };
    CHAR               pps_cb_qp_offset;
    CHAR               pps_cr_qp_offset;
    UCHAR              num_tile_columns_minus1;
    UCHAR              num_tile_rows_minus1;
    USHORT             column_width_minus1[19];
    USHORT             row_height_minus1[21];
    UCHAR              diff_cu_qp_delta_depth;
    CHAR               pps_beta_offset_div2;
    CHAR               pps_tc_offset_div2;
    UCHAR              log2_parallel_merge_level_minus2;
    INT                CurrPicOrderCntVal;
    DXVA_PicEntry_HEVC RefPicList[15];
    UCHAR              ReservedBits5;
    INT                PicOrderCntValList[15];
    UCHAR              RefPicSetStCurrBefore[8];
    UCHAR              RefPicSetStCurrAfter[8];
    UCHAR              RefPicSetLtCurr[8];
    USHORT             ReservedBits6;
    USHORT             ReservedBits7;
    UINT               StatusReportFeedbackNumber;
  };
} DXVA_PicParams_HEVC, *PDXVA_PicParams_HEVC;
```



## <a name="members"></a>Члены

<dl> <dt>

**пиквидсинминкбси**
</dt> <dd></dd> <dt>

**пичеигхтинминкбси**
</dt> <dd></dd> <dt>

**\_Формат чрома \_ IDC**
</dt> <dd></dd> <dt>

**отдельный \_ флаг цветовой \_ плоскости \_** 
</dt> <dd></dd> <dt>

**Битовая \_ глубина \_ яркости \_ minus8** 
</dt> <dd></dd> <dt>

**Битовая \_ глубина \_ чрома \_ minus8**
</dt> <dd></dd> <dt>

**log2 \_ Max \_ PIC \_ Order \_ CNT \_ ЛСБ \_ minus4**
</dt> <dd></dd> <dt>

**нопикреордерингфлаг** 
</dt> <dd></dd> <dt>

 **нобипредфлаг** 
</dt> <dd></dd> <dt>

**ReservedBits1** 
</dt> <dd></dd> <dt>

**вформатандсекуенцеинфофлагс**
</dt> <dd></dd> <dt>

**куррпик**
</dt> <dd></dd> <dt>

**\_Максимальное количество \_ \_ \_ буферизованных \_ minus1 в SP Dec PIC**
</dt> <dd></dd> <dt>

**log2 \_ min \_ яркости \_ \_ Размер блока \_ кода \_ minus3**
</dt> <dd></dd> <dt>

**log2 \_ diff \_ Max \_ min \_ яркости \_ \_ Размер блока \_ кодирования**
</dt> <dd></dd> <dt>

**log2 \_ Минимальный \_ \_ Размер блока \_ преобразования \_ minus2**
</dt> <dd></dd> <dt>

**log2 \_ diff \_ Max \_ Минимальный \_ \_ Размер блока \_ преобразования**
</dt> <dd></dd> <dt>

**число \_ \_ внутрихолдинговых иерархий преобразований \_ \_**
</dt> <dd></dd> <dt>

**Максимальная \_ Глубина иерархии преобразований в \_ \_ \_ пределах**
</dt> <dd></dd> <dt>

**число \_ простых краткосрочных \_ \_ \_ \_ наборов PIC**
</dt> <dd></dd> <dt>

**\_SP с \_ \_ ключевыми \_ словами \_ num Long**
</dt> <dd></dd> <dt>

**NUM \_ ref \_ idx \_ \_ minus1 по умолчанию на уровне 0 \_ \_**
</dt> <dd></dd> <dt>

**NUM \_ ref \_ idx \_ L1 \_ Default \_ Active \_ minus1**
</dt> <dd></dd> <dt>

**init \_ QP \_ minus26**
</dt> <dd></dd> <dt>

**укнумделтапоксофрефрпсидкс**
</dt> <dd></dd> <dt>

**внумбитсфоршорттермрпсинслице**
</dt> <dd></dd> <dt>

**ReservedBits2**
</dt> <dd></dd> <dt>

**\_ \_ флаг включения списка \_ масштабирования**
</dt> <dd></dd> <dt>

**\_флаг включения \_ amp**
</dt> <dd></dd> <dt>

**Пример \_ \_ \_ флага включения адаптивного смещения \_**
</dt> <dd></dd> <dt>

**\_флаг включения \_ PCM** 
</dt> <dd></dd> <dt>

**\_ \_ Битовая глубина примера \_ PCM \_ яркости \_ minus1** 
</dt> <dd></dd> <dt>

**\_ \_ Битовая глубина примера \_ PCM \_ чрома \_ minus1** 
</dt> <dd></dd> <dt>

**log2 \_ Минимальный \_ \_ \_ \_ Размер блока кода яркости \_ PCM \_ minus3** 
</dt> <dd></dd> <dt>

**\_ \_ \_ \_ \_ \_ \_ Размер блока кодирования \_ log2 для инструмента сравнения с минимальным числом яркости PCM**
</dt> <dd></dd> <dt>

**\_ \_ \_ флаг отключения фильтра цикла \_ PCM**
</dt> <dd></dd> <dt>

**\_ \_ \_ \_ флаг присутствия терминов "долгосрочные ссылки" \_** 
</dt> <dd></dd> <dt>

**флаг "темпоральный" для \_ темпоральной \_ \_ поддержки MVP \_**
</dt> <dd></dd> <dt>

**strong \_ \_ \_ флаг включения сглаживания \_** 
</dt> <dd></dd> <dt>

**\_ \_ \_ флаг включения зависимых сегментов среза \_** 
</dt> <dd></dd> <dt>

**\_ \_ флаг отображения флага вывода \_** 
</dt> <dd></dd> <dt>

**число \_ \_ бит дополнительного \_ заголовка среза \_** 
</dt> <dd></dd> <dt>

**\_ \_ флаг включения скрытия данных \_ подписывания \_**
</dt> <dd></dd> <dt>

**\_ \_ флаг присутствия Кабак \_ init**
</dt> <dd></dd> <dt>

**ReservedBits3** 
</dt> <dd></dd> <dt>

**двкодингпарамтулфлагс**
</dt> <dd></dd> <dt>

**ограниченный \_ флаг " \_ пред \_ "**
</dt> <dd></dd> <dt>

**\_ \_ флаг включения и выключения преобразования \_**
</dt> <dd></dd> <dt>

**\_флаг изменения \_ \_ разрешения Cu \_ QP**
</dt> <dd></dd> <dt>

**\_ \_ \_ \_ \_ \_ флаг представления "срезы чрома QP" в PPS**
</dt> <dd></dd> <dt>

**Флаг взвешенного \_ ПРЕДА \_**
</dt> <dd></dd> <dt>

**Флаг взвешенного \_ бипред \_**
</dt> <dd></dd> <dt>

**\_ \_ флаг включения обхода \_ транскуант**
</dt> <dd></dd> <dt>

**\_флаг с поддержкой плиток \_** 
</dt> <dd></dd> <dt>

**\_ \_ \_ флаг включения синхронизации кода энтропии \_** 
</dt> <dd></dd> <dt>

**\_флаг единого промежутка \_** 
</dt> <dd></dd> <dt>

**\_Фильтр цикла \_ по \_ \_ флагу включенных плиток \_** 
</dt> <dd></dd> <dt>

**\_флаг " \_ Фильтр цикла PPS \_ по нескольким \_ срезам" \_ \_**
</dt> <dd></dd> <dt>

**Деблокировка \_ \_ \_ флага включения переопределения \_ фильтра**
</dt> <dd></dd> <dt>

**\_ \_ \_ флаг отключения фильтра деблокировки PPS \_**
</dt> <dd></dd> <dt>

**\_ \_ флаг представления "список изменений" \_**
</dt> <dd></dd> <dt>

**\_ \_ \_ \_ флаг присутствия расширения заголовка сегмента среза \_**
</dt> <dd></dd> <dt>

**ираппикфлаг**
</dt> <dd></dd> <dt>

**идрпикфлаг** 
</dt> <dd></dd> <dt>

**интрапикфлаг** 
</dt> <dd></dd> <dt>

**ReservedBits4** 
</dt> <dd></dd> <dt>

**двкодингсеттингпиктурепропертифлагс**
</dt> <dd></dd> <dt>

**\_ \_ смещение QP для PPS CB \_**
</dt> <dd></dd> <dt>

**\_ \_ смещение неqp в PPS \_**
</dt> <dd></dd> <dt>

**число \_ \_ столбцов плитки \_ minus1**
</dt> <dd></dd> <dt>

**число \_ строк мозаики \_ \_ minus1**
</dt> <dd></dd> <dt>

**\_Ширина столбца \_ minus1**
</dt> <dd></dd> <dt>

**\_Высота строки \_ minus1**
</dt> <dd></dd> <dt>

**\_ \_ \_ разностная глубина Cu \_ QP**
</dt> <dd></dd> <dt>

**\_возмещение бета-версии PPS \_ \_ div2**
</dt> <dd></dd> <dt>

**\_ \_ div2 смещение PPS \_ TC**
</dt> <dd></dd> <dt>

**log2 \_ параллельный \_ \_ уровень слияния \_ minus2**
</dt> <dd></dd> <dt>

**куррпикордеркнтвал**
</dt> <dd></dd> <dt>

**рефпиклист**
</dt> <dd></dd> <dt>

**ReservedBits5**
</dt> <dd></dd> <dt>

**пикордеркнтваллист**
</dt> <dd></dd> <dt>

**рефпиксетсткуррбефоре**
</dt> <dd></dd> <dt>

**рефпиксетсткуррафтер**
</dt> <dd></dd> <dt>

**рефпиксетлткурр**
</dt> <dd></dd> <dt>

**ReservedBits6**
</dt> <dd></dd> <dt>

**ReservedBits7**
</dt> <dd></dd> <dt>

**статусрепортфидбаккнумбер**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                           |
| Header<br/>                   | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




