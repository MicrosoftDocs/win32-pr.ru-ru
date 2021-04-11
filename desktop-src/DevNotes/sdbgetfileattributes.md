---
description: Извлекает данные атрибута для указанного файла.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: Функция Сдбжетфилеаттрибутес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140735"
---
# <a name="sdbgetfileattributes-function"></a>Функция Сдбжетфилеаттрибутес

Извлекает данные атрибута для указанного файла.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпвсзфиленаме* \[ окне\]
</dt> <dd>

Путь к файлу.

</dd> <dt>

*ппаттринфо* \[ заполняет\]
</dt> <dd>

Массив структур [**аттринфо**](attrinfo.md) , содержащих данные атрибута.

</dd> <dt>

*лпдваттркаунт* \[ заполняет\]
</dt> <dd>

Количество атрибутов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="remarks"></a>Комментарии

Завершив работу с данными, освободите ее с помощью функции [**сдбфрифилеаттрибутес**](sdbfreefileattributes.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбформататтрибуте**](sdbformatattribute.md)
</dt> <dt>

[**сдбфрифилеаттрибутес**](sdbfreefileattributes.md)
</dt> </dl>

 

 




