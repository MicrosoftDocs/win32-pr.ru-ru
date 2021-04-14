---
title: Метод Иконнектионброкеррекуест CheckStatus (Кбклиент. h)
description: Вызывается для определения состояния асинхронного запроса.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода CheckStatus
- Службы удаленных рабочих столов метода CheckStatus, интерфейс Иконнектионброкеррекуест
- Службы удаленных рабочих столов интерфейса Иконнектионброкеррекуест, метод CheckStatus
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416053"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a>Метод Иконнектионброкеррекуест:: CheckStatus

Вызывается для определения состояния асинхронного запроса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прекстатус* \[ заполняет\]
</dt> <dd>

Адрес переменной, получающей значение перечисления [**\_ \_ состояния запроса CB**](cb-request-status.md) , которое указывает состояние запроса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| Header<br/>                   | <dl> <dt>Кбклиент. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Кбклиент. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконнектионброкеррекуест**](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





