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
# <a name="kerberos-sspap"></a><span data-ttu-id="a7829-103">Поставщик общих служб (AP) Kerberos</span><span class="sxs-lookup"><span data-stu-id="a7829-103">Kerberos SSP/AP</span></span>

<span data-ttu-id="a7829-104">Пакет проверки подлинности [*Kerberos*](../secgloss/k-gly.md) используется при входе в сеть; локальные входы в систему обрабатываются MSV1 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="a7829-104">The [*Kerberos*](../secgloss/k-gly.md) authentication package is used when logging on to a network; local logons are handled by MSV1\_0.</span></span>

<span data-ttu-id="a7829-105">Когда пользователь входит в систему с использованием сетевой учетной записи, по умолчанию Kerberos пытается подключиться к [*центр распространения ключейу*](../secgloss/k-gly.md) Kerberos (KDC) на контроллере домена и получить билет предоставления билета (TGT), используя данные входа, предоставленные пользователем.</span><span class="sxs-lookup"><span data-stu-id="a7829-105">When a user logs on using a network account, by default, Kerberos attempts to connect to the Kerberos [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) on the domain controller and obtain a ticket granting ticket (TGT) by using the logon data supplied by the user.</span></span>

<span data-ttu-id="a7829-106">Если Kerberos KDC недоступен, Windows использует MSV1 \_ 0 и сквозную проверку подлинности, как описано в [ \_ пакете проверки подлинности MSV1 0](msv1-0-authentication-package.md).</span><span class="sxs-lookup"><span data-stu-id="a7829-106">If a Kerberos KDC is not available, Windows uses MSV1\_0 and pass-through authentication as described in [MSV1\_0 Authentication Package](msv1-0-authentication-package.md).</span></span>

<span data-ttu-id="a7829-107">Пакет проверки подлинности Kerberos поддерживает версию 5 (версия 6) протокола Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a7829-107">The Kerberos authentication package supports version 5, revision 6 of the Kerberos protocol.</span></span> <span data-ttu-id="a7829-108">Этот протокол основан на стандарте Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span><span class="sxs-lookup"><span data-stu-id="a7829-108">This protocol is based on Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span></span> <span data-ttu-id="a7829-109">Дополнительные сведения см. на веб-сайте IETF:</span><span class="sxs-lookup"><span data-stu-id="a7829-109">For more information, see the IETF website:</span></span>

[https://www.ietf.org](https://www.ietf.org/)

<span data-ttu-id="a7829-110">Дополнительные сведения о протоколе Kerberos см. в разделе [Microsoft Kerberos](microsoft-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="a7829-110">For more information about Kerberos, see [Microsoft Kerberos](microsoft-kerberos.md).</span></span>

## <a name="kerberos-credential-formats"></a><span data-ttu-id="a7829-111">Форматы учетных данных Kerberos</span><span class="sxs-lookup"><span data-stu-id="a7829-111">Kerberos Credential Formats</span></span>

<span data-ttu-id="a7829-112">[*Учетные данные*](../secgloss/c-gly.md) пользователя, назначенные пакетом проверки подлинности Kerberos после успешной попытки входа, — это билет и временный ключ шифрования, часто называемый [*ключом сеанса*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a7829-112">The user [*credentials*](../secgloss/c-gly.md) assigned by the Kerberos authentication package after a successful logon attempt are a ticket and a temporary encryption key, often called a [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="a7829-113">Билет содержит как зашифрованную копию учетных данных клиента, так и ключ сеанса.</span><span class="sxs-lookup"><span data-stu-id="a7829-113">The ticket contains both an encrypted copy of the client's credentials and the session key.</span></span>

 

 
