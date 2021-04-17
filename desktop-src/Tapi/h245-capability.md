---
description: '\_Перечисление возможностей H245 описывает поддержку формата аудио и видео.'
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: Перечисление H245_CAPABILITY (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689376"
---
# <a name="h245_capability-enumeration"></a>\_Перечисление возможностей H245

\[**H245 \_ ВОЗМОЖНОСТЬ** недоступна для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Перечисление **\_ возможностей H245** описывает поддержку формата аудио и видео.

## <a name="syntax"></a>Синтаксис


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="HC_G711"></span><span id="hc_g711"></span>**HC \_ G711**
</dt> <dd>

Поддерживается звуковой протокол G. 711.

</dd> <dt>

<span id="HC_G723"></span><span id="hc_g723"></span>**HC \_ G723**
</dt> <dd>

Поддерживается звуковой протокол G. 723.

</dd> <dt>

<span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC \_ H263QCIF**
</dt> <dd>

Поддерживается протокол видео H. 263.

</dd> <dt>

<span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC \_ H261QCIF**
</dt> <dd>

Поддерживается протокол видео H. 263.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|---------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IH323LineEx:: Сетдефаулткапабилитипреферренце**](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




