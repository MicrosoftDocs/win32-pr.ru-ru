---
description: Закрывает указанную базу данных оболочек совместимости.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: Функция Сдбклоседатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072437"
---
# <a name="sdbclosedatabase-function"></a>Функция Сдбклоседатабасе

Закрывает указанную базу данных оболочек совместимости.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл в, out\]
</dt> <dd>

Маркер базы данных оболочек совместимости. Этот параметр не может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбопендатабасе**](sdbopendatabase.md)
</dt> </dl>

 

 




