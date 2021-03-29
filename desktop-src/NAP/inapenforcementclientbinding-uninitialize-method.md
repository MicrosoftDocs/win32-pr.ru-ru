---
title: Метод Uninitialize Инапенфорцементклиентбиндинг (Напенфорцементклиент. h)
description: Завершает службу Напажент.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Отмена инициализации метода NAP
- Отмена инициализации метода NAP, интерфейс Инапенфорцементклиентбиндинг
- Инапенфорцементклиентбиндинг интерфейс NAP, метод Uninitialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661991"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a>Метод Инапенфорцементклиентбиндинг:: Uninitialize

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **инапенфорцементклиентбиндинг:: Uninitialize** завершает службу напажент.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Также могут возвращаться другие коды ошибок, относящиеся к COM.



| Код возврата                                                                                     | Описание                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl>           | Операция прошла успешно.<br/>                            |
| <dl> <dt>**Д \_ ACCESSDENIED**</dt> </dl> | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**Д \_ OUTOFMEMORY**</dt> </dl>  | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |



 

## <a name="remarks"></a>Комментарии

Напажент блокирует дальнейшую обработку до завершения всех существующих вызовов интерфейсов [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) и [**инапенфорцементклиенткаллбакк**](inapenforcementclientcallback.md) . В конце этого вызова Напажент освобождает все ссылки на клиентские указатели COM на принудительное применение.

Перед вызовом этой функции необходимо вызвать [**инапенфорцементклиентбиндинг:: нотификоннектионстатедовн**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) для всех активных соединений, чтобы SHA мог получать уведомления, если какие-либо из их SoH-Requests были потеряны.

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

[**Инапенфорцементклиентбиндинг:: Нотификоннектионстатедовн**](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[**инапенфорцементклиенткаллбакк**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





