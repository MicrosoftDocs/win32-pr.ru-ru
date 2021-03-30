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
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072341"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




