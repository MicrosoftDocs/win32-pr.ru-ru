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
ms.openlocfilehash: 3e72c8ef4760d611c45291f0de1039b915e9bc8fedde94c314bb1272e4b99b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891284"
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



 

## <a name="remarks"></a>Remarks

Клиент принудительного применения должен вызвать метод [**инапенфорцементклиентбиндинг:: Initialize**](inapenforcementclientbinding-initialize-method.md) перед вызовом этого или любого другого метода интерфейса [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                |
| Заголовок<br/>                   | <dl> <dt>Напенфорцементклиент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напенфорцементклиент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>См. также

<dl> <dt>


</dt> <dt>

[**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md)
</dt> <dt>

[**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





