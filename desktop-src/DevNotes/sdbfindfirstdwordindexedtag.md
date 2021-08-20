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
ms.openlocfilehash: 40f54dfc109ec2f7f4807d57052b9c4e1f99d5b629e8028be2931d9b42081f43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161575"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбфиндфирсттаг**](sdbfindfirsttag.md)
</dt> </dl>

 

 




