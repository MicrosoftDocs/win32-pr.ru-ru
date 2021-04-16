---
description: Запрашивает проверку пользователя.
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: 'Метод Искардверифи:: Verify'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650768"
---
# <a name="iscardverifyverify-method"></a>Метод Искардверифи:: Verify

\[Метод **Verify** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Verify** запрашивает проверку пользователя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*коде Pcode* \[ окне\]
</dt> <dd>

Содержит код, который будет представлен [*смарт-карте*](../secgloss/s-gly.md) в процессе ЧВ (проверка держателя карты).

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Указывает, является ли код глобальным или локальным.

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

**\_ \_ глобальный IHV для SC FL \_**
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

**локальный поставщик IHV для SC \_ FL \_ \_**
</dt> </dl> </dd> <dt>

*лреф* \[ окне\]
</dt> <dd>

Ссылка на смарт-карту.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод **Verify** возвращает одно из следующих значений:



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

[**искардверифи**](iscardverify.md)
</dt> </dl>

 

 
