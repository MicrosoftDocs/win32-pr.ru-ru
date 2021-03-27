---
description: Преобразует строку в идентификатор GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: Функция Гуидфромстринг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909556"
---
# <a name="guidfromstring-function"></a>Функция Гуидфромстринг

\[**Гуидфромстринг** доступен в Windows XP с пакетом обновления 2 (SP2) или Windows Vista. Он может быть изменен или недоступен в последующих версиях. Приложения должны использовать [**клсидфромстринг**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) или [**иидфромстринг**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) вместо этой функции.\]

Преобразует строку в идентификатор GUID.

## <a name="syntax"></a>Синтаксис


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПСЗ* \[ окне\]
</dt> <dd>

Тип: **LPCTSTR**

Указатель на строку, завершающуюся нулем, для преобразования. Строка должна иметь следующий вид:

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

*пгуид* \[ заполняет\]
</dt> <dd>

Тип: **лпгуид**

Указатель на буфер для получения идентификатора GUID при возврате из метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **bool** .

**Значение true** , если GUID был успешно создан; в противном случае — **значение false**.

## <a name="remarks"></a>Примечания

Эта функция не объявлена в заголовке или экспортируется по имени из DLL-файла. Он должен быть загружен с Shell32.dll как порядковый номер 703 для **гуидфромстринга** и порядковый номер 704 для **гуидфромстрингв**.

К нему также можно получить доступ из Shlwapi.dll как порядковый номер 269 для **гуидфромстринга** и порядковый номер 270 для **гуидфромстрингв**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Гуидфромстрингв** (Юникод) и **гуидфромстринга** (ANSI)<br/>                |



 

 
