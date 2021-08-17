---
description: Метод Directory извлекает из текущего каталога список файлов указанного типа.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: 'Искардфилеакцесс: метод:D каталога'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 009263a92f014367636c7ff16b7f43635f73fa1b2ed17b52d53e81152c6e15b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481304"
---
# <a name="iscardfileaccessdirectory-method"></a>Искардфилеакцесс: метод:D каталога

\[Метод **Directory** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Directory** извлекает из текущего каталога список файлов указанного типа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тип* \[ файла окне\]
</dt> <dd>

Тип файлов [*смарт-карты*](../secgloss/s-gly.md) для перечисления.



| Значение                                                                                                                                                                                      | Значение                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <dt>**\_каталоги типов \_ SC**</dt> </dl>           | Вывод списка только файлов каталога.<br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <dt>**\_файлы типов \_ SC**</dt> </dl>                             | Перечисление только простейших файлов.<br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <dt>**SC \_ Type \_ All \_ Files**</dt> </dl>                | Перечислите каталог и простейшие файлы.<br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <dt>**SC \_ тип \_ \_ файл каталога**</dt> </dl> | Файл каталога.<br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <dt>**SC \_ \_ прозрачный тип \_ EF**</dt> </dl> | Прозрачный простой файл.<br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <dt>**\_тип SC \_ фиксированный \_ EF**</dt> </dl>                   | Линейный фиксированный файл простой.<br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <dt>**\_ \_ циклическая ссылка на тип SC \_**</dt> </dl>                | Циклический простой файл.<br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <dt>**\_переменная типа \_ SC \_**</dt> </dl>          | Простой файл с линейной переменной.<br/>          |



 

</dd> <dt>

*ппфилелист* \[ заполняет\]
</dt> <dd>

Массив BSTR, представляющий список файлов, соответствующих спецификатору в *filetype*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Операция успешно завершена.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                             |
| <dl> <dt>**E \_ нотимпл**</dt> </dl>     | Этот метод не реализован в интерфейсе.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                                 |
| <dl> <dt>**\_указатель E**</dt> </dl>     | Для *ппфилелист* был передан недопустимый указатель.<br/>  |



 

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искардфилеакцесс**](iscardfileaccess.md)
</dt> </dl>

 

 
