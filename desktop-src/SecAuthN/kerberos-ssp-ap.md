---
description: Пакет проверки подлинности Kerberos используется при входе в сеть; локальные входы в систему обрабатываются MSV1 \_ 0.
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: Поставщик общих служб (AP) Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080911"
---
# <a name="kerberos-sspap"></a>Поставщик общих служб (AP) Kerberos

Пакет проверки подлинности [*Kerberos*](../secgloss/k-gly.md) используется при входе в сеть; локальные входы в систему обрабатываются MSV1 \_ 0.

Когда пользователь входит в систему с использованием сетевой учетной записи, по умолчанию Kerberos пытается подключиться к [*центр распространения ключейу*](../secgloss/k-gly.md) Kerberos (KDC) на контроллере домена и получить билет предоставления билета (TGT), используя данные входа, предоставленные пользователем.

Если Kerberos KDC недоступен, Windows использует MSV1 \_ 0 и сквозную проверку подлинности, как описано в [ \_ пакете проверки подлинности MSV1 0](msv1-0-authentication-package.md).

Пакет проверки подлинности Kerberos поддерживает версию 5 (версия 6) протокола Kerberos. Этот протокол основан на стандарте Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt). Дополнительные сведения см. на веб-сайте IETF:

[https://www.ietf.org](https://www.ietf.org/)

Дополнительные сведения о протоколе Kerberos см. в разделе [Microsoft Kerberos](microsoft-kerberos.md).

## <a name="kerberos-credential-formats"></a>Форматы учетных данных Kerberos

[*Учетные данные*](../secgloss/c-gly.md) пользователя, назначенные пакетом проверки подлинности Kerberos после успешной попытки входа, — это билет и временный ключ шифрования, часто называемый [*ключом сеанса*](../secgloss/s-gly.md). Билет содержит как зашифрованную копию учетных данных клиента, так и ключ сеанса.

 

 
