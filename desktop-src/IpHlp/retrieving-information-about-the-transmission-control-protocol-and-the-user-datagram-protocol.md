---
description: Вспомогательный модуль IP позволяет получить доступ к сведениям о сетевых протоколах, используемых на локальном компьютере.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Получение сведений о протоколе управления передачей и протоколе датаграммы пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819481"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>Получение сведений о протоколе управления передачей и протоколе датаграммы пользователя

Вспомогательный модуль IP позволяет получить доступ к сведениям о сетевых протоколах, используемых на локальном компьютере. Для получения сведений о протоколе TCP и UDP на локальном компьютере используйте функции, описанные в следующих параграфах.

Функция [**жетткпстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) извлекает текущую СТАТИСТИКУ по протоколу TCP. Примеры кода, включающие **жетткпстатистикс** , см. [в разделе Получение сведений с помощью жетткпстатистикс](retrieving-information-using-gettcpstatistics.md).

Функция [**жетудпстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) извлекает текущую СТАТИСТИКУ по протоколу UDP.

Функция [**жетткптабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) ИЗВЛЕКАЕТ таблицу TCP-соединения. [**Жетудптабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) извлекает таблицу прослушивателя UDP.

Функция [**сетткпентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) позволяет разработчику установить состояние указанного TCP-подключения в MIB- \_ \_ состоянии TCP \_ DELETE \_ TCB.

 

 



