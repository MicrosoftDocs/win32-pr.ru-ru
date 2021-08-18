---
description: Определяет, является ли указанная база данных одной из стандартных баз данных (Сисмаин, AppHelp, Дрвмаин или Мсимаин).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: Функция Сдбисстандарддатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7ef30f54b4d8eb4df4d8f136de6357a072cdb0183f462cb3af8a9340ce68b0c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045194"
---
# <a name="sdbisstandarddatabase-function"></a>Функция Сдбисстандарддатабасе

Определяет, является ли указанная база данных одной из стандартных баз данных (Сисмаин, AppHelp, Дрвмаин или Мсимаин).

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Гуиддб* \[ окне\]
</dt> <dd>

Идентификатор GUID для базы данных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **значение true** , если идентификатор GUID представляет стандартную базу данных, или **значение false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




