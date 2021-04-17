---
description: Функция Жетнппетипесапфилтер извлекает фильтр ETYPE или SAP из заданного большого двоичного объекта.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Функция Жетнппетипесапфилтер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674488"
---
# <a name="getnppetypesapfilter-function"></a>Функция Жетнппетипесапфилтер

Функция **жетнппетипесапфилтер** извлекает фильтр ETYPE или SAP из заданного большого двоичного объекта.

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Обработчик для большого двоичного объекта.

</dd> <dt>

*пнсапс* \[ заполняет\]
</dt> <dd>

Указатель на возвращенное число протоколов в таблице SAP.

</dd> <dt>

*пнетипес* \[ заполняет\]
</dt> <dd>

Указатель на возвращенное число ETYPE в таблице etype.

</dd> <dt>

*ппсаптабле* \[ заполняет\]
</dt> <dd>

Указатель на возвращенную таблицу SAP.

</dd> <dt>

*ппетипетабле* \[ заполняет\]
</dt> <dd>

Указатель на возвращенную таблицу etype.

</dd> <dt>

*пфилтерфлагс* \[ заполняет\]
</dt> <dd>

Указатель на возвращаемые флаги фильтра.

</dd> <dt>

*херрорблоб* \[ заполняет\]
</dt> <dd>

Обработайте с BLOB-объектом ошибок, который указывает расположение в исходном большом двоичном объекте, где произошла ошибка (если таковая имеется).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.

## <a name="remarks"></a>Комментарии

Информация ETYPE/SAP хранится в категории **config** раздела НПП **owner** .

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

[сетнппетипесапфилтер](setnppetypesapfilter.md)
</dt> </dl>

 

 




