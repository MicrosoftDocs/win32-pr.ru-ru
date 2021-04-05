---
title: Параметры реестра для System-Wide безопасности
description: Параметры реестра для System-Wide безопасности
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986337"
---
# <a name="registry-values-for-system-wide-security"></a>Параметры реестра для System-Wide безопасности

Не рекомендуется изменять параметры безопасности на уровне системы, так как это повлияет на все серверные приложения COM, которые не устанавливают собственную систему безопасности на уровне процесса и могут препятствовать их правильной работе. Если вы изменяете параметры безопасности на уровне системы, чтобы они влияли на параметры безопасности для конкретного приложения COM, вместо этого следует изменить параметры безопасности для этого конкретного COM-приложения. Дополнительные сведения о настройке безопасности на уровне процесса см. в разделе [setting Process-Wide Security](setting-processwide-security.md).

Определенные значения в реестре используются для определения параметров безопасности для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Для изменения этих параметров безопасности по умолчанию для компьютера можно использовать Dcomcnfg.exe. Пошаговые инструкции, описывающие использование Dcomcnfg.exe для этой цели, см. в разделе [настройка System-Wide безопасности с помощью DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Другой способ изменения параметров по умолчанию для всей системы заключается в непосредственном управлении значениями реестра. Однако только администраторы и система имеют полный доступ к части реестра, содержащей параметры безопасности вызова по умолчанию для всей системы. Все остальные пользователи имеют доступ только для чтения.

Ниже приведены именованные значения, влияющие на параметры безопасности на уровне системы.

-   [дефаултлаунчпермиссион](defaultlaunchpermission.md)
-   [дефаултакцесспермиссион](defaultaccesspermission.md)
-   [легациаусентикатионлевел](legacyauthenticationlevel.md)
-   [легациимперсонатионлевел](legacyimpersonationlevel.md)
-   [легацисекуререференцес](legacysecurereferences.md)
-   [српруннингобжектчеккс](srprunningobjectchecks.md)
-   [српактиватеасактиваторчеккс](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка безопасности Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 




