---
title: Используемый поставщик безопасности
description: Все остальные элементы равны, используйте RPC \_ c \_ AUTHN \_ GSS \_ Kerberos или RPC \_ c \_ AUTHN \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b89bdb10eb95952183b2a992fd12a668e79b0716f3c453f597d2241323c4ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010452"
---
# <a name="which-security-provider-to-use"></a>Используемый поставщик безопасности

Все остальные элементы равны, используйте RPC \_ c \_ AUTHN \_ GSS \_ Kerberos или RPC \_ c \_ AUTHN \_ GSS \_ Negotiate. Каждый из них предоставляет наиболее масштабируемую и безопасную службу. При использовании RPC \_ C \_ AUTHN GSS \_ для \_ согласования на сервере это позволяет клиентам нижнего уровня, таким как клиенты NTLM, подключаться к серверу. Если это нежелательно, либо Ограничьте выбор \_ только RPC C \_ AUTHN \_ GSS \_ только Kerberos, либо вызовите [**рпкбиндингинкаусклиентекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) , чтобы определить, какой поставщик безопасности используется клиентом, и отклоните доступ к клиентам, использующим NTLM. Предпочтительным способом установки поставщика безопасности, используемого клиентом, является функция [**рпксерверинккаллаттрибутес**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .

 

 




