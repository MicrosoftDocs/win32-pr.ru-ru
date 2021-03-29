---
title: Используемый поставщик безопасности
description: Все остальные элементы равны, используйте RPC \_ c \_ AUTHN \_ GSS \_ Kerberos или RPC \_ c \_ AUTHN \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776106"
---
# <a name="which-security-provider-to-use"></a>Используемый поставщик безопасности

Все остальные элементы равны, используйте RPC \_ c \_ AUTHN \_ GSS \_ Kerberos или RPC \_ c \_ AUTHN \_ GSS \_ Negotiate. Каждый из них предоставляет наиболее масштабируемую и безопасную службу. При использовании RPC \_ C \_ AUTHN GSS \_ для \_ согласования на сервере это позволяет клиентам нижнего уровня, таким как клиенты NTLM, подключаться к серверу. Если это нежелательно, либо Ограничьте выбор \_ только RPC C \_ AUTHN \_ GSS \_ только Kerberos, либо вызовите [**рпкбиндингинкаусклиентекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) , чтобы определить, какой поставщик безопасности используется клиентом, и отклоните доступ к клиентам, использующим NTLM. Предпочтительным способом установки поставщика безопасности, используемого клиентом, является функция [**рпксерверинккаллаттрибутес**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .

 

 




