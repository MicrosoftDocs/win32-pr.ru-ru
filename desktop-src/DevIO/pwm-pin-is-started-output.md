---
description: Содержит текущее состояние создания сигнала для ПИН-кода.
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: Структура PWM_PIN_IS_STARTED_OUTPUT (широт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 448b38e66b7cfb4bf7e24c5d3b7658d0e38ccb8a5ca8c95e1155129737087c68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076188"
---
# <a name="pwm_pin_is_started_output-structure"></a>Закрепление ШИРОТного \_ закрепления \_ \_ начинает \_ выходную структуру

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Содержит текущее состояние создания сигнала для ПИН-кода.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a>Члены

<dl> <dt>

**С начала**
</dt> <dd>

Закрепление текущего состояния создания сигнала. Значение true означает, что ПИН-код запущен. Значение false означает, что ПИН-код остановлен.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                      |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                             |
| Минимальная версия КМДФ<br/>     | 1,19<br/>                                                                                  |
| Минимальная версия UMDF<br/>     | 2.19<br/>                                                                                  |
| Заголовок<br/>                   | <dl> <dt>Широт. h (включая широту. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ПИН-код модуляторного запроса IOCTL \_ \_ \_ запущен**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




