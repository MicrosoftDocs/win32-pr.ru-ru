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
ms.openlocfilehash: 36bfa9df62aba2ce8fb1df637c802369ca35911bd02c9876ea6b649c66698685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666479"
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

## <a name="remarks"></a>Remarks

Полученный индекс можно использовать для операций чтения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




