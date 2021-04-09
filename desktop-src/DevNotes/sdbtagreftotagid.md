---
description: Получает TAGID и маркер для базы данных оболочек для указанного ТАГРЕФ.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: Функция Сдбтагрефтотагид
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141243"
---
# <a name="sdbtagreftotagid-function"></a>Функция Сдбтагрефтотагид

Получает **TAGID** и маркер для базы данных оболочек для указанного [**тагреф**](tagref.md).

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсдб* \[ окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости, возвращаемый функцией [**сдбинитдатабасе**](sdbinitdatabase.md) .

</dd> <dt>

*трвхич* \[ окне\]
</dt> <dd>

[**Тагреф**](tagref.md).

</dd> <dt>

*ппдб* \[ заполняет\]
</dt> <dd>

Результирующий обработчик для базы данных оболочек совместимости.

</dd> <dt>

*птивхич* \[ заполняет\]
</dt> <dd>

Результирующий **TAGID**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбинитдатабасе**](sdbinitdatabase.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**тагреф**](tagref.md)
</dt> </dl>

 

 




