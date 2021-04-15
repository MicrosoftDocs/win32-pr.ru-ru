---
description: '\_ \_ Тип перечисления «параметры белого баланса» \_ содержит сведения о том, как видеоролики и видеоизображения выводят цветовые каналы для достижения правильного баланса белого.'
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: Перечисление WPD_WHITE_BALANCE_SETTINGS (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648645"
---
# <a name="wpd_white_balance_settings-enumeration"></a><span data-ttu-id="fbef8-103">\_ \_ Перечисление параметров белого баланса WPD \_</span><span class="sxs-lookup"><span data-stu-id="fbef8-103">WPD\_WHITE\_BALANCE\_SETTINGS enumeration</span></span>

<span data-ttu-id="fbef8-104">Тип перечисления « **\_ \_ \_ Параметры белого баланса** » содержит сведения о том, как видеоролики и видеоизображения выводят цветовые каналы для достижения правильного баланса белого.</span><span class="sxs-lookup"><span data-stu-id="fbef8-104">The **WPD\_WHITE\_BALANCE\_SETTINGS** enumeration type describes how a video or image device weights color channels to achieve a proper white balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbef8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbef8-105">Syntax</span></span>


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="fbef8-106">Константы</span><span class="sxs-lookup"><span data-stu-id="fbef8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fbef8-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_неопределенный \_ баланс белого WPD \_**</span><span class="sxs-lookup"><span data-stu-id="fbef8-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD\_WHITE\_BALANCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="fbef8-108">Это значение не было определено.</span><span class="sxs-lookup"><span data-stu-id="fbef8-108">This value has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="fbef8-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**\_ \_ Ручное баланс белого по \_**</span><span class="sxs-lookup"><span data-stu-id="fbef8-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD\_WHITE\_BALANCE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="fbef8-110">Баланс белого задается явным образом с помощью [свойства \_ \_ \_ \_ коэффициента по прежнему RGB-изображения WPD](still-image-properties.md) и не изменяется самим собой.</span><span class="sxs-lookup"><span data-stu-id="fbef8-110">The white balance is set explicitly by using the [WPD\_STILL\_IMAGE\_RGB\_GAIN](still-image-properties.md) property and will not change by itself.</span></span>

</dd> <dt>

<span data-ttu-id="fbef8-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**\_белый баланс белого, \_ \_ Автоматический**</span><span class="sxs-lookup"><span data-stu-id="fbef8-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD\_WHITE\_BALANCE\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="fbef8-112">Устройство будет устанавливать баланс белого цвета.</span><span class="sxs-lookup"><span data-stu-id="fbef8-112">The device will set the white balance.</span></span>

</dd> <dt>

<span data-ttu-id="fbef8-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**\_белый баланс по белого \_ регулятора для \_ \_ \_ автоматической отправки**</span><span class="sxs-lookup"><span data-stu-id="fbef8-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD\_WHITE\_BALANCE\_ONE\_PUSH\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="fbef8-114">Устройство задаст баланс белого, но только когда пользователь отправит кнопку захвата устройства при надежде устройства в белом поле.</span><span class="sxs-lookup"><span data-stu-id="fbef8-114">The device will set the white balance, but only when the user pushes the device's capture button while aiming the device at a white field.</span></span>

</dd> <dt>

<span data-ttu-id="fbef8-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**\_белый \_ баланс на \_ летнее время**</span><span class="sxs-lookup"><span data-stu-id="fbef8-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD\_WHITE\_BALANCE\_DAYLIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="fbef8-116">Устройство будет использовать баланс белого цвета, подходящий для использования в большинстве параметров перехода на летнее время.</span><span class="sxs-lookup"><span data-stu-id="fbef8-116">The device will use white balance numbers appropriate for use in most daylight settings.</span></span>

</dd> <dt>

<span data-ttu-id="fbef8-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**\_тунгстен белого \_ баланса \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="fbef8-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD\_WHITE\_BALANCE\_TUNGSTEN**</span></span>
</dt> <dd>

<span data-ttu-id="fbef8-118">Устройство будет использовать баланс белого цвета, подходящий для использования в большинстве инкандесцент параметров освещения.</span><span class="sxs-lookup"><span data-stu-id="fbef8-118">The device will use white balance numbers appropriate for use in most indoor, incandescent lighting settings.</span></span>

</dd> <dt>

<span data-ttu-id="fbef8-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**\_ \_ вспышка белого баланса WPD \_**</span><span class="sxs-lookup"><span data-stu-id="fbef8-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD\_WHITE\_BALANCE\_FLASH**</span></span>
</dt> <dd>

<span data-ttu-id="fbef8-120">Устройство будет использовать номера белого баланса, которые подходят для использования с Flash.</span><span class="sxs-lookup"><span data-stu-id="fbef8-120">The device will use white balance numbers appropriate for use with a flash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbef8-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fbef8-121">Remarks</span></span>

<span data-ttu-id="fbef8-122">Это перечисление используется свойством " [ \_ неподвижный \_ \_ \_ баланс изображения WPD](still-image-properties.md) ".</span><span class="sxs-lookup"><span data-stu-id="fbef8-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_WHITE\_BALANCE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbef8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fbef8-123">Requirements</span></span>



| <span data-ttu-id="fbef8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fbef8-124">Requirement</span></span> | <span data-ttu-id="fbef8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fbef8-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbef8-126">Header</span><span class="sxs-lookup"><span data-stu-id="fbef8-126">Header</span></span><br/> | <dl> <span data-ttu-id="fbef8-127"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbef8-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbef8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbef8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbef8-129">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="fbef8-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




