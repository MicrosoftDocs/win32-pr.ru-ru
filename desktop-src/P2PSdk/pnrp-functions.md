---
description: API поставщика пространства имен PNRP использует следующие функции.
ms.assetid: 7c9f2dd7-8dbc-4bbe-b53c-8036c79faa8a
title: Функции PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f109684be61bf1a9a194acb89b22fd4a50be652a6615a18a789e157ca2a5d909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034384"
---
# <a name="pnrp-functions"></a>Функции PNRP

API поставщика пространства имен PNRP использует следующие функции.



| Функция                                                             | Описание                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**пирнаметопирхостнаме**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname)             | кодирует введенное имя однорангового узла как формат, который можно использовать при последующем вызове функции [**функцию getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows sockets. |
| [**пирхостнаметопирнаме**](/windows/desktop/api/P2P/nf-p2p-peerhostnametopeername)             | Декодирует имя узла, возвращенное [**пирнаметопирхостнаме**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname) , в строку имен одноранговых узлов, которую он представляет.                            |
| [**пирпнрпстартуп**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartup)                           | Запускает службу PNRP для вызывающего однорангового узла.                                                                                |
| [**пирпнрпшутдовн**](/windows/desktop/api/P2P/nf-p2p-peerpnrpshutdown)                         | Завершает работу работающего экземпляра службы PNRP и освобождает все связанные с ней ресурсы.                             |
| [**пирпнрпрегистер**](/windows/desktop/api/P2P/nf-p2p-peerpnrpregister)                         | Регистрирует одноранговый узел в облаке PNRP и возвращает маркер, который можно использовать для обновления регистрации.                                                           |
| [**пирпнрпупдатерегистратион**](/windows/desktop/api/P2P/nf-p2p-peerpnrpupdateregistration)     | Обновляет сведения о регистрации PNRP для имени.                                                                                                        |
| [**пирпнрпунрегистер**](/windows/desktop/api/P2P/nf-p2p-peerpnrpunregister)                     | Отменяет регистрацию однорангового узла в облаке PNRP.                                                                                                                        |
| [**пирпнрпресолве**](/windows/desktop/api/P2P/nf-p2p-peerpnrpresolve)                           | Получает адреса конечных точек, зарегистрированные для указанного имени однорангового узла.                                                                                        |
| [**пирпнрпстартресолве**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)                 | Запускает асинхронную операцию разрешения имени однорангового узла.                                                                                                       |
| [**пирпнрпжетклаудинфо**](/windows/desktop/api/P2P/nf-p2p-peerpnrpgetcloudinfo)                 | Получает сведения о облаках PNRP, в которых участвует вызывающий одноранговый узел.                                         |
| [**пирпнрпендресолве**](/windows/desktop/api/P2P/nf-p2p-peerpnrpendresolve)                     | Закрывает маркер асинхронной операции разрешения PNRP, инициированной предыдущим вызовом [**пирпнрпстартресолве**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve).      |
| [PNRP и Всалукупсервицебегин](pnrp-and-wsalookupservicebegin.md) | Запускает процесс, позволяющий приложению разрешать имена и перечислять сетевые облака.                                                                 |
| [PNRP и Всалукупсервицеенд](pnrp-and-wsalookupserviceend.md)     | Завершает запрос, инициированный в предыдущем вызове [**всалукупсервицебегин**](winsock-nsp-reference-links.md).                                             |
| [PNRP и Всалукупсервиценекст](pnrp-and-wsalookupservicenext.md)   | Соответствует запросам, указанным в предыдущем вызове [**всалукупсервицебегин**](winsock-nsp-reference-links.md).                                                |
| [PNRP и Всанспиоктл](pnrp-and-wsanspioctl.md)                     | Получает уведомления об изменениях в списке сетевых облаков и доступности результатов запроса на разрешение имен.                                     |
| [PNRP и Всасетсервице](pnrp-and-wsasetservice.md)                 | Регистрирует или удаляет [одноранговые имена](peer-names.md).                                                                                                           |



 

 

 
