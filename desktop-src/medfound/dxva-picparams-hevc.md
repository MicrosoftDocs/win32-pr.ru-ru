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
# <a name="dxva_picparams_hevc-structure"></a><span data-ttu-id="06d04-103">\_ \_ Структура HEVC пикпарамс дксва</span><span class="sxs-lookup"><span data-stu-id="06d04-103">DXVA\_PicParams\_HEVC structure</span></span>

<span data-ttu-id="06d04-104">Предоставляет параметры уровня изображения сжатого изображения для HEVCного декодирования видео.</span><span class="sxs-lookup"><span data-stu-id="06d04-104">Provides the picture-level parameters of a compressed picture for HEVC video decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="06d04-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06d04-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="06d04-106">Члены</span><span class="sxs-lookup"><span data-stu-id="06d04-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="06d04-107">**пиквидсинминкбси**</span><span class="sxs-lookup"><span data-stu-id="06d04-107">**PicWidthInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-108">**пичеигхтинминкбси**</span><span class="sxs-lookup"><span data-stu-id="06d04-108">**PicHeightInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-109">**\_Формат чрома \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="06d04-109">**chroma\_format\_idc**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-110">**отдельный \_ флаг цветовой \_ плоскости \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-110">**separate\_colour\_plane\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-111">**Битовая \_ глубина \_ яркости \_ minus8**</span><span class="sxs-lookup"><span data-stu-id="06d04-111">**bit\_depth\_luma\_minus8**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-112">**Битовая \_ глубина \_ чрома \_ minus8**</span><span class="sxs-lookup"><span data-stu-id="06d04-112">**bit\_depth\_chroma\_minus8**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-113">**log2 \_ Max \_ PIC \_ Order \_ CNT \_ ЛСБ \_ minus4**</span><span class="sxs-lookup"><span data-stu-id="06d04-113">**log2\_max\_pic\_order\_cnt\_lsb\_minus4**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-114">**нопикреордерингфлаг**</span><span class="sxs-lookup"><span data-stu-id="06d04-114">**NoPicReorderingFlag**</span></span> 
</dt> <dd></dd> <dt>

 <span data-ttu-id="06d04-115">**нобипредфлаг**</span><span class="sxs-lookup"><span data-stu-id="06d04-115">**NoBiPredFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-116">**ReservedBits1**</span><span class="sxs-lookup"><span data-stu-id="06d04-116">**ReservedBits1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-117">**вформатандсекуенцеинфофлагс**</span><span class="sxs-lookup"><span data-stu-id="06d04-117">**wFormatAndSequenceInfoFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-118">**куррпик**</span><span class="sxs-lookup"><span data-stu-id="06d04-118">**CurrPic**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-119">**\_Максимальное количество \_ \_ \_ буферизованных \_ minus1 в SP Dec PIC**</span><span class="sxs-lookup"><span data-stu-id="06d04-119">**sps\_max\_dec\_pic\_buffering\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-120">**log2 \_ min \_ яркости \_ \_ Размер блока \_ кода \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="06d04-120">**log2\_min\_luma\_coding\_block\_size\_minus3**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-121">**log2 \_ diff \_ Max \_ min \_ яркости \_ \_ Размер блока \_ кодирования**</span><span class="sxs-lookup"><span data-stu-id="06d04-121">**log2\_diff\_max\_min\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-122">**log2 \_ Минимальный \_ \_ Размер блока \_ преобразования \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="06d04-122">**log2\_min\_transform\_block\_size\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-123">**log2 \_ diff \_ Max \_ Минимальный \_ \_ Размер блока \_ преобразования**</span><span class="sxs-lookup"><span data-stu-id="06d04-123">**log2\_diff\_max\_min\_transform\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-124">**число \_ \_ внутрихолдинговых иерархий преобразований \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-124">**max\_transform\_hierarchy\_depth\_inter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-125">**Максимальная \_ Глубина иерархии преобразований в \_ \_ \_ пределах**</span><span class="sxs-lookup"><span data-stu-id="06d04-125">**max\_transform\_hierarchy\_depth\_intra**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-126">**число \_ простых краткосрочных \_ \_ \_ \_ наборов PIC**</span><span class="sxs-lookup"><span data-stu-id="06d04-126">**num\_short\_term\_ref\_pic\_sets**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-127">**\_SP с \_ \_ ключевыми \_ словами \_ num Long**</span><span class="sxs-lookup"><span data-stu-id="06d04-127">**num\_long\_term\_ref\_pics\_sps**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-128">**NUM \_ ref \_ idx \_ \_ minus1 по умолчанию на уровне 0 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-128">**num\_ref\_idx\_l0\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-129">**NUM \_ ref \_ idx \_ L1 \_ Default \_ Active \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="06d04-129">**num\_ref\_idx\_l1\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-130">**init \_ QP \_ minus26**</span><span class="sxs-lookup"><span data-stu-id="06d04-130">**init\_qp\_minus26**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-131">**укнумделтапоксофрефрпсидкс**</span><span class="sxs-lookup"><span data-stu-id="06d04-131">**ucNumDeltaPocsOfRefRpsIdx**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-132">**внумбитсфоршорттермрпсинслице**</span><span class="sxs-lookup"><span data-stu-id="06d04-132">**wNumBitsForShortTermRPSInSlice**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-133">**ReservedBits2**</span><span class="sxs-lookup"><span data-stu-id="06d04-133">**ReservedBits2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-134">**\_ \_ флаг включения списка \_ масштабирования**</span><span class="sxs-lookup"><span data-stu-id="06d04-134">**scaling\_list\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-135">**\_флаг включения \_ amp**</span><span class="sxs-lookup"><span data-stu-id="06d04-135">**amp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-136">**Пример \_ \_ \_ флага включения адаптивного смещения \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-136">**sample\_adaptive\_offset\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-137">**\_флаг включения \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="06d04-137">**pcm\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-138">**\_ \_ Битовая глубина примера \_ PCM \_ яркости \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="06d04-138">**pcm\_sample\_bit\_depth\_luma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-139">**\_ \_ Битовая глубина примера \_ PCM \_ чрома \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="06d04-139">**pcm\_sample\_bit\_depth\_chroma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-140">**log2 \_ Минимальный \_ \_ \_ \_ Размер блока кода яркости \_ PCM \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="06d04-140">**log2\_min\_pcm\_luma\_coding\_block\_size\_minus3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-141">**\_ \_ \_ \_ \_ \_ \_ Размер блока кодирования \_ log2 для инструмента сравнения с минимальным числом яркости PCM**</span><span class="sxs-lookup"><span data-stu-id="06d04-141">**log2\_diff\_max\_min\_pcm\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-142">**\_ \_ \_ флаг отключения фильтра цикла \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="06d04-142">**pcm\_loop\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-143">**\_ \_ \_ \_ флаг присутствия терминов "долгосрочные ссылки" \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-143">**long\_term\_ref\_pics\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-144">**флаг "темпоральный" для \_ темпоральной \_ \_ поддержки MVP \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-144">**sps\_temporal\_mvp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-145">**strong \_ \_ \_ флаг включения сглаживания \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-145">**strong\_intra\_smoothing\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-146">**\_ \_ \_ флаг включения зависимых сегментов среза \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-146">**dependent\_slice\_segments\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-147">**\_ \_ флаг отображения флага вывода \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-147">**output\_flag\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-148">**число \_ \_ бит дополнительного \_ заголовка среза \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-148">**num\_extra\_slice\_header\_bits**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-149">**\_ \_ флаг включения скрытия данных \_ подписывания \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-149">**sign\_data\_hiding\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-150">**\_ \_ флаг присутствия Кабак \_ init**</span><span class="sxs-lookup"><span data-stu-id="06d04-150">**cabac\_init\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-151">**ReservedBits3**</span><span class="sxs-lookup"><span data-stu-id="06d04-151">**ReservedBits3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-152">**двкодингпарамтулфлагс**</span><span class="sxs-lookup"><span data-stu-id="06d04-152">**dwCodingParamToolFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-153">**ограниченный \_ флаг " \_ пред \_ "**</span><span class="sxs-lookup"><span data-stu-id="06d04-153">**constrained\_intra\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-154">**\_ \_ флаг включения и выключения преобразования \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-154">**transform\_skip\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-155">**\_флаг изменения \_ \_ разрешения Cu \_ QP**</span><span class="sxs-lookup"><span data-stu-id="06d04-155">**cu\_qp\_delta\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-156">**\_ \_ \_ \_ \_ \_ флаг представления "срезы чрома QP" в PPS**</span><span class="sxs-lookup"><span data-stu-id="06d04-156">**pps\_slice\_chroma\_qp\_offsets\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-157">**Флаг взвешенного \_ ПРЕДА \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-157">**weighted\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-158">**Флаг взвешенного \_ бипред \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-158">**weighted\_bipred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-159">**\_ \_ флаг включения обхода \_ транскуант**</span><span class="sxs-lookup"><span data-stu-id="06d04-159">**transquant\_bypass\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-160">**\_флаг с поддержкой плиток \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-160">**tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-161">**\_ \_ \_ флаг включения синхронизации кода энтропии \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-161">**entropy\_coding\_sync\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-162">**\_флаг единого промежутка \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-162">**uniform\_spacing\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-163">**\_Фильтр цикла \_ по \_ \_ флагу включенных плиток \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-163">**loop\_filter\_across\_tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-164">**\_флаг " \_ Фильтр цикла PPS \_ по нескольким \_ срезам" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-164">**pps\_loop\_filter\_across\_slices\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-165">**Деблокировка \_ \_ \_ флага включения переопределения \_ фильтра**</span><span class="sxs-lookup"><span data-stu-id="06d04-165">**deblocking\_filter\_override\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-166">**\_ \_ \_ флаг отключения фильтра деблокировки PPS \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-166">**pps\_deblocking\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-167">**\_ \_ флаг представления "список изменений" \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-167">**lists\_modification\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-168">**\_ \_ \_ \_ флаг присутствия расширения заголовка сегмента среза \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-168">**slice\_segment\_header\_extension\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-169">**ираппикфлаг**</span><span class="sxs-lookup"><span data-stu-id="06d04-169">**IrapPicFlag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-170">**идрпикфлаг**</span><span class="sxs-lookup"><span data-stu-id="06d04-170">**IdrPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-171">**интрапикфлаг**</span><span class="sxs-lookup"><span data-stu-id="06d04-171">**IntraPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-172">**ReservedBits4**</span><span class="sxs-lookup"><span data-stu-id="06d04-172">**ReservedBits4**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-173">**двкодингсеттингпиктурепропертифлагс**</span><span class="sxs-lookup"><span data-stu-id="06d04-173">**dwCodingSettingPicturePropertyFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-174">**\_ \_ смещение QP для PPS CB \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-174">**pps\_cb\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-175">**\_ \_ смещение неqp в PPS \_**</span><span class="sxs-lookup"><span data-stu-id="06d04-175">**pps\_cr\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-176">**число \_ \_ столбцов плитки \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="06d04-176">**num\_tile\_columns\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-177">**число \_ строк мозаики \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="06d04-177">**num\_tile\_rows\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-178">**\_Ширина столбца \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="06d04-178">**column\_width\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-179">**\_Высота строки \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="06d04-179">**row\_height\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-180">**\_ \_ \_ разностная глубина Cu \_ QP**</span><span class="sxs-lookup"><span data-stu-id="06d04-180">**diff\_cu\_qp\_delta\_depth**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-181">**\_возмещение бета-версии PPS \_ \_ div2**</span><span class="sxs-lookup"><span data-stu-id="06d04-181">**pps\_beta\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-182">**\_ \_ div2 смещение PPS \_ TC**</span><span class="sxs-lookup"><span data-stu-id="06d04-182">**pps\_tc\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-183">**log2 \_ параллельный \_ \_ уровень слияния \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="06d04-183">**log2\_parallel\_merge\_level\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-184">**куррпикордеркнтвал**</span><span class="sxs-lookup"><span data-stu-id="06d04-184">**CurrPicOrderCntVal**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-185">**рефпиклист**</span><span class="sxs-lookup"><span data-stu-id="06d04-185">**RefPicList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-186">**ReservedBits5**</span><span class="sxs-lookup"><span data-stu-id="06d04-186">**ReservedBits5**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-187">**пикордеркнтваллист**</span><span class="sxs-lookup"><span data-stu-id="06d04-187">**PicOrderCntValList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-188">**рефпиксетсткуррбефоре**</span><span class="sxs-lookup"><span data-stu-id="06d04-188">**RefPicSetStCurrBefore**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-189">**рефпиксетсткуррафтер**</span><span class="sxs-lookup"><span data-stu-id="06d04-189">**RefPicSetStCurrAfter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-190">**рефпиксетлткурр**</span><span class="sxs-lookup"><span data-stu-id="06d04-190">**RefPicSetLtCurr**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-191">**ReservedBits6**</span><span class="sxs-lookup"><span data-stu-id="06d04-191">**ReservedBits6**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-192">**ReservedBits7**</span><span class="sxs-lookup"><span data-stu-id="06d04-192">**ReservedBits7**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="06d04-193">**статусрепортфидбаккнумбер**</span><span class="sxs-lookup"><span data-stu-id="06d04-193">**StatusReportFeedbackNumber**</span></span>
<span data-ttu-id="06d04-194"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="06d04-194"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="06d04-195">Требования</span><span class="sxs-lookup"><span data-stu-id="06d04-195">Requirements</span></span>



| <span data-ttu-id="06d04-196">Требование</span><span class="sxs-lookup"><span data-stu-id="06d04-196">Requirement</span></span> | <span data-ttu-id="06d04-197">Значение</span><span class="sxs-lookup"><span data-stu-id="06d04-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="06d04-198">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06d04-198">Minimum supported client</span></span><br/> | <span data-ttu-id="06d04-199">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="06d04-199">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="06d04-200">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06d04-200">Minimum supported server</span></span><br/> | <span data-ttu-id="06d04-201">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="06d04-201">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="06d04-202">Header</span><span class="sxs-lookup"><span data-stu-id="06d04-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="06d04-203"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="06d04-203"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06d04-204">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06d04-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06d04-205">Структуры Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06d04-205">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




