---
description: '\_ \_ Тип перечисления WPD Flash Modes описывает режим Flash, используемый при записи изображений с устройства.'
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: Перечисление WPD_FLASH_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668683"
---
# <a name="wpd_flash_modes-enumeration"></a><span data-ttu-id="daa3c-103">\_Перечисление Flash- \_ режимов WPD</span><span class="sxs-lookup"><span data-stu-id="daa3c-103">WPD\_FLASH\_MODES enumeration</span></span>

<span data-ttu-id="daa3c-104">Тип **перечисления \_ WPD \_ Flash** Modes описывает режим Flash, используемый при записи изображений с устройства.</span><span class="sxs-lookup"><span data-stu-id="daa3c-104">The **WPD\_FLASH\_MODES** enumeration type describes a flash mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="daa3c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="daa3c-105">Syntax</span></span>


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="daa3c-106">Константы</span><span class="sxs-lookup"><span data-stu-id="daa3c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="daa3c-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_режим Flash-памяти WPD не \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="daa3c-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**WPD\_FLASH\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="daa3c-108">Не указан режим вспышки.</span><span class="sxs-lookup"><span data-stu-id="daa3c-108">No flash mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="daa3c-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**\_Автоматическое вспышка в \_ режиме Flash \_**</span><span class="sxs-lookup"><span data-stu-id="daa3c-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD\_FLASH\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="daa3c-110">Указывает, что Flash следует использовать в автоматическом режиме, как указано устройством.</span><span class="sxs-lookup"><span data-stu-id="daa3c-110">Specifies that the flash should be used in the automatic mode, as specified by the device.</span></span>

</dd> <dt>

<span data-ttu-id="daa3c-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**\_Вспышка Flash- \_ режима \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="daa3c-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD\_FLASH\_MODE\_OFF**</span></span>
</dt> <dd>

<span data-ttu-id="daa3c-112">Указывает, что Flash не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="daa3c-112">Specifies that no flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="daa3c-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**\_ \_ Заливка флеш-режима WPD \_**</span><span class="sxs-lookup"><span data-stu-id="daa3c-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**WPD\_FLASH\_MODE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="daa3c-114">Задает тип заливки Flash.</span><span class="sxs-lookup"><span data-stu-id="daa3c-114">Specifies a fill-type flash.</span></span>

</dd> <dt>

<span data-ttu-id="daa3c-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**\_ \_ \_ \_ Автоматический глаз флеш-режима WPD Flash \_**</span><span class="sxs-lookup"><span data-stu-id="daa3c-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="daa3c-116">Указывает, что следует использовать Flash-память для сокращения красных глаз.</span><span class="sxs-lookup"><span data-stu-id="daa3c-116">Specifies that the red eye reduction flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="daa3c-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_Заливка флэш-памяти WPD с \_ \_ красным \_ глазом \_**</span><span class="sxs-lookup"><span data-stu-id="daa3c-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="daa3c-118">Указывает, что следует использовать вспышку с заливкой красных глаз.</span><span class="sxs-lookup"><span data-stu-id="daa3c-118">Specifies that the red eye fill flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="daa3c-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ \_ Внешняя синхронизация флеш-режима WPD \_**</span><span class="sxs-lookup"><span data-stu-id="daa3c-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**WPD\_FLASH\_MODE\_EXTERNAL\_SYNC**</span></span>
</dt> <dd>

<span data-ttu-id="daa3c-120">Указывает, что Flash должен быть синхронизирован с другими внешними устройствами Flash.</span><span class="sxs-lookup"><span data-stu-id="daa3c-120">Specifies that the flash should be synchronized with other external flash devices.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="daa3c-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="daa3c-121">Remarks</span></span>

<span data-ttu-id="daa3c-122">Это перечисление используется в свойстве [ \_ \_ \_ \_ режима вспышки для изображения WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="daa3c-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_FLASH\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="daa3c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="daa3c-123">Requirements</span></span>



| <span data-ttu-id="daa3c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="daa3c-124">Requirement</span></span> | <span data-ttu-id="daa3c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="daa3c-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="daa3c-126">Header</span><span class="sxs-lookup"><span data-stu-id="daa3c-126">Header</span></span><br/> | <dl> <span data-ttu-id="daa3c-127"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="daa3c-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daa3c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="daa3c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daa3c-129">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="daa3c-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




