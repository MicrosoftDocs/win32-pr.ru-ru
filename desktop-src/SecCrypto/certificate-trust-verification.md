---
description: Между получателем подписанного сообщения и подписавшимся сообщением должно существовать отношение доверия.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Проверка доверия сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b711e0a86dcc5ae9cdedea278d6a3a698dfd633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684004"
---
# <a name="certificate-trust-verification"></a><span data-ttu-id="8b68a-103">Проверка доверия сертификата</span><span class="sxs-lookup"><span data-stu-id="8b68a-103">Certificate Trust Verification</span></span>

<span data-ttu-id="8b68a-104">Между получателем подписанного сообщения и подписавшимся сообщением должно существовать отношение доверия.</span><span class="sxs-lookup"><span data-stu-id="8b68a-104">A trust must exist between the recipient of a signed message and the signer of the message.</span></span> <span data-ttu-id="8b68a-105">Одним из способов установки этого доверия является [*сертификат*](../secgloss/c-gly.md), электронный документ, подтверждающий, что субъекты или лица являются сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="8b68a-105">One method of establishing this trust is through a [*certificate*](../secgloss/c-gly.md), an electronic document verifying that entities or persons are who they claim to be.</span></span> <span data-ttu-id="8b68a-106">Сертификат выдается в сущность третьим лицом, которому доверяет обе стороны.</span><span class="sxs-lookup"><span data-stu-id="8b68a-106">A certificate is issued to an entity by a third party that is trusted by both of the other parties.</span></span> <span data-ttu-id="8b68a-107">Таким образом, каждый получатель подписанного сообщения принимает решение о том, заслуживает ли издатель сертификата подписавшего.</span><span class="sxs-lookup"><span data-stu-id="8b68a-107">So, each recipient of a signed message decides if the issuer of the signer's certificate is trustworthy.</span></span> <span data-ttu-id="8b68a-108">[*CryptoAPI*](../secgloss/c-gly.md) реализовал методологию, позволяющую разработчикам приложений создавать приложения, которые автоматически проверяют сертификаты по стандартному списку доверенных сертификатов или [*корней*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8b68a-108">[*CryptoAPI*](../secgloss/c-gly.md) has implemented a methodology to allow application developers to create applications that automatically verify certificates against a predefined list of trusted certificates or [*roots*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="8b68a-109">Этот список доверенных сущностей (называемых субъектами) называется [*списком доверия сертификатов*](../secgloss/c-gly.md) (CTL).</span><span class="sxs-lookup"><span data-stu-id="8b68a-109">This list of trusted entities (called subjects) is called a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

<span data-ttu-id="8b68a-110">В следующем примере использования списка доверия сертификатов предполагается, что администратор интрасети (внутренней сети) хочет контролировать, какие внешние источники являются доверенными.</span><span class="sxs-lookup"><span data-stu-id="8b68a-110">The following example of using a CTL involves an intranet (intra-company network) administrator who wants to control just which outside sources are trusted.</span></span> <span data-ttu-id="8b68a-111">В этом случае администратор может создать список доверенных сертификатов или корней, подписать его и сделать список доступным для всех клиентов в сети в виде списка доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="8b68a-111">In this case, the administrator can create a list of trusted certificates or roots, sign it, and make the list available to all clients on the network in the form of a CTL.</span></span> <span data-ttu-id="8b68a-112">Приложение, предназначенное для использования этой функции CryptoAPI, будет принимать только подписанные сообщения или загруженное программное обеспечение, подписанное сущностями в списке.</span><span class="sxs-lookup"><span data-stu-id="8b68a-112">An application designed to use this CryptoAPI functionality would then only accept signed messages or downloaded software that was signed by entities on the list.</span></span>

<span data-ttu-id="8b68a-113">Список этих функций см. в разделе [функции проверки сертификатов](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="8b68a-113">For a list of these functions, see [Certificate Verification Functions](cryptography-functions.md).</span></span>

 

 
