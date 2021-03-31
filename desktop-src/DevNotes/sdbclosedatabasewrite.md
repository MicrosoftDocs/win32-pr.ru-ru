---
description: Закрывает указанную базу данных.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: Функция Сдбклоседатабасеврите
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 24df6f9ce2c4f0fae4dd1c1ef244e006ea00c047
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895753"
---
# <a name="sdbclosedatabasewrite-function"></a>Функция Сдбклоседатабасеврите

Закрывает указанную базу данных.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл в, out\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Эта функция вызывает [**сдбклоседатабасе**](sdbclosedatabase.md); Поэтому эти две функции эквивалентны.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдббегинврителисттаг**](sdbbeginwritelisttag.md)
</dt> <dt>

[**сдбклоседатабасе**](sdbclosedatabase.md)
</dt> <dt>

[**сдбендврителисттаг**](sdbendwritelisttag.md)
</dt> </dl>

 

 




