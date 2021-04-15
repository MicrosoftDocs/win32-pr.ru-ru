---
description: Перечисление Тапиконтролфлагс используется несколькими методами для указания того, управляется ли данное свойство автоматически, или вручную.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Перечисление Тапиконтролфлагс (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689225"
---
# <a name="tapicontrolflags-enumeration"></a>Перечисление Тапиконтролфлагс

\[ Это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Перечисление **тапиконтролфлагс** используется несколькими методами для указания того, управляется ли данное свойство автоматически, или вручную.

## <a name="syntax"></a>Синтаксис


```C++
} TAPIControlFlags;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**Тапиконтрол \_ без флагов \_**
</dt> <dd>

У TAPI нет управляющих флагов для свойства.

</dd> <dt>

<span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**\_Auto тапиконтрол flags \_**
</dt> <dd>

Свойство управляется автоматически.

</dd> <dt>

<span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**\_Ручные флаги тапиконтрол \_**
</dt> <dd>

Свойство управляется вручную.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ипмсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Итаудиодевицеконтрол:: Range**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**Итаудиодевицеконтрол:: Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**Итаудиодевицеконтрол:: Set**](itaudiodevicecontrol-set.md)
</dt> <dt>

[**Итаудиосеттингс:: Range**](itaudiosettings-getrange.md)
</dt> <dt>

[**Итаудиосеттингс:: Get**](itaudiosettings-get.md)
</dt> <dt>

[**Итаудиосеттингс:: Set**](itaudiosettings-set.md)
</dt> <dt>

[**Иткаллкуалитиконтрол:: Range**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**Иткаллкуалитиконтрол:: Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**Иткаллкуалитиконтрол:: Set**](itcallqualitycontrol-set.md)
</dt> <dt>

[**Итстреамкуалитиконтрол:: Range**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**Итстреамкуалитиконтрол:: Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**Итстреамкуалитиконтрол:: Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




