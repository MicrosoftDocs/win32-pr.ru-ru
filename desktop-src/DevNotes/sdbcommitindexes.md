---
description: Фиксирует вновь созданные индексы для указанной базы данных.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: Функция Сдбкоммитиндексес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141099"
---
# <a name="sdbcommitindexes-function"></a>Функция Сдбкоммитиндексес

Фиксирует вновь созданные индексы для указанной базы данных.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbCommitIndexes(
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

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбдеклареиндекс**](sdbdeclareindex.md)
</dt> <dt>

[**сдбстартиндексинг**](sdbstartindexing.md)
</dt> <dt>

[**сдбстопиндексинг**](sdbstopindexing.md)
</dt> </dl>

 

 




