---
description: '\_ \_ Тип перечисления «исправленные \_ значения состояния WPD» \_ описывает состояние цветовой коррекции изображения или видеофайла.'
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: Перечисление WPD_COLOR_CORRECTED_STATUS_VALUES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718047"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a><span data-ttu-id="7d748-103">\_ \_ \_ Перечисление значений состояния ИСПРАВЛЕНного цвета WPD \_</span><span class="sxs-lookup"><span data-stu-id="7d748-103">WPD\_COLOR\_CORRECTED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="7d748-104">Тип перечисления « **\_ \_ исправленные \_ \_ значения состояния WPD** » описывает состояние цветовой коррекции изображения или видеофайла.</span><span class="sxs-lookup"><span data-stu-id="7d748-104">The **WPD\_COLOR\_CORRECTED\_STATUS\_VALUES** enumeration type describes the color correction status of an image or video file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d748-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d748-105">Syntax</span></span>


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="7d748-106">Константы</span><span class="sxs-lookup"><span data-stu-id="7d748-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7d748-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_ \_ Исправлено цветовое \_ состояние WPD \_ не \_ исправлено**</span><span class="sxs-lookup"><span data-stu-id="7d748-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_NOT\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="7d748-108">Изображение не исправлено цветом.</span><span class="sxs-lookup"><span data-stu-id="7d748-108">The image has not been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="7d748-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**Исправлено \_ \_ состояние исправленного цвета WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d748-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="7d748-110">Изображение исправлено цветом.</span><span class="sxs-lookup"><span data-stu-id="7d748-110">The image has been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="7d748-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**\_ \_ Исправлено цветовое \_ состояние WPD \_ \_ не должно \_ быть \_ исправлено**</span><span class="sxs-lookup"><span data-stu-id="7d748-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_SHOULD\_NOT\_BE\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="7d748-112">Образ не был и не должен быть исправлен цветом.</span><span class="sxs-lookup"><span data-stu-id="7d748-112">The image has not been, and should not be, color corrected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d748-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d748-113">Remarks</span></span>

<span data-ttu-id="7d748-114">Указывает состояние исправленного цвета изображения.</span><span class="sxs-lookup"><span data-stu-id="7d748-114">Indicates the color corrected status of an image.</span></span> <span data-ttu-id="7d748-115">Это перечисление используется свойством " [ \_ \_ \_ исправленное \_ состояние цветового изображения WPD](image-properties.md) ".</span><span class="sxs-lookup"><span data-stu-id="7d748-115">This enumeration is used by the [WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d748-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7d748-116">Requirements</span></span>



| <span data-ttu-id="7d748-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7d748-117">Requirement</span></span> | <span data-ttu-id="7d748-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7d748-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d748-119">Header</span><span class="sxs-lookup"><span data-stu-id="7d748-119">Header</span></span><br/> | <dl> <span data-ttu-id="7d748-120"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d748-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d748-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d748-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d748-122">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="7d748-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




