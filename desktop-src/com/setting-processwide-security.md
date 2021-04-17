---
title: Настройка безопасности Process-Wide
description: Существует несколько способов установки безопасности на уровне процесса.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710175"
---
# <a name="setting-process-wide-security"></a>Настройка безопасности Process-Wide

Существует несколько способов установки безопасности на уровне процесса. Первый способ заключается в том, что использование средства Dcomcnfg.exe проще, поскольку оно не требует программирования. Второй способ предоставляет программисту больший контроль и требует вызова [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Другой способ — задать безопасность на уровне процесса в реестре с помощью ключа [AppID](appid-key.md) .

Дополнительные сведения об этих методах см. в следующих разделах:

-   [Настройка безопасности Process-Wide с помощью DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)
-   [Настройка безопасности Process-Wide с помощью CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md)
-   [Настройка безопасности Process-Wide в реестре](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка безопасности на уровне прокси-сервера интерфейса](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[Настройка безопасности для приложений COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




