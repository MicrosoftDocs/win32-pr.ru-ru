---
description: Метод Delete удаляет файл в указанном месте в файловой системе смарт-карты.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: Искардфилеакцесс::D удалить метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 721830ea3d446585e7f52c699642b1534c78d34826722b5737e191dfce94c817
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008052"
---
# <a name="iscardfileaccessdelete-method"></a>Искардфилеакцесс::D удалить метод

\[Метод **Delete** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Delete** удаляет файл в указанном месте в файловой системе [*смарт-карты*](../secgloss/s-gly.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*рефтипе* \[ окне\]
</dt> <dd>

Тип ссылки, используемый в *бстрпасспек*.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**\_тип SC \_ по \_ имени**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**\_тип SC \_ по \_ идентификатору**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ Type \_ по \_ короткому типу**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ Type \_ по \_ любому**
</dt> </dl> </dd> <dt>

*бстрпасспек* \[ окне\]
</dt> <dd>

Идентификатор удаляемого файла.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Указывает, следует ли использовать безопасный обмен сообщениями и предварительно выделенные данные.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ Защита \_ обмена сообщениями через SC FL**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**предварительно \_ \_ выделенный SC FL**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                  | Описание                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Операция успешно завершена.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр.<br/>                             |
| <dl> <dt>**E \_ нотимпл**</dt> </dl>    | Этот метод не реализован в интерфейсе.<br/> |



 

## <a name="remarks"></a>Remarks

Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Создание**](iscardfileaccess-create.md)
</dt> <dt>

[**искардфилеакцесс**](iscardfileaccess.md)
</dt> </dl>

 

 
