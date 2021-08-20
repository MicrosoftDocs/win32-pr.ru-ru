---
title: Изменение параметров безопасности компьютера по умолчанию
description: Изменение параметров безопасности компьютера по умолчанию
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7936e2d0bc1113b651fd40f94e84037f00f4ffbe12b7e0232f1dc6a6cd8aaeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118105402"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a>Изменение параметров безопасности компьютера по умолчанию

Не рекомендуется изменять параметры безопасности на уровне системы, так как это повлияет на все серверные приложения COM, которые не устанавливают собственную систему безопасности на уровне процесса и могут препятствовать их правильной работе. Если вы изменяете параметры безопасности на уровне системы, чтобы они влияли на параметры безопасности для конкретного приложения COM, вместо этого следует изменить параметры безопасности для этого конкретного COM-приложения. Дополнительные сведения о настройке безопасности на уровне процесса см. в разделе [setting Process-Wide Security](setting-processwide-security.md).

Определенные значения в реестре определяют параметры безопасности для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Эти параметры можно изменить с помощью Dcomcnfg.exe.

Дополнительные сведения см. в следующих разделах:

-   [Параметры реестра для System-Wide безопасности](registry-values-for-machine-wide-security.md)
-   [Настройка безопасности System-Wide с помощью DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка безопасности на уровне процесса](setting-processwide-security.md)
</dt> <dt>

[Настройка безопасности для приложений COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




