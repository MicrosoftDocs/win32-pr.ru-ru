---
description: Извлекает индекс указанного тега и типа ключа из указанной базы данных.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: Функция Сдбжетиндекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496176"
---
# <a name="sdbgetindex-function"></a>Функция Сдбжетиндекс

Извлекает индекс указанного тега и типа ключа из указанной базы данных.

## <a name="syntax"></a>Синтаксис


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
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

ТЕГ.

</dd> <dt>

*tKey* \[ окне\]
</dt> <dd>

Тип ключа.

</dd> <dt>

*лпдвфлагс* \[ out, необязательно\]
</dt> <dd>

Этот параметр может быть равен 0 **или \_ шимдб \_ уникальному \_ ключу индекса** (0x00000001).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**TAGID** индекса или **TAGID \_ null**.

## <a name="remarks"></a>Комментарии

Полученный индекс можно использовать для операций чтения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




