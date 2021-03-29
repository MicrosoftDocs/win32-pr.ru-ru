---
description: Завершает операции записи для указанного списка.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: Функция Сдбендврителисттаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662063"
---
# <a name="sdbendwritelisttag-function"></a>Функция Сдбендврителисттаг

Завершает операции записи для указанного списка.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл в, out\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*тилист* \[ окне\]
</dt> <dd>

[**TAGID**](tagid.md) списка

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="remarks"></a>Комментарии

Вызовите эту функцию после записи всех записей списка. Он помечает конец списка.

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

[**сдбклоседатабасеврите**](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




