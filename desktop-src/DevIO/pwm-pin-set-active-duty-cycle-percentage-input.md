---
description: Содержит требуемый процент циклов пошлины для ПИН-кода или канала в контроллере широты импульсов.
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: Структура PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (широт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423202"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>Закрепление ШИРОТного \_ закрепления. \_ \_ \_ \_ \_ процент \_ входных данных цикла активной пошлины

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Содержит требуемый процент циклов пошлины для ПИН-кода или канала в контроллере широты импульсов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Percentage**
</dt> <dd>

Требуемый цикл обработки сигнала ШИРОТы в виде коэффициента ШИРОТы в \_ процентах (улонглонг).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                             |
| Минимальная версия КМДФ<br/>     | 1,19<br/>                                                                                  |
| Минимальная версия UMDF<br/>     | 2.19<br/>                                                                                  |
| Header<br/>                   | <dl> <dt>Широт. h (включая широту. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**запрос \_ ioctl \_ модулятор \_ Установка \_ активных \_ \_ циклов \_ активности**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




