---
description: Создает ключ из строки.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: Функция Сдбмакеиндекскэйфромстринг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990306"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>Функция Сдбмакеиндекскэйфромстринг

Создает ключ из строки.

## <a name="syntax"></a>Синтаксис


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзкэй* \[ окне\]
</dt> <dd>

Строка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает ключ или значение 0, если возникает ошибка.

## <a name="remarks"></a>Комментарии

Стандартный ключ индекса — первые восемь символов строки, преобразованный в верхний регистр, а затем приведенный к значению **улонглонг** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




