---
description: Возвращает количество элементов, хранящихся в этом перечислителе.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'Метод IEnumWiaItem2:: NOCOUNT (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 23c067b8e4da93d678f641890a85e2535b3ca50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080367"
---
# <a name="ienumwiaitem2getcount-method"></a>Метод IEnumWiaItem2:: NOCOUNT

Возвращает количество элементов, хранящихся в этом перечислителе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*cElt* \[ заполняет\]
</dt> <dd>

Тип: **ulong \** _

Получает указатель на _ *ulong**, который получает количество элементов в перечислении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




