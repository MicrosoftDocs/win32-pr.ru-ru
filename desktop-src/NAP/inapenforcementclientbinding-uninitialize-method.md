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
ms.openlocfilehash: 613646eb169ab12c788cc294ab012962606a77b5f9fe5dfc8c041e6a4ad6fa35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940149"
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



 

## <a name="remarks"></a>Remarks

Напажент блокирует дальнейшую обработку до завершения всех существующих вызовов интерфейсов [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) и [**инапенфорцементклиенткаллбакк**](inapenforcementclientcallback.md) . В конце этого вызова Напажент освобождает все ссылки на клиентские указатели COM на принудительное применение.

Перед вызовом этой функции необходимо вызвать [**инапенфорцементклиентбиндинг:: нотификоннектионстатедовн**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) для всех активных соединений, чтобы SHA мог получать уведомления, если какие-либо из их SoH-Requests были потеряны.

Клиент принудительного применения должен вызвать метод [**инапенфорцементклиентбиндинг:: Initialize**](inapenforcementclientbinding-initialize-method.md) перед вызовом этого или любого другого метода интерфейса [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) .

## <a name="requirements"></a>Требования



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

[**Инапенфорцементклиентбиндинг:: Нотификоннектионстатедовн**](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[**инапенфорцементклиенткаллбакк**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





