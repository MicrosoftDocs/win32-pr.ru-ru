---
description: Перечисление Тапиконтролфлагс используется несколькими методами для указания того, управляется ли данное свойство автоматически, или вручную.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Перечисление Тапиконтролфлагс (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278cc2328335409d4ffcc95ea136826d121acd57776f98aaad947c8fb9ee5d93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139807"
---
# <a name="tapicontrolflags-enumeration"></a>Перечисление Тапиконтролфлагс

\[это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

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
| Заголовок<br/>       | <dl> <dt>Ипмсп. h</dt> </dl> |



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

 

 




