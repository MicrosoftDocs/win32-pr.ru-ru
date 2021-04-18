---
description: Несколько функций добавляют контекст сертификата или ссылку на контекст в \[ пакет средств разработки для платформы магазина (SDK) \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Работа с сертификатами в хранилищах сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347662"
---
# <a name="working-with-certificates-in-certificate-stores"></a><span data-ttu-id="3e2df-103">Работа с сертификатами в хранилищах сертификатов</span><span class="sxs-lookup"><span data-stu-id="3e2df-103">Working with Certificates in Certificate Stores</span></span>

<span data-ttu-id="3e2df-104">Несколько функций добавляют контекст сертификата или ссылку на контекст в хранилище.</span><span class="sxs-lookup"><span data-stu-id="3e2df-104">Several functions add a certificate context or a link to a context to a store.</span></span>

<span data-ttu-id="3e2df-105">Для сертификатов, которые уже находятся в форме контекста сертификата:</span><span class="sxs-lookup"><span data-stu-id="3e2df-105">For certificates already in certificate context form:</span></span>

-   [<span data-ttu-id="3e2df-106">**цертаддцертификатеконтексттосторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-106">**CertAddCertificateContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [<span data-ttu-id="3e2df-107">**цертаддкрлконтексттосторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-107">**CertAddCRLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [<span data-ttu-id="3e2df-108">**цертаддктлконтексттосторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-108">**CertAddCTLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [<span data-ttu-id="3e2df-109">**цертаддцертификателинктосторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-109">**CertAddCertificateLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [<span data-ttu-id="3e2df-110">**цертаддкрллинктосторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-110">**CertAddCRLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [<span data-ttu-id="3e2df-111">**цертаддктллинктосторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-111">**CertAddCTLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

<span data-ttu-id="3e2df-112">Для сертификатов в кодированной форме, но не полных контекстов сертификатов:</span><span class="sxs-lookup"><span data-stu-id="3e2df-112">For certificates that are in encoded form but not full certificate contexts:</span></span>

-   [<span data-ttu-id="3e2df-113">**CertAddEncodedCertificateToStore**</span><span class="sxs-lookup"><span data-stu-id="3e2df-113">**CertAddEncodedCertificateToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [<span data-ttu-id="3e2df-114">**цертадденкодедкрлтосторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-114">**CertAddEncodedCRLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [<span data-ttu-id="3e2df-115">**цертадденкодедктлтосторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-115">**CertAddEncodedCTLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

<span data-ttu-id="3e2df-116">Следующие функции удаляют сертификат, список отзыва сертификатов или CTL из хранилища, уменьшая число ссылок на единицу.</span><span class="sxs-lookup"><span data-stu-id="3e2df-116">The following functions delete a certificate, CRL, or CTL from a store by decrementing its reference count by one.</span></span> <span data-ttu-id="3e2df-117">Если это приводит к тому, что счетчик ссылок будет обнулен, то память, используемая для хранения сертификата, списка отзыва сертификатов или CTL, освобождается.</span><span class="sxs-lookup"><span data-stu-id="3e2df-117">If this causes the reference count to become zero, the memory used to store the certificate, CRL, or CTL is freed.</span></span>

-   [<span data-ttu-id="3e2df-118">**цертделетецертификатефромсторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-118">**CertDeleteCertificateFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [<span data-ttu-id="3e2df-119">**цертделетекрлфромсторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-119">**CertDeleteCRLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [<span data-ttu-id="3e2df-120">**цертделетектлфромсторе**</span><span class="sxs-lookup"><span data-stu-id="3e2df-120">**CertDeleteCTLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



