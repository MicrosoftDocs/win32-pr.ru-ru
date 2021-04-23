---
description: Службы сертификатов поддерживают иерархии центров сертификации (ЦС).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Иерархии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664113"
---
# <a name="hierarchies"></a><span data-ttu-id="eade6-103">Иерархии</span><span class="sxs-lookup"><span data-stu-id="eade6-103">Hierarchies</span></span>

<span data-ttu-id="eade6-104">Службы сертификатов поддерживают иерархии [*центров сертификации*](../secgloss/c-gly.md) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="eade6-104">Certificate Services supports [*certification authority*](../secgloss/c-gly.md) (CA) hierarchies.</span></span> <span data-ttu-id="eade6-105">[*Иерархия ЦС*](../secgloss/c-gly.md) состоит из ЦС верхнего уровня (называемого корневым ЦС) с одним или несколькими подчиненными ЦС, которые выдавали сертификаты корневым ЦС.</span><span class="sxs-lookup"><span data-stu-id="eade6-105">A [*CA hierarchy*](../secgloss/c-gly.md) consists of a top-level CA (called the Root CA) with one or more subordinate CAs which have been issued certificates by the root CA.</span></span> <span data-ttu-id="eade6-106">Возможный сценарий иерархии ЦС будет в Организации с одним корневым центром сертификации, который использовался для выдаче сертификатов нескольким подчиненным ЦС.</span><span class="sxs-lookup"><span data-stu-id="eade6-106">A possible CA hierarchy scenario would be in an organization with one root CA, which was used to issue certificates to several subordinate CAs.</span></span> <span data-ttu-id="eade6-107">Затем подчиненные ЦС могут выдавать сертификаты конечного субъекта, например сертификаты, выданные пользователю.</span><span class="sxs-lookup"><span data-stu-id="eade6-107">The subordinate CAs can then issue end-entity certificates, such as certificates issued to a user.</span></span> <span data-ttu-id="eade6-108">Сертификат пользователя будет содержать путь доверия для иерархии ЦС, в данном случае, включая сертификат для выдающего подчиненного ЦС, а также корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="eade6-108">The user's certificate will contain a trust path for the CA hierarchy, in this case, including the certificate for both the issuing subordinate CA as well as the root CA.</span></span>

 

 
