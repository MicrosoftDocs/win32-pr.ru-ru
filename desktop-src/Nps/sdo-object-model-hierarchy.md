---
title: Иерархия объектной модели
description: Объекты в объектной модели SDO упорядочиваются в иерархии. Это означает, что объекты в SDO обеспечивают доступ к другим объектам в SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413242"
---
# <a name="object-model-hierarchy"></a>Иерархия объектной модели

Объекты в объектной модели SDO упорядочиваются в иерархии. Это означает, что объекты в SDO обеспечивают доступ к другим объектам в SDO.

Объекты предоставляют доступ к другим объектам двумя способами. Один из способов заключается в том, чтобы объект предоставлял интерфейс, предоставляющий методы для получения других объектов. Примером такого подхода является объект компьютера. Объект Machine предоставляет интерфейс [**исдомачине**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) . Метод [**исдомачине:: жетсервицесдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) извлекает объект службы. Метод [**исдомачине:: жетусерсдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) извлекает объект пользователя.

![объект компьютера, предоставляющий интерфейс исдомачине](images/sdo01.png)

Дополнительные сведения см. в разделе [Получение службы и пользователя сдос](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).

Второй способ, которым объекты предоставляют доступ к другим объектам, заключается в том, что коллекция объектов представляется как свойство объекта, содержащего его. Чтобы получить коллекцию объектов, вызовите [**исдо::**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) GetObject свойства объекта, представляющего коллекцию. Например, чтобы получить коллекцию политик, вызовите **исдо::** GetObject в интерфейсе [**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) , предоставляемом объектом NPS.

> [!Note]  
> Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.

 

![получение коллекции политик](images/sdo02.png)

Пример кода, который получает коллекцию Policies, см. в разделе [Получение коллекции](/windows/desktop/Nps/sdo-retrieving-a-collection).

[**Объект данных сервера NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) имеет следующие свойства, представляющие коллекции:

<dl> <dt>

<span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Аудиторов
</dt> <dd>

Единственным аудитором в коллекции аудиторий является [**журнал событий NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).

</dd> <dt>

<span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Политике
</dt> <dd>

Каждый [**объект политики**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) имеет свойство, представляющее коллекцию условий.

</dd> <dt>

<span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Профили
</dt> <dd>

Каждый [**объект профиля**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) в коллекциях Profiles имеет свойство, представляющее коллекцию атрибутов. Список атрибутов, поддерживаемых SDO, см. в разделе [атрибуты, поддерживаемые SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) .

</dd> <dt>

<span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>CHAP
</dt> <dd>

Коллекция Protocols содержит объект протокола RADIUS, который содержит коллекцию клиентов, представляющую клиенты RADIUS. См. раздел [Добавление клиента](/windows/desktop/Nps/sdo-adding-a-client) для примера кода, в котором показано, как получить коллекцию клиентов.

</dd> <dt>

<span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Политики прокси-сервера
</dt> <dd>

Эта коллекция содержит политики сетевого доступа, используемые для обработки запросов на подключение.

</dd> <dt>

<span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Профили прокси-сервера
</dt> <dd>

Эта коллекция содержит профили, используемые для обработки запросов на соединение.

</dd> <dt>

<span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Группы серверов RADIUS
</dt> <dd>

Каждая [**Группа серверов RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) в коллекции "группы серверов RADIUS" имеет свойство, представляющее коллекцию серверов в этой группе серверов.

</dd> <dt>

<span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Обработчики запросов
</dt> <dd>

Эта коллекция содержит коллекцию "оценщик сфер Майкрософт". В этой коллекции также доступны параметры "Проверка подлинности Microsoft NT SAM" и "учет Майкрософт".

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Объекты и свойства SDO](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[Поддерживаемые в SDO атрибуты](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 