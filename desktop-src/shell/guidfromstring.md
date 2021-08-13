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
ms.openlocfilehash: 38dd6d6365c3b306e63634fee02ac7add07b1bf262598efc88ffec2595e14c82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351064"
---
# <a name="guidfromstring-function"></a>Функция Гуидфромстринг

\[**гуидфромстринг** доступен в Windows XP с пакетом обновления 2 (sp2) или Windows Vista. Он может быть изменен или недоступен в последующих версиях. Приложения должны использовать [**клсидфромстринг**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) или [**иидфромстринг**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) вместо этой функции.\]

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

## <a name="remarks"></a>Remarks

Эта функция не объявлена в заголовке или экспортируется по имени из файла .dll. Он должен быть загружен с Shell32.dll как порядковый номер 703 для **гуидфромстринга** и порядковый номер 704 для **гуидфромстрингв**.

К нему также можно получить доступ из Shlwapi.dll как порядковый номер 269 для **гуидфромстринга** и порядковый номер 270 для **гуидфромстрингв**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Гуидфромстрингв** (Юникод) и **гуидфромстринга** (ANSI)<br/>                |



 

 
