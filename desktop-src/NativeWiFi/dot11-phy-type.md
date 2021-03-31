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
# <a name="dot11_phy_type-enumeration"></a>\_ \_ Перечисление типа PHY DOT11

Перечисление **\_ \_ типа phy DOT11** определяет 802,11 PHY и тип носителя.

## <a name="syntax"></a>Синтаксис


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



## <a name="constants"></a>Константы

<dl> <dt>

<span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**\_неизвестный \_ тип PHY Dot11 \_**
</dt> <dd>

Указывает неизвестный или неинициализированный тип PHY.

</dd> <dt>

<span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**\_тип PHY \_ Dot11 \_ ANY**
</dt> <dd>

Указывает любой тип PHY.

</dd> <dt>

<span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**\_ \_ фхсс типа PHY \_ Dot11**
</dt> <dd>

Указывает PHY с частотой прыгающее»-спектр (ФХСС). Устройства Bluetooth могут использовать ФХСС или адаптацию ФХСС.

</dd> <dt>

<span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**\_ \_ технология DSSS типа PHY Dot11 \_**
</dt> <dd>

Указывает тип PHY для прямого распределения последовательности (DSSS).

</dd> <dt>

<span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**\_ \_ ирбасебанд типа PHY \_ Dot11**
</dt> <dd>

Задает тип PHY инфракрасной связи (IR) басебанд.

</dd> <dt>

<span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**\_ \_ офдм типа PHY \_ Dot11**
</dt> <dd>

Указывает тип PHY для мультиплексирования деления по частоте (ОФДМ). 802.11. устройства могут использовать ОФДМ.

</dd> <dt>

<span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**\_ \_ хрдссс типа PHY \_ Dot11**
</dt> <dd>

Указывает тип PHY с высокой частотой (ХРДССС).

</dd> <dt>

<span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**\_ \_ ERP типа PHY \_ Dot11**
</dt> <dd>

Задает тип PHY с расширенной частотой (ERP). устройства 802.11 g могут использовать ERP.

</dd> <dt>

<span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**\_тип PHY Dot11 с \_ типом \_ HT**
</dt> <dd>

Указывает тип PHY n 802.11.

</dd> <dt>

<span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**\_ \_ ВХТ типа PHY \_ Dot11**
</dt> <dd>

Указывает тип PHY AC 802.11. Это тип PHY высокой пропускной способности, указанный в IEEE 802.11 AC.

Это значение поддерживается в Windows 8.1, Windows Server 2012 R2 и более поздних версиях.

</dd> <dt>

<span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**\_ \_ \_ Начало независимого типа PHY Dot11 \_**
</dt> <dd>

Указывает начало диапазона, который используется для определения типов PHY, разработанных независимым поставщиком оборудования (IHV).

</dd> <dt>

<span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**\_ \_ \_ конец IHV типа PHY \_ Dot11**
</dt> <dd>

Указывает начало диапазона, который используется для определения типов PHY, разработанных независимым поставщиком оборудования (IHV).

</dd> </dl>

## <a name="remarks"></a>Комментарии

IHV может назначать значения для собственных типов PHY из **\_ \_ типа PHY \_ \_** на основе Dot11, начиная с **\_ \_ \_ \_ конца типа PHY Dot11**. IHV должен назначить уникальное число из этого диапазона для каждого из собственных типов PHY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Распространяемые компоненты<br/>          | Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                                   |
| Header<br/>                   | <dl> <dt>Windot11. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_атрибуты связи \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**\_возможности интерфейса \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




