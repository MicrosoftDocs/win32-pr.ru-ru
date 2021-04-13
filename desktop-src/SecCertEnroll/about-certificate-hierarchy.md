---
description: По мере увеличения числа выданных сертификатов в инфраструктуре открытых ключей (PKI) может оказаться затруднительным, чтобы один центр сертификации (CA) мог эффективно отразить выданные сертификаты.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Иерархия сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05c4ed9a69ff96ec0904e658444d6a32b65ed82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568299"
---
# <a name="certificate-hierarchy"></a><span data-ttu-id="b5ae6-103">Иерархия сертификатов</span><span class="sxs-lookup"><span data-stu-id="b5ae6-103">Certificate Hierarchy</span></span>

<span data-ttu-id="b5ae6-104">По мере увеличения числа выданных сертификатов в инфраструктуре открытых ключей (PKI) может оказаться затруднительным, чтобы один центр сертификации (CA) мог эффективно отразить выданные сертификаты.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-104">As the number of issued certificates in a public key infrastructure (PKI) increases, it can become difficult for a single certification authority (CA) to effectively track the certificates it has issued.</span></span> <span data-ttu-id="b5ae6-105">Один из способов решения этой проблемы — создать иерархию сертификатов, в которой ЦС делегирует полномочия выдавать сертификаты подчиненным органам, которые, в свою очередь, могут делегировать полномочия своим подчиненным пользователям.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-105">One way to address this is to create a certificate hierarchy in which the CA delegates the authority to issue certificates to subordinate authorities which can, in turn, delegate authority to their subordinates.</span></span> <span data-ttu-id="b5ae6-106">Каждый ЦС делегирует полномочия, выдавая сертификат ЦС подчиненному.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-106">Each CA delegates authority by issuing a CA certificate to a subordinate.</span></span> <span data-ttu-id="b5ae6-107">Первоначальный ЦС в цепочке называется корнем, и не требуется, чтобы сущность установила отношения доверия с любым центром сертификации, который находится в [цепочке сертификатов](about-certificate-chain.md) , отличной от той, в которой находится сущность.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-107">The initial CA in the chain is called the root, and it is not necessary for an entity to establish trust with any CA that resides on a different [Certificate Chain](about-certificate-chain.md) from that on which the entity resides.</span></span>

<span data-ttu-id="b5ae6-108">На следующем рисунке показана иерархия сертификатов, состоящие из одного корневого центра сертификации, двух центров сертификации, подчиненных корневому центру (один для отдела маркетинга, а другой — для отдела производства) и центров сертификации, подчиненных этим.</span><span class="sxs-lookup"><span data-stu-id="b5ae6-108">The following illustration shows a certificate hierarchy made up of one root CA, two CAs subordinate to the root (one for the marketing department and one for the manufacturing department), and CAs that are subordinate to these.</span></span>

![схема иерархии сертификатов](images/certificate-hierarchy.png)

## <a name="related-topics"></a><span data-ttu-id="b5ae6-110">См. также</span><span class="sxs-lookup"><span data-stu-id="b5ae6-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5ae6-111">Модели доверия</span><span class="sxs-lookup"><span data-stu-id="b5ae6-111">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



