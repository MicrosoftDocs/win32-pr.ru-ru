---
title: Функция Вссетаутофаил (Вебсервицесдебуг. h)
description: Задает следующую точку для внедрения сбоя. Это функция только для отладки.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Веб-службы Вссетаутофаил Function для Windows
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
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534925"
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Вебсервицесдебуг. h</dt> </dl> |



 

 





