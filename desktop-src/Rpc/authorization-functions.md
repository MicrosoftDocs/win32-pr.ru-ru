---
title: Функции авторизации (RPC)
description: Каждый раз, когда серверная программа получает клиентский запрос на доступ к одной из удаленных процедур управления, Библиотека времени выполнения RPC вызывает функцию авторизации по умолчанию.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490c06ba8e40f132c17986edaef4dc02bbe056d7
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2019
ms.locfileid: "104069308"
---
# <a name="authorization-functions"></a>Функции авторизации

Каждый раз, когда серверная программа получает клиентский запрос на доступ к одной из удаленных процедур управления, Библиотека времени выполнения RPC вызывает функцию авторизации по умолчанию. Эта функция использует поставщик общих служб для проверки учетных данных клиента и авторизации или отклонения запроса.

Серверная программа может переопределить функцию авторизации, предоставляемую поставщиком общих служб. Вызовите функцию [**рпкмгмтсетаусоризатионфн**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) и передайте ее в адрес функции авторизации. После того как серверная программа настроит функцию авторизации, Библиотека времени выполнения RPC вызывает ее каждый раз, когда серверная программа получает клиентский запрос одной из функций управления. Дополнительные сведения см. в разделе [**рпкмгмтиссерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**рпкмгмтинкифидс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**рпкмгмтинксерверпринкнаме**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)и [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).

 

 




