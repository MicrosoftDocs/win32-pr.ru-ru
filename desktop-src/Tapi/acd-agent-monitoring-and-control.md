---
description: Мониторинг и контроль состояния ACD-агента на станциях поддерживается с помощью этих функций Линежетаженткапс Линежетажентстатус Линежетажентграуплист Линежетажентактивитилист lineSetAgentGroup lineSetAgentState и lineSetAgentActivity.
ms.assetid: 2851fe54-f807-4cef-b6ca-2dcc7e1ae6fb
title: Мониторинг и контроль агента ACD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8986fc31e8b30e8b32c4b347a26abfa46adbd426c20c506553ae2f41ea879a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872661"
---
# <a name="acd-agent-monitoring-and-control"></a>Мониторинг и контроль агента ACD

Мониторинг и контроль состояния ACD-агента на станциях поддерживается с помощью следующих функций: [**линежетаженткапс**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa), [**линежетажентстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa), [**линежетажентграуплист**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista), [**линежетажентактивитилист**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista), [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup), [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)и [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).

Сообщение [**Line \_ Агент находится**](line-agentstatus.md) используется, чтобы указать, когда изменились сведения об агенте.

Эти элементы управления связаны с адресом, а не со строкой, так как многие системы ACD реализуются с помощью различных ACD-очередей, связанных с кнопками в телефонном терминале (и отдельных внешнего вида вызовов). Кроме того, ACD на телефонах агентов часто могут иметь отдельные внешнего вида вызовов для личных вызовов.

В архитектуре, ACD-функции должны быть реализованы в серверном приложении. Функции клиента, упомянутые выше, вместо сопоставления с поставщиком услуг телефонии передаются в серверное приложение, зарегистрированное (с помощью параметра [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen)) в качестве обработчика для таких функций. Сообщение [**Line \_ проксирекуест**](line-proxyrequest.md) используется для сигнализации приложения обработчика о выполнении запроса. оно вызывает функцию [**линепроксиреспонсе**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) для возвращения результатов и данных. Приложения обработчика также могут вызывать [**линепроксимессаже**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) для создания \_ сообщений агент находится при необходимости. В случае устаревшей УАТС или автономной ACD, которая реализует функцию ACD, поставщик услуг телефонии для коммутатора должен включать приложение прокси-сервера, которое принимает запросы и направляет их (возможно, с помощью функций [**линедевспеЦифик**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) или частного интерфейса) поставщику услуг, который направляет их в коммутатор.

 

 



