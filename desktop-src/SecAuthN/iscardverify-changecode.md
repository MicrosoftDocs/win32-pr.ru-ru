---
description: Заменяет текущий код ЧВ (проверки держателя карты) новым кодом ЧВ.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: 'Метод Искардверифи:: Чанжекоде'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6fcb6d79e6135293ad91e3ea18fa535ef4edbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814384"
---
# <a name="iscardverifychangecode-method"></a>Метод Искардверифи:: Чанжекоде

\[Метод **чанжекоде** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **чанжекоде** заменяет текущий код ЧВ (проверка держателя карты) новым кодом ЧВ.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*полдкоде* \[ окне\]
</dt> <dd>

Указатель на [**ибитебуффер**](ibytebuffer.md) , содержащий текущий код пользователя.

</dd> <dt>

*пневкоде* \[ окне\]
</dt> <dd>

Указатель на [**ибитебуффер**](ibytebuffer.md) , содержащий новый код, который будет представлен [*смарт-карте*](../secgloss/s-gly.md) во время процесса изменения для проверки подлинности пользователя.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Указывает, является ли код глобальным или локальным, а также следует ли включать или отключать код.

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

**\_ \_ глобальный IHV для SC FL \_**
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

**локальный поставщик IHV для SC \_ FL \_ \_**
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

**\_включить SC FL \_ IHV \_**
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

**\_ \_ Отключение поставщика оборудования SC FL \_**
</dt> </dl> </dd> <dt>

*лреф* \[ окне\]
</dt> <dd>

Ссылка на смарт-карту.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений:



| Код возврата                                                                                   | Описание                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                |
| <dl> <dt>**\_указатель E**</dt> </dl>     | Передан неверный указатель.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                    |



 

## <a name="remarks"></a>Комментарии

Список всех методов, определенных этим интерфейсом, см. в разделе [**искардверифи**](iscardverify.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибитебуффер**](ibytebuffer.md)
</dt> <dt>

[**искардверифи**](iscardverify.md)
</dt> <dt>

[Возвращаемые значения смарт-карты](authentication-return-values.md)
</dt> </dl>

 

 
