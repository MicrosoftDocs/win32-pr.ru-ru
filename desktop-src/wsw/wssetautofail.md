---
title: Функция Вссетаутофаил (Вебсервицесдебуг. h)
description: Задает следующую точку для внедрения сбоя. Это функция только для отладки.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Веб-службы функции Вссетаутофаил для Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e2ae3ed731edce429aac78700d52d0e7504a5688d1bf35bbb9c64a5d34bc0a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838544"
---
# <a name="wssetautofail-function"></a>Функция Вссетаутофаил

Задает следующую точку для внедрения сбоя. Это функция только для отладки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*количество* \[ окне\]
</dt> <dd>

Указывает, сколько операций должно быть выполнено до начала ошибок.

</dd> <dt>

*Ошибка при* \[ в необязательное\]
</dt> <dd>

Указатель на объект [ \_ ошибки WS](ws-error.md) , в котором необходимо сохранить дополнительные сведения об ошибке в случае сбоя функции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Вебсервицесдебуг. h</dt> </dl> |



 

 





