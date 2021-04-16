---
description: Находит первую запись DWORD в указанном индексе, которая соответствует заданным условиям.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: Функция Сдбфиндфирстдвординдекседтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538264"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>Функция Сдбфиндфирстдвординдекседтаг

Находит первую запись **DWORD** в указанном индексе, которая соответствует заданным условиям.

## <a name="syntax"></a>Синтаксис


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*твхич* \[ окне\]
</dt> <dd>

Тип индекса. Список значений см. в разделе " [**тег**](tag.md) ".

</dd> <dt>

*tKey* \[ окне\]
</dt> <dd>

Тип ключа.

</dd> <dt>

*двнаме* \[ окне\]
</dt> <dd>

Имя найденных данных. Это значение будет преобразовано в ключ.

</dd> <dt>

*пфиндинфо* \[ заполняет\]
</dt> <dd>

Структура [**поиска \_ сведений**](find-info.md) , которая получает запись.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**TAGID** первого совпадения или **тега \_ null** , если совпадений не найдено.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбфиндфирсттаг**](sdbfindfirsttag.md)
</dt> </dl>

 

 




