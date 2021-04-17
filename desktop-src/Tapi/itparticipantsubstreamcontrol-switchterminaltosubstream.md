---
description: Метод Свитчтерминалтосубстреам задает терминал для подпотока участника.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'Метод ИтпартиЦипантсубстреамконтрол:: Свитчтерминалтосубстреам (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680057"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a>Метод ИтпартиЦипантсубстреамконтрол:: Свитчтерминалтосубстреам

\[**Свитчтерминалтосубстреам** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Метод **свитчтерминалтосубстреам** задает терминал для подпотока участника.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*питтерминал* \[ окне\]
</dt> <dd>

Указатель на интерфейс [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .

</dd> <dt>

*питсубстреам* \[ окне\]
</dt> <dd>

Указатель на интерфейс [**итсубстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                                     | Описание                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>            | Метод успешно выполнен.<br/>                                                                       |
| <dl> <dt>**\_непредвиденная E**</dt> </dl>    | Не удалось получить доступ к сведениям о участнике для потока.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | Параметр *ппартиЦипант* или *питсубстреам* не указывает на допустимый интерфейс.<br/> |
| <dl> <dt>**\_нежелательные \_ элементы TAPI**</dt> </dl> | Подпоток не готов.<br/>                                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Недостаточно памяти для выполнения операции.<br/>                                    |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|---------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                                 |
| Header<br/>       | <dl> <dt>Конфприв. h</dt> </dl> |
| Библиотека<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итпартиЦипантсубстреамконтрол**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**итпартиЦипант**](itparticipant.md)
</dt> <dt>

[**итсубстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

