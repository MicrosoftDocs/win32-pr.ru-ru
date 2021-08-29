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
ms.openlocfilehash: feeb622fd196ed20efb60d866d59b634fdcd9ecd955a97a1d7af0aef1347c8f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815323"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбинитдатабасе**](sdbinitdatabase.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**тагреф**](tagref.md)
</dt> </dl>

 

 




