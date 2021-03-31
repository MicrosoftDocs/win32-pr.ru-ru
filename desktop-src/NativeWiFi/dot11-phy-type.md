---
description: Определяет 802,11 PHY и тип носителя.
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
title: Перечисление DOT11_PHY_TYPE (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_PHY_TYPE
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 4e8fc4a1154b9f95fad5024607435861b9e98ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910655"
---
# <a name="dot11_phy_type-enumeration"></a><span data-ttu-id="1b35e-103">\_ \_ Перечисление типа PHY DOT11</span><span class="sxs-lookup"><span data-stu-id="1b35e-103">DOT11\_PHY\_TYPE enumeration</span></span>

<span data-ttu-id="1b35e-104">Перечисление **\_ \_ типа phy DOT11** определяет 802,11 PHY и тип носителя.</span><span class="sxs-lookup"><span data-stu-id="1b35e-104">The **DOT11\_PHY\_TYPE** enumeration defines an 802.11 PHY and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b35e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b35e-105">Syntax</span></span>


```C++
typedef enum _DOT11_PHY_TYPE { 
  dot11_phy_type_unknown     = 0,
  dot11_phy_type_any         = 0,
  dot11_phy_type_fhss        = 1,
  dot11_phy_type_dsss        = 2,
  dot11_phy_type_irbaseband  = 3,
  dot11_phy_type_ofdm        = 4,
  dot11_phy_type_hrdsss      = 5,
  dot11_phy_type_erp         = 6,
  dot11_phy_type_ht          = 7,
  dot11_phy_type_vht         = 8,
  dot11_phy_type_IHV_start   = 0x80000000,
  dot11_phy_type_IHV_end     = 0xffffffff
} DOT11_PHY_TYPE, *PDOT11_PHY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="1b35e-106">Константы</span><span class="sxs-lookup"><span data-stu-id="1b35e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1b35e-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**\_неизвестный \_ тип PHY Dot11 \_**</span><span class="sxs-lookup"><span data-stu-id="1b35e-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11\_phy\_type\_unknown**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-108">Указывает неизвестный или неинициализированный тип PHY.</span><span class="sxs-lookup"><span data-stu-id="1b35e-108">Specifies an unknown or uninitialized PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**\_тип PHY \_ Dot11 \_ ANY**</span><span class="sxs-lookup"><span data-stu-id="1b35e-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11\_phy\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-110">Указывает любой тип PHY.</span><span class="sxs-lookup"><span data-stu-id="1b35e-110">Specifies any PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**\_ \_ фхсс типа PHY \_ Dot11**</span><span class="sxs-lookup"><span data-stu-id="1b35e-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11\_phy\_type\_fhss**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-112">Указывает PHY с частотой прыгающее»-спектр (ФХСС).</span><span class="sxs-lookup"><span data-stu-id="1b35e-112">Specifies a frequency-hopping spread-spectrum (FHSS) PHY.</span></span> <span data-ttu-id="1b35e-113">Устройства Bluetooth могут использовать ФХСС или адаптацию ФХСС.</span><span class="sxs-lookup"><span data-stu-id="1b35e-113">Bluetooth devices can use FHSS or an adaptation of FHSS.</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**\_ \_ технология DSSS типа PHY Dot11 \_**</span><span class="sxs-lookup"><span data-stu-id="1b35e-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11\_phy\_type\_dsss**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-115">Указывает тип PHY для прямого распределения последовательности (DSSS).</span><span class="sxs-lookup"><span data-stu-id="1b35e-115">Specifies a direct sequence spread spectrum (DSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**\_ \_ ирбасебанд типа PHY \_ Dot11**</span><span class="sxs-lookup"><span data-stu-id="1b35e-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11\_phy\_type\_irbaseband**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-117">Задает тип PHY инфракрасной связи (IR) басебанд.</span><span class="sxs-lookup"><span data-stu-id="1b35e-117">Specifies an infrared (IR) baseband PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**\_ \_ офдм типа PHY \_ Dot11**</span><span class="sxs-lookup"><span data-stu-id="1b35e-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11\_phy\_type\_ofdm**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-119">Указывает тип PHY для мультиплексирования деления по частоте (ОФДМ).</span><span class="sxs-lookup"><span data-stu-id="1b35e-119">Specifies an orthogonal frequency division multiplexing (OFDM) PHY type.</span></span> <span data-ttu-id="1b35e-120">802.11. устройства могут использовать ОФДМ.</span><span class="sxs-lookup"><span data-stu-id="1b35e-120">802.11a devices can use OFDM.</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**\_ \_ хрдссс типа PHY \_ Dot11**</span><span class="sxs-lookup"><span data-stu-id="1b35e-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11\_phy\_type\_hrdsss**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-122">Указывает тип PHY с высокой частотой (ХРДССС).</span><span class="sxs-lookup"><span data-stu-id="1b35e-122">Specifies a high-rate DSSS (HRDSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**\_ \_ ERP типа PHY \_ Dot11**</span><span class="sxs-lookup"><span data-stu-id="1b35e-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11\_phy\_type\_erp**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-124">Задает тип PHY с расширенной частотой (ERP).</span><span class="sxs-lookup"><span data-stu-id="1b35e-124">Specifies an extended rate PHY type (ERP).</span></span> <span data-ttu-id="1b35e-125">устройства 802.11 g могут использовать ERP.</span><span class="sxs-lookup"><span data-stu-id="1b35e-125">802.11g devices can use ERP.</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**\_тип PHY Dot11 с \_ типом \_ HT**</span><span class="sxs-lookup"><span data-stu-id="1b35e-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11\_phy\_type\_ht**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-127">Указывает тип PHY n 802.11.</span><span class="sxs-lookup"><span data-stu-id="1b35e-127">Specifies the 802.11n PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**\_ \_ ВХТ типа PHY \_ Dot11**</span><span class="sxs-lookup"><span data-stu-id="1b35e-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11\_phy\_type\_vht**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-129">Указывает тип PHY AC 802.11.</span><span class="sxs-lookup"><span data-stu-id="1b35e-129">Specifies the 802.11ac PHY type.</span></span> <span data-ttu-id="1b35e-130">Это тип PHY высокой пропускной способности, указанный в IEEE 802.11 AC.</span><span class="sxs-lookup"><span data-stu-id="1b35e-130">This is the very high throughput PHY type specified in IEEE 802.11ac.</span></span>

<span data-ttu-id="1b35e-131">Это значение поддерживается в Windows 8.1, Windows Server 2012 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1b35e-131">This value is supported on Windows 8.1, Windows Server 2012 R2, and later.</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**\_ \_ \_ Начало независимого типа PHY Dot11 \_**</span><span class="sxs-lookup"><span data-stu-id="1b35e-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11\_phy\_type\_IHV\_start**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-133">Указывает начало диапазона, который используется для определения типов PHY, разработанных независимым поставщиком оборудования (IHV).</span><span class="sxs-lookup"><span data-stu-id="1b35e-133">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="1b35e-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**\_ \_ \_ конец IHV типа PHY \_ Dot11**</span><span class="sxs-lookup"><span data-stu-id="1b35e-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11\_phy\_type\_IHV\_end**</span></span>
</dt> <dd>

<span data-ttu-id="1b35e-135">Указывает начало диапазона, который используется для определения типов PHY, разработанных независимым поставщиком оборудования (IHV).</span><span class="sxs-lookup"><span data-stu-id="1b35e-135">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b35e-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b35e-136">Remarks</span></span>

<span data-ttu-id="1b35e-137">IHV может назначать значения для собственных типов PHY из **\_ \_ типа PHY \_ \_** на основе Dot11, начиная с **\_ \_ \_ \_ конца типа PHY Dot11**.</span><span class="sxs-lookup"><span data-stu-id="1b35e-137">An IHV can assign a value for its proprietary PHY types from **dot11\_phy\_type\_IHV\_start** through **dot11\_phy\_type\_IHV\_end**.</span></span> <span data-ttu-id="1b35e-138">IHV должен назначить уникальное число из этого диапазона для каждого из собственных типов PHY.</span><span class="sxs-lookup"><span data-stu-id="1b35e-138">The IHV must assign a unique number from this range for each of its proprietary PHY types.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b35e-139">Требования</span><span class="sxs-lookup"><span data-stu-id="1b35e-139">Requirements</span></span>



| <span data-ttu-id="1b35e-140">Требование</span><span class="sxs-lookup"><span data-stu-id="1b35e-140">Requirement</span></span> | <span data-ttu-id="1b35e-141">Значение</span><span class="sxs-lookup"><span data-stu-id="1b35e-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b35e-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b35e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1b35e-143">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1b35e-143">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="1b35e-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b35e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1b35e-145">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b35e-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b35e-146">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1b35e-146">Redistributable</span></span><br/>          | <span data-ttu-id="1b35e-147">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="1b35e-147">Wireless LAN API for Windows XP with SP2</span></span><br/>                                   |
| <span data-ttu-id="1b35e-148">Header</span><span class="sxs-lookup"><span data-stu-id="1b35e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b35e-149"><dt>Windot11. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b35e-149"><dt>Windot11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b35e-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b35e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b35e-151">**\_атрибуты связи \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="1b35e-151">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="1b35e-152">**\_возможности интерфейса \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="1b35e-152">**WLAN\_INTERFACE\_CAPABILITY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




