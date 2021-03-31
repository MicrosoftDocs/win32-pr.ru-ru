---
description: Создает новый тег списка для операций записи.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: Функция Сдббегинврителисттаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807709"
---
# <a name="sdbbeginwritelisttag-function"></a>Функция Сдббегинврителисттаг

Создает новый тег списка для операций записи.

## <a name="syntax"></a>Синтаксис


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*ттаг* \[ окне\]
</dt> <dd>

ТЕГ для новой записи. Это значение должно иметь тип " **\_ \_ список типов тегов**".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает [**TAGID**](tagid.md) нового списка при успешном выполнении или **TAGID \_ null** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбклоседатабасе**](sdbclosedatabase.md)
</dt> <dt>

[**сдбклоседатабасеврите**](sdbclosedatabasewrite.md)
</dt> <dt>

[**сдбендврителисттаг**](sdbendwritelisttag.md)
</dt> <dt>

[**ТЕГАМИ**](tag.md)
</dt> <dt>

[Типы тегов](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




