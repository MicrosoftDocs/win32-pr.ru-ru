---
description: 'Члены \_ перечисления типизированных сведений участника \_ определяют тип сведений о участнике, извлекаемых методом итпартиЦипант:: Get \_ партиЦипанттипединфо. Это перечисление используется приложениями, которые обращаются к Ипконф MSP.'
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: Перечисление PARTICIPANT_TYPED_INFO (Конфприв. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675394"
---
# <a name="participant_typed_info-enumeration"></a>\_Перечисление типизированных \_ сведений участника

\[**Участник \_ ТИПИЗИРОВАНная \_ информация** недоступна для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Члены перечисления **\_ типизированных \_ сведений участника** определяют тип сведений о участнике, извлекаемых методом [**итпартиЦипант:: Get \_ партиЦипанттипединфо**](itparticipant-get-participanttypedinfo.md) . Это перечисление используется приложениями, которые обращаются к [ИПКОНФ MSP](ipconf-msp.md).

## <a name="syntax"></a>Синтаксис


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**Пти \_ каноникалнаме**
</dt> <dd>

Каноническое имя участника, например someone@example.com .

</dd> <dt>

<span id="PTI_NAME"></span><span id="pti_name"></span>**\_имя Пти**
</dt> <dd>

Отображаемое имя участника.

</dd> <dt>

<span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**Пти \_ EMAILADDRESS**
</dt> <dd>

Адрес электронной почты участника.

</dd> <dt>

<span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**Пти \_ PHONENUMBER**
</dt> <dd>

Телефонный адрес участника.

</dd> <dt>

<span id="PTI_LOCATION"></span><span id="pti_location"></span>**\_Расположение Пти**
</dt> <dd>

Географический адрес участника.

</dd> <dt>

<span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_средство Пти**
</dt> <dd>

Приложение участника.

</dd> <dt>

<span id="PTI_NOTES"></span><span id="pti_notes"></span>**\_заметки Пти**
</dt> <dd>

Примечания, касающиеся участников.

</dd> <dt>

<span id="PTI_PRIVATE"></span><span id="pti_private"></span>**Пти \_ закрытый**
</dt> <dd>

Определяет экспериментальное или зависящее от приложения расширение источника (СДЕС). Дополнительные сведения см. в RFC 1889.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|---------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                                 |
| Header<br/>       | <dl> <dt>Конфприв. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ИтпартиЦипант:: Get \_ партиЦипанттипединфо**](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[Ипконф MSP](ipconf-msp.md)
</dt> <dt>

[Интерфейсы MSP Ипконф](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




