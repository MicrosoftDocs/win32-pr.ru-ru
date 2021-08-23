---
title: Интерфейс Инапенфорцементклиентконнектион (Напенфорцементклиент. h)
description: Разрешить управление клиентскими подключениями. | Интерфейс Инапенфорцементклиентконнектион (Напенфорцементклиент. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- Инапенфорцементклиентконнектион интерфейса NAP
- Инапенфорцементклиентконнектион интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba017ca0948c5769466be9ad43ef68dc5ff60e75ecea430c96a1e8b0c36ab1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686254"
---
# <a name="inapenforcementclientconnection-interface"></a>Интерфейс Инапенфорцементклиентконнектион

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

**Инапенфорцементклиентконнектион** предоставляет методы, позволяющие управлять подключениями клиентов.

> [!Note]  
> [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) наследует все методы этого интерфейса, и вместо него следует использовать.

 

## <a name="members"></a>Элементы

Интерфейс **инапенфорцементклиентконнектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Инапенфорцементклиентконнектион** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **инапенфорцементклиентконнектион** содержит следующие методы.



| Метод                                                                                                                           | Описание                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Инапенфорцементклиентконнектион:: Жетконнектионид**](inapenforcementclientconnection-getconnectionid-method.md)               | Возвращает идентификатор соединения клиента.<br/>                                                                                          |
| [**Инапенфорцементклиентконнектион:: Жеткоррелатионид**](inapenforcementclientconnection-getcorrelationid-method.md)             | Возвращает идентификатор, используемый для корреляции запросов SoH и состояний работоспособности.<br/>                                                                  |
| [**Инапенфорцементклиентконнектион:: Жетенфорцерприватедата**](inapenforcementclientconnection-getenforcerprivatedata-method.md) | Используется средством применения для получения закрытых данных.<br/>                                                                                      |
| [**Флаги Инапенфорцементклиентконнектион:: "**](inapenforcementclientconnection-getflags-method.md)                             | Возвращает значение флага, которое отличает ответы первого времени от ответов, из-за кэширования Сохрекуестс с помощью триггеров.<br/> |
| [**Инапенфорцементклиентконнектион:: Жетисолатионинфо**](inapenforcementclientconnection-getisolationinfo-method.md)             | Используется для получения сведений о изоляции клиента.<br/>                                                                              |
| [**Инапенфорцементклиентконнектион:: Жетмакссизе**](inapenforcementclientconnection-getmaxsize-method.md)                         | Возвращает максимальный размер пакета SoH для этого клиента.<br/>                                                                       |
| [**Инапенфорцементклиентконнектион:: Жетприватедата**](inapenforcementclientconnection-getprivatedata-method.md)                 | Используется Напажент для получения закрытых данных.<br/>                                                                                      |
| [**Инапенфорцементклиентконнектион:: Жетсохрекуест**](inapenforcementclientconnection-getsohrequest-method.md)                   | Возвращает запрос SoH.<br/>                                                                                                          |
| [**Инапенфорцементклиентконнектион:: Жетсохреспонсе**](inapenforcementclientconnection-getsohresponse-method.md)                 | Возвращает SoH-Response, полученную клиентом принудительного применения.<br/>                                                                      |
| [**Инапенфорцементклиентконнектион:: Жетстрингкоррелатионид**](inapenforcementclientconnection-getstringcorrelationid-method.md) | Возвращает строку версии CorrelationId. Используется в основном для ведения журнала.<br/>                                             |
| [**Инапенфорцементклиентконнектион:: Initialize**](inapenforcementclientconnection-initialize-method.md)                         | Инициализирует подключение.<br/>                                                                                                    |
| [**Инапенфорцементклиентконнектион:: Сетконнектионид**](inapenforcementclientconnection-setconnectionid-method.md)               | Задает идентификатор соединения клиента.<br/>                                                                                          |
| [**Инапенфорцементклиентконнектион:: Сеткоррелатионид**](inapenforcementclientconnection-setcorrelationid-method.md)             | Задает идентификатор, используемый для корреляции запросов SoH и ответов о состоянии работоспособности.<br/>                                                                  |
| [**Инапенфорцементклиентконнектион:: Сетенфорцерприватедата**](inapenforcementclientconnection-setenforcerprivatedata-method.md) | Используется в принудительном применении для установки закрытых данных.<br/>                                                                                      |
| [**Инапенфорцементклиентконнектион:: Сетфлагс**](inapenforcementclientconnection-setflags-method.md)                             | Устанавливает флаг, который отличает отклики первого времени от ответов из-за того, что Сохрекуестс кэшируется принудительно.<br/>                  |
| [**Инапенфорцементклиентконнектион:: Сетисолатионинфо**](inapenforcementclientconnection-setisolationinfo-method.md)             | Используется Напажент для установки сведений о изоляции клиента.<br/>                                                           |
| [**Инапенфорцементклиентконнектион:: Сетмакссизе**](inapenforcementclientconnection-setmaxsize-method.md)                         | Задает максимальный размер пакета SoH для этого клиента.<br/>                                                                       |
| [**Инапенфорцементклиентконнектион:: Сетприватедата**](inapenforcementclientconnection-setprivatedata-method.md)                 | Используется Напажент для установки частных данных.<br/>                                                                                      |
| [**Инапенфорцементклиентконнектион:: Сетсохрекуест**](inapenforcementclientconnection-setsohrequest-method.md)                   | Задает запрос SoH.<br/>                                                                                                          |
| [**Инапенфорцементклиентконнектион:: Сетсохреспонсе**](inapenforcementclientconnection-setsohresponse-method.md)                 | Задает SoH-Response и используется клиентом принудительного применения при получении пакета.<br/>                                             |



 

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

[Интерфейсы NAP](nap-interfaces.md)
</dt> <dt>

[Справочник по NAP](nap-reference.md)
</dt> </dl>

 

