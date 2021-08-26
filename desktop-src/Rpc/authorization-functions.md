---
title: Функции авторизации (RPC)
description: Каждый раз, когда серверная программа получает клиентский запрос на доступ к одной из удаленных процедур управления, Библиотека времени выполнения RPC вызывает функцию авторизации по умолчанию.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47234f83ae76ab6ee29ed434099ba3e4a7dbb3f9c7a01a2448d0cb0dad0267dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023418"
---
# <a name="authorization-functions"></a>Функции авторизации

Каждый раз, когда серверная программа получает клиентский запрос на доступ к одной из удаленных процедур управления, Библиотека времени выполнения RPC вызывает функцию авторизации по умолчанию. Эта функция использует поставщик общих служб для проверки учетных данных клиента и авторизации или отклонения запроса.

Серверная программа может переопределить функцию авторизации, предоставляемую поставщиком общих служб. Вызовите функцию [**рпкмгмтсетаусоризатионфн**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) и передайте ее в адрес функции авторизации. После того как серверная программа настроит функцию авторизации, Библиотека времени выполнения RPC вызывает ее каждый раз, когда серверная программа получает клиентский запрос одной из функций управления. Дополнительные сведения см. в разделе [**рпкмгмтиссерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**рпкмгмтинкифидс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**рпкмгмтинксерверпринкнаме**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)и [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).

 

 




