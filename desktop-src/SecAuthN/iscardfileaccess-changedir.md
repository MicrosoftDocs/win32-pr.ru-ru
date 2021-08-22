---
description: Метод Чанжедир изменяет текущий каталог смарт-карты на новый указанный каталог.
ms.assetid: 1eb53236-c88f-4b43-ac91-de67d4029433
title: 'Метод Искардфилеакцесс:: Чанжедир'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.ChangeDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3d14f104fd40a10c4d17e3751b59245299e7c8f5b63508d6e73ef1140ec7e906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008062"
---
# <a name="iscardfileaccesschangedir-method"></a>Метод Искардфилеакцесс:: Чанжедир

\[Метод **чанжедир** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **чанжедир** изменяет текущий каталог [*смарт-карты*](../secgloss/s-gly.md) на новый указанный каталог.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ChangeDir(
  [in] REFTYPE refType,
  [in] BSTR    bstrNewDir
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*рефтипе* \[ окне\]
</dt> <dd>

Тип ссылки, используемый в *бстрневдир*.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**\_тип SC \_ по \_ имени**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**\_тип SC \_ по \_ идентификатору**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ Type \_ по \_ короткому типу**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ Type \_ по \_ любому**
</dt> </dl> </dd> <dt>

*бстрневдир* \[ окне\]
</dt> <dd>

Имя файла или каталога ( *рефтипе*) для выбора.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                    |



 

## <a name="remarks"></a>Remarks

Чтобы получить абсолютный путь к текущему выбранному каталогу, вызовите [**жеткуррентдир**](iscardfileaccess-getcurrentdir.md).

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

[**жеткуррентдир**](iscardfileaccess-getcurrentdir.md)
</dt> <dt>

[**искардфилеакцесс**](iscardfileaccess.md)
</dt> </dl>

 

 
