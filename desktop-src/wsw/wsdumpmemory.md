---
title: Функция Всдумпмемори (Вебсервицесдебуг. h)
description: Эта функция создает дамп всех выделений памяти для консоли.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Веб-службы Всдумпмемори Function для Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989129"
---
# <a name="wsdumpmemory-function"></a>Функция Всдумпмемори

Эта функция создает дамп всех выделений памяти для консоли.

> [!Note]  
> Эта функция предназначена только для отладки.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ошибка при* \[ в необязательное\]
</dt> <dd>

Указатель на объект [ \_ ошибки WS](ws-error.md) , в котором необходимо сохранить дополнительные сведения об ошибке в случае сбоя функции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                                |
| Header<br/>                   | <dl> <dt>Вебсервицесдебуг. h</dt> </dl> |



 

 





