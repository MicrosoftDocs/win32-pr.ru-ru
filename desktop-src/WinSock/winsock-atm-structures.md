---
description: В следующем списке приведены краткие описания каждой структуры Winsock ATM. Для получения дополнительных сведений о любой структуре щелкните имя структуры.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Структуры Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f45cafef8bcf628f9172f2ad7ce3323d0d5b0c3e2c3912d195615ea2471501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612804"
---
# <a name="winsock-atm-structures"></a>Структуры Winsock ATM

В следующем списке приведены краткие описания каждой структуры Winsock ATM. Для получения дополнительных сведений о любой структуре щелкните имя структуры.



| Структура ATM                           | Описание                                                |
|-----------------------------------------|------------------------------------------------------------|
| [**ATM- \_ адрес**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | Хранит данные об ATM-адресах для сокетов на основе ATM.             |
| [**\_БХЛИ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | Определяет сведения о B-ХЛИ для соответствующего сокета ATM. |
| [**\_БЛЛИ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | Определяет сведения о B-лли для соответствующего сокета ATM. |
| [**SOCKADDR \_ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | Хранит сведения об адресе сокета для сокетов ATM.         |



 

Для собственных служб ATM используйте AF \_ ATM для семейства адресов и SOCKADDR в качестве структуры адресов сокетов [**\_ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) . Чтобы открыть собственный сокет ATM, передайте \_ соккный ATM-код, \_ а также атмпрото \_ AAL5 или атмпрото \_ аалусер в функцию [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) соответственно.

 

 



