---
description: Для создания запросов на сертификаты можно использовать следующие интерфейсы.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Интерфейсы запросов сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e18a4f8e1ce60348ffdf52afe210247f6d20a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154738"
---
# <a name="certificate-request-interfaces"></a><span data-ttu-id="c3872-103">Интерфейсы запросов сертификатов</span><span class="sxs-lookup"><span data-stu-id="c3872-103">Certificate Request Interfaces</span></span>

<span data-ttu-id="c3872-104">Для создания запросов на сертификаты можно использовать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="c3872-104">The following interfaces can be used to create certificate requests.</span></span>



| <span data-ttu-id="c3872-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="c3872-105">Interface</span></span>                                                                          | <span data-ttu-id="c3872-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c3872-106">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3872-107">**IX509CertificateRequest**</span><span class="sxs-lookup"><span data-stu-id="c3872-107">**IX509CertificateRequest**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | <span data-ttu-id="c3872-108">Представляет абстрактный интерфейс верхнего уровня для запроса сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3872-108">Represents the abstract top-level interface for a certificate request.</span></span>                                                                                        |
| [<span data-ttu-id="c3872-109">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="c3872-109">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | <span data-ttu-id="c3872-110">Позволяет создавать сертификаты напрямую, не обращаясь к центру регистрации или сертификации.</span><span class="sxs-lookup"><span data-stu-id="c3872-110">Enables you to create certificates directly without going through a registration or certification authority.</span></span>                                                  |
| [<span data-ttu-id="c3872-111">**IX509CertificateRequestCertificate2**</span><span class="sxs-lookup"><span data-stu-id="c3872-111">**IX509CertificateRequestCertificate2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | <span data-ttu-id="c3872-112">Расширяет интерфейс [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) , чтобы включить инициализацию из шаблона.</span><span class="sxs-lookup"><span data-stu-id="c3872-112">Extends the [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) interface to enable initialization from a template.</span></span>              |
| [<span data-ttu-id="c3872-113">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="c3872-113">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | <span data-ttu-id="c3872-114">Представляет запрос CMC.</span><span class="sxs-lookup"><span data-stu-id="c3872-114">Represents a CMC request.</span></span>                                                                                                                                     |
| [<span data-ttu-id="c3872-115">**IX509CertificateRequestCmc2**</span><span class="sxs-lookup"><span data-stu-id="c3872-115">**IX509CertificateRequestCmc2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | <span data-ttu-id="c3872-116">Расширяет интерфейс [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) , чтобы включить инициализацию из шаблона.</span><span class="sxs-lookup"><span data-stu-id="c3872-116">Extends the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) interface to enable initialization from a template.</span></span>                              |
| [<span data-ttu-id="c3872-117">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="c3872-117">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | <span data-ttu-id="c3872-118">Представляет запрос PKCS \# 10.</span><span class="sxs-lookup"><span data-stu-id="c3872-118">Represents a PKCS \#10 request.</span></span>                                                                                                                               |
| [<span data-ttu-id="c3872-119">**IX509CertificateRequestPkcs10V2**</span><span class="sxs-lookup"><span data-stu-id="c3872-119">**IX509CertificateRequestPkcs10V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | <span data-ttu-id="c3872-120">Расширяет интерфейс [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) , чтобы включить инициализацию из шаблона.</span><span class="sxs-lookup"><span data-stu-id="c3872-120">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface to enable initialization from a template.</span></span>                        |
| [<span data-ttu-id="c3872-121">**IX509CertificateRequestPkcs10V3**</span><span class="sxs-lookup"><span data-stu-id="c3872-121">**IX509CertificateRequestPkcs10V3**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | <span data-ttu-id="c3872-122">Расширяет интерфейс [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и добавляет свойства, обеспечивающие аттестацию сертификатов TPM.</span><span class="sxs-lookup"><span data-stu-id="c3872-122">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface and adds properties that enable TPM certificate attestation.</span></span> |
| [<span data-ttu-id="c3872-123">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="c3872-123">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | <span data-ttu-id="c3872-124">Представляет запрос PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="c3872-124">Represents a PKCS \#7 request.</span></span>                                                                                                                                |
| [<span data-ttu-id="c3872-125">**IX509CertificateRequestPkcs7V2**</span><span class="sxs-lookup"><span data-stu-id="c3872-125">**IX509CertificateRequestPkcs7V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | <span data-ttu-id="c3872-126">Расширяет интерфейс [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) , чтобы включить инициализацию из шаблона.</span><span class="sxs-lookup"><span data-stu-id="c3872-126">Extends the [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) interface to enable initialization from a template.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="c3872-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c3872-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3872-128">Интерфейсы Цертенролл</span><span class="sxs-lookup"><span data-stu-id="c3872-128">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



