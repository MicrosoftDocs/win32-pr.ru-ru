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
ms.openlocfilehash: a75dd64bfbeaf027839c63227c594ada7602101d059cbbd9d10deb085152918d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103654"
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

## <a name="remarks"></a>Remarks

Завершив работу с данными, освободите ее с помощью функции [**сдбфрифилеаттрибутес**](sdbfreefileattributes.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбформататтрибуте**](sdbformatattribute.md)
</dt> <dt>

[**сдбфрифилеаттрибутес**](sdbfreefileattributes.md)
</dt> </dl>

 

 




