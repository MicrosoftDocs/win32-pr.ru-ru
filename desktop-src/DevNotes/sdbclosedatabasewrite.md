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
ms.openlocfilehash: 0ef1c02731f2875fbdfc910243ed80faa28b6ab029314ea43ef281355a08487a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161585"
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

## <a name="remarks"></a>Remarks

Эта функция вызывает [**сдбклоседатабасе**](sdbclosedatabase.md); Поэтому эти две функции эквивалентны.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдббегинврителисттаг**](sdbbeginwritelisttag.md)
</dt> <dt>

[**сдбклоседатабасе**](sdbclosedatabase.md)
</dt> <dt>

[**сдбендврителисттаг**](sdbendwritelisttag.md)
</dt> </dl>

 

 




