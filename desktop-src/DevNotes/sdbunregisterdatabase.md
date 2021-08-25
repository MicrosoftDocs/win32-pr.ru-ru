---
description: Отменяет регистрацию указанной базы данных и делает ее более недоступной.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: Функция Сдбунрегистердатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2ea0cfeedbf74bea02af60b8c01d04b9e0e02f527ba35c0478da801253687b8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815314"
---
# <a name="sdbunregisterdatabase-function"></a>Функция Сдбунрегистердатабасе

Отменяет регистрацию указанной базы данных и делает ее более недоступной.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуиддб* \[ окне\]
</dt> <dd>

Идентификатор GUID базы данных. Этот параметр не может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбрегистердатабасикс**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




