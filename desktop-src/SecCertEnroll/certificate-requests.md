---
description: Пакет SDK для регистрации сертификатов можно использовать для создания запросов PKCS \# 10, PKCS \# 7, CMC и самозаверяющих сертификатов.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Запросы сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682900"
---
# <a name="certificate-requests"></a><span data-ttu-id="af8e6-103">Запросы сертификатов</span><span class="sxs-lookup"><span data-stu-id="af8e6-103">Certificate Requests</span></span>

<span data-ttu-id="af8e6-104">Пакет SDK для регистрации сертификатов можно использовать для создания запросов PKCS \# 10, PKCS \# 7, CMC и самозаверяющих сертификатов.</span><span class="sxs-lookup"><span data-stu-id="af8e6-104">The Certificate Enrollment SDK can be used to create PKCS \#10, PKCS \#7, CMC, and self-signed certificate requests.</span></span> <span data-ttu-id="af8e6-105">Каждый тип запроса представлен одним из интерфейсов, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="af8e6-105">Each type of request is represented by one of the interfaces listed in the following table.</span></span> <span data-ttu-id="af8e6-106">Все интерфейсы запроса напрямую или косвенно наследуются от интерфейса [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) .</span><span class="sxs-lookup"><span data-stu-id="af8e6-106">All request interfaces inherit directly or indirectly from the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) interface.</span></span> 

| <span data-ttu-id="af8e6-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="af8e6-107">Interface</span></span>                                                                        | <span data-ttu-id="af8e6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="af8e6-108">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af8e6-109">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="af8e6-109">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | <span data-ttu-id="af8e6-110">Представляет запрос PKCS \# 10.</span><span class="sxs-lookup"><span data-stu-id="af8e6-110">Represents a PKCS \#10 request.</span></span> <span data-ttu-id="af8e6-111">Этот интерфейс наследуется от [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="af8e6-111">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                   |
| [<span data-ttu-id="af8e6-112">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="af8e6-112">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | <span data-ttu-id="af8e6-113">Представляет запрос PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="af8e6-113">Represents a PKCS \#7 request.</span></span> <span data-ttu-id="af8e6-114">Этот интерфейс наследуется от [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="af8e6-114">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                    |
| [<span data-ttu-id="af8e6-115">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="af8e6-115">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | <span data-ttu-id="af8e6-116">Представляет самозаверяющий сертификат.</span><span class="sxs-lookup"><span data-stu-id="af8e6-116">Represents a self-signed certificate.</span></span> <span data-ttu-id="af8e6-117">Этот интерфейс наследуется от [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span><span class="sxs-lookup"><span data-stu-id="af8e6-117">This interface inherits from [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span></span> |
| [<span data-ttu-id="af8e6-118">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="af8e6-118">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | <span data-ttu-id="af8e6-119">Представляет запрос CMC.</span><span class="sxs-lookup"><span data-stu-id="af8e6-119">Represents a CMC request.</span></span> <span data-ttu-id="af8e6-120">Этот интерфейс наследуется от [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span><span class="sxs-lookup"><span data-stu-id="af8e6-120">This interface inherits from [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span></span>               |



 

<span data-ttu-id="af8e6-121">На следующем рисунке показана структура наследования объектов Request, поддерживаемых API регистрации сертификатов.</span><span class="sxs-lookup"><span data-stu-id="af8e6-121">The following illustration shows the inheritance structure of the request objects supported by the Certificate Enrollment API.</span></span> <span data-ttu-id="af8e6-122">Объект [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) напрямую или косвенно выступает в качестве базового класса для всех доступных объектов запроса.</span><span class="sxs-lookup"><span data-stu-id="af8e6-122">An [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object serves, directly or indirectly, as the base class for all of the available request objects.</span></span>

![Структура наследования интерфейсов запросов](images/certificate-request-inheritance.png)

<span data-ttu-id="af8e6-124">Независимо от типа запрос на сертификат содержит сведения о субъекте, который делает запрос, Открытый ключ субъекта, набор атрибутов, набор расширений X. 509 версии 3 (которые могут быть отправлены как часть атрибутов) и подпись.</span><span class="sxs-lookup"><span data-stu-id="af8e6-124">Regardless of type, a certificate request contains information about the subject making the request, the subject's public key, a set of attributes, a set of X.509 version 3 extensions (which may be submitted as part of the attributes), and a signature.</span></span> <span data-ttu-id="af8e6-125">Эти проблемы решаются в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="af8e6-125">These issues are addressed by the following topics:</span></span>

-   [<span data-ttu-id="af8e6-126">Имена субъектов</span><span class="sxs-lookup"><span data-stu-id="af8e6-126">Subject Names</span></span>](subject-names.md)
-   [<span data-ttu-id="af8e6-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="af8e6-127">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="af8e6-128">Расширения</span><span class="sxs-lookup"><span data-stu-id="af8e6-128">Extensions</span></span>](extensions.md)

## <a name="related-topics"></a><span data-ttu-id="af8e6-129">См. также</span><span class="sxs-lookup"><span data-stu-id="af8e6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af8e6-130">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="af8e6-130">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[<span data-ttu-id="af8e6-131">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="af8e6-131">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[<span data-ttu-id="af8e6-132">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="af8e6-132">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[<span data-ttu-id="af8e6-133">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="af8e6-133">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



