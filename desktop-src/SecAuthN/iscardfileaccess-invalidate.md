---
description: Делает указанный файл (EF или DF) недопустимым. Недопустимый файл не может быть доступен другим методам до использования Рехабилитате.
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: 'Метод Искардфилеакцесс:: unvalidate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e1d74885f97eca64f403155f1dba52e398b9426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651027"
---
# <a name="iscardfileaccessinvalidate-method"></a>Метод Искардфилеакцесс:: unvalidate

\[Метод **Validate** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **unvalidate** делает указанный файл (EF или DF) недопустимым. Недопустимый файл не может быть доступен другим методам до использования [**рехабилитате**](iscardfileaccess-rehabilitate.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрпасспек* \[ окне\]
</dt> <dd>

File.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Указывает, следует ли использовать безопасный обмен сообщениями.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ Защита \_ обмена сообщениями через SC FL**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недействительный параметр.<br/>         |
| <dl> <dt>**\_указатель E**</dt> </dl>     | Передан неверный указатель.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                    |



 

## <a name="remarks"></a>Комментарии

Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искардфилеакцесс**](iscardfileaccess.md)
</dt> <dt>

[**рехабилитате**](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
