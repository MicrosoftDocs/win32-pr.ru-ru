---
title: Функции сервера (Управление сетью)
description: Функции сервера управления сетью выполняют задачи администрирования на локальном или удаленном сервере. Ниже перечислены функции сервера.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086abbd23682c17bb1bbfee6180067ca0947a848a4a8dfadb36ba1b87ef13c11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983138"
---
# <a name="server-functions-network-management"></a>Функции сервера (Управление сетью)

Функции сервера управления сетью выполняют задачи администрирования на локальном или удаленном сервере. Ниже перечислены функции сервера.



| Функция                                       | Описание                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**нетсервердискенум**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Возвращает список локальных дисков на сервере.                                   |
| [**нетсерверенум**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Список всех видимых серверов определенного типа (или типов) в указанном домене. |
| [**нетсервержетинфо**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Возвращает сведения о конфигурации указанного сервера.                        |
| [**нетсерверсетинфо**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Задает параметры операционной системы для сервера.                                        |



 

Только пользователь или приложение с членством в административной группе на локальном или удаленном сервере может выполнять административные задачи на этом сервере для управления работой сервера, доступом пользователей и предоставлением общего доступа к ресурсам. Параметры низкого уровня, влияющие на работу сервера, можно просмотреть и изменить, вызвав функции [**нетсервержетинфо**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) и [**нетсерверсетинфо**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) . Эти параметры определяются в файле LANMAN.INI сервера.

Большинство функций сервера управления сетью выполняются только на удаленном сервере. Функция [**нетсерверенум**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) выполняется как на локальной рабочей станции, так и на удаленном сервере. При попытке выполнения других серверных функций на локальной рабочей станции функции возвращают ошибку НЕРР \_ RemoteOnly.

Сведения, относящиеся к серверу, доступны на следующих уровнях:

-   [**\_Сведения о сервере \_ 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**\_Сведения о сервере \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**\_Сведения о сервере \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**\_Сведения о сервере \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**\_Сведения о сервере \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**\_Сведения о сервере \_ 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**\_Сведения о сервере \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**\_Сведения о сервере \_ 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**\_Сведения о сервере \_ 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**\_Сведения о сервере \_ 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**\_Сведения о сервере \_ 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**\_Сведения о сервере \_ 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**\_Сведения о сервере \_ 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**\_Сведения о сервере \_ 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**\_Сведения о сервере \_ 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**\_Сведения о сервере \_ 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**\_Сведения о сервере \_ 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**\_Сведения о сервере \_ 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**\_Сведения о сервере \_ 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**\_Сведения о сервере \_ 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**\_Сведения о сервере \_ 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**\_Сведения о сервере \_ 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**\_Сведения о сервере \_ 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**\_Сведения о сервере \_ 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**\_Сведения о сервере \_ 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**\_Сведения о сервере \_ 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**\_Сведения о сервере \_ 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**\_Сведения о сервере \_ 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**\_Сведения о сервере \_ 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**\_Сведения о сервере \_ 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**\_Сведения о сервере \_ 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

При программировании для Active Directory можно вызвать определенные методы интерфейса Active Directory (ADSI) для достижения тех же функций, которые можно достичь, вызвав функции сервера управления сетью. Дополнительные сведения см. в разделе [**иадскомпутер**](/windows/desktop/api/iads/nn-iads-iadscomputer).

Дополнительные сведения см. в статье [транспортная функция сервера и рабочей станции](server-and-workstation-transport-functions.md).

 

 
