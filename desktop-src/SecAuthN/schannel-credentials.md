---
description: Протоколы SChannel занимают учетные данные для проверки подлинности серверов и, при необходимости, клиентов.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Учетные данные SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998396"
---
# <a name="schannel-credentials"></a><span data-ttu-id="17734-103">Учетные данные SChannel</span><span class="sxs-lookup"><span data-stu-id="17734-103">Schannel Credentials</span></span>

<span data-ttu-id="17734-104">Протоколы SChannel занимают учетные данные для проверки подлинности серверов и, при необходимости, клиентов.</span><span class="sxs-lookup"><span data-stu-id="17734-104">Schannel protocols require credentials to authenticate servers and optionally, clients.</span></span> <span data-ttu-id="17734-105">Проверка подлинности сервера, где сервер предоставляет клиенту подтверждение своего удостоверения, требует [*протоколов безопасности*](../secgloss/s-gly.md)SChannel.</span><span class="sxs-lookup"><span data-stu-id="17734-105">Server authentication, where the server provides proof of its identity to the client, is required by the Schannel [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="17734-106">Проверка подлинности клиента может быть запрошена сервером в любое время.</span><span class="sxs-lookup"><span data-stu-id="17734-106">Client authentication may be requested by the server at any time.</span></span>

<span data-ttu-id="17734-107">Учетные данные Schannel — это сертификаты [*X. 509*](../secgloss/x-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="17734-107">Schannel credentials are [*X.509*](../secgloss/x-gly.md) certificates.</span></span> <span data-ttu-id="17734-108">Сведения об [*открытых*](../secgloss/p-gly.md) и [*закрытых ключах*](../secgloss/p-gly.md) из сертификатов используются для проверки подлинности сервера и, при необходимости, клиента.</span><span class="sxs-lookup"><span data-stu-id="17734-108">[*Public*](../secgloss/p-gly.md) and [*private key*](../secgloss/p-gly.md) information from certificates is used to authenticate the server and optionally, the client.</span></span> <span data-ttu-id="17734-109">Эти ключи также используются для обеспечения [*целостности*](../secgloss/i-gly.md) сообщений, когда клиент и сервер обмениваются данными, необходимыми для создания и обмена [*ключами сеанса*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="17734-109">These keys are also used to provide message [*integrity*](../secgloss/i-gly.md) while client and server exchange the information required to generate and exchange [*session keys*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="17734-110">Сведения о программировании см. в разделе [Получение учетных данных SChannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="17734-110">For programming information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
