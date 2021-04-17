---
title: Функция Кбкреатеклиентинстанце (Кбклиент. h)
description: Создает экземпляр клиента RPC компонента подключение к удаленному рабочему столу Broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Кбкреатеклиентинстанце
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680048"
---
# <a name="cbcreateclientinstance-function"></a>Функция Кбкреатеклиентинстанце

Создает экземпляр клиента RPC компонента подключение к удаленному рабочему столу Broker.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Версия* \[ окне\]
</dt> <dd>

Указывает версию запрашиваемого интерфейса клиента компонента подключение к удаленному рабочему столу Broker. Это должно быть следующее значение.

<dt>

1
</dt> <dd>

Версия 1 клиента брокера подключение к удаленному рабочему столу.

</dd> </dl> </dd> <dt>

*ппкбклиент* \[ заполняет\]
</dt> <dd>

Адрес указателя интерфейса [**иконнектионброкерклиент**](iconnectionbrokerclient.md) , который получает объект клиента компонента Подключение к удаленному рабочему столу Broker.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кбклиент. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Кбклиент. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Cbclient.dll</dt> </dl> |



 

 





