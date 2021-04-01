---
title: Метод Инапенфорцементклиентбиндинг CreateConnection (Напенфорцементклиент. h)
description: Используется принудительно триггерами для создания объектов подключения.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- Метод CreateConnection NAP
- Метод CreateConnection NAP, интерфейс Инапенфорцементклиентбиндинг
- Инапенфорцементклиентбиндинг интерфейса NAP, метод CreateConnection
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071420"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a>Метод Инапенфорцементклиентбиндинг:: CreateConnection

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод фабрики **инапенфорцементклиентбиндинг:: CreateConnection** используется принудительно для создания объектов подключения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Подключение к* \[ заполняет\]
</dt> <dd>

Указатель COM на новый интерфейс [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) , возвращенный системой защиты доступа к сети.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Также могут возвращаться другие коды ошибок, относящиеся к COM.



| Код возврата                                                                                     | Описание                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl>           | Операция прошла успешно.<br/>                            |
| <dl> <dt>**Д \_ ACCESSDENIED**</dt> </dl> | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**Д \_ OUTOFMEMORY**</dt> </dl>  | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |



 

## <a name="remarks"></a>Комментарии

Клиент принудительного применения должен вызвать метод [**инапенфорцементклиентбиндинг:: Initialize**](inapenforcementclientbinding-initialize-method.md) перед вызовом этого или любого другого метода интерфейса [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Напенфорцементклиент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напенфорцементклиент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>


</dt> <dt>

[**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md)
</dt> <dt>

[**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





