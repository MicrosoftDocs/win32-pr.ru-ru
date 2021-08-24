---
title: Поставщики безопасности
description: Интерфейс поставщика поддержки безопасности (SSPI) обеспечивает взаимную проверку подлинности и предоставляется напрямую через интерфейсы API и службы SSPI, включенные на уровне SSPI, включая RPC.
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3685ad95b5e339853be947170bb0a8681a376d8d2f34368534d02b3b0cbdf4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183659"
---
# <a name="security-providers"></a>Поставщики безопасности

Интерфейс поставщика поддержки безопасности (SSPI) обеспечивает взаимную проверку подлинности и предоставляется напрямую через интерфейсы API и службы SSPI, включенные на уровне SSPI, включая RPC.

Не все пакеты безопасности, доступные для SSPI, поддерживают взаимную проверку подлинности. Чтобы получить взаимную проверку подлинности, приложение должно запросить взаимную проверку подлинности и пакет безопасности, который его поддерживает. например, пример кода для [взаимной проверки подлинности в службе Windows sockets с SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) использует пакет negotiate в Secur32.dll, который входит в состав Windows 2000.

 

 




