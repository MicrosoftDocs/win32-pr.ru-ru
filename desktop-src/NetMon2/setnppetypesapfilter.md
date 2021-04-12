---
description: Задает фильтр для BLOB-объектов ETYPE/SAP.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Функция Сетнппетипесапфилтер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344962"
---
# <a name="setnppetypesapfilter-function"></a>Функция Сетнппетипесапфилтер

Функция **сетнппетипесапфилтер** задает фильтр типа BLOB-объекта ETYPE/SAP.

## <a name="syntax"></a>Синтаксис


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Маркер для большого двоичного объекта.

</dd> <dt>

*нсапс* \[ окне\]
</dt> <dd>

Число SAPs.

</dd> <dt>

*нетипес* \[ окне\]
</dt> <dd>

Число ETYPE в устанавливаемой таблице etype.

</dd> <dt>

*лпсаптабле* \[ окне\]
</dt> <dd>

Указатель на заданную таблицу SAP.

</dd> <dt>

*лпетипетабле* \[ окне\]
</dt> <dd>

Указатель на заданную таблицу etype.

</dd> <dt>

*Филтерфлагс* \[ окне\]
</dt> <dd>

Заданные флаги фильтра.

</dd> <dt>

*херрорблоб* \[ заполняет\]
</dt> <dd>

Маркер для большого двоичного объекта ошибки, указывающий, где в исходном большом двоичном объекте произошла ошибка (если таковая имеется).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Нпптулс. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[жетнппетипесапфилтер](getnppetypesapfilter.md)
</dt> </dl>

 

 




