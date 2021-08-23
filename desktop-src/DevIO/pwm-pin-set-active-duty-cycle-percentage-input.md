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
ms.openlocfilehash: ca6b2ee6aa4d4d2da3f94aa7cc471de12c1f8040b597edf568bf061c8e392aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758854"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>Закрепление ШИРОТного \_ закрепления. \_ \_ \_ \_ \_ процент \_ входных данных цикла активной пошлины

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

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
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                      |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                             |
| Минимальная версия КМДФ<br/>     | 1,19<br/>                                                                                  |
| Минимальная версия UMDF<br/>     | 2.19<br/>                                                                                  |
| Заголовок<br/>                   | <dl> <dt>Широт. h (включая широту. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**запрос \_ ioctl \_ модулятор \_ Установка \_ активных \_ \_ циклов \_ активности**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




