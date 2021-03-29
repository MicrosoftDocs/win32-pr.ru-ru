---
description: Создает запрос на сертификат CMC и регистрирует компьютер в иерархии сертификатов.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: енроллкустомкмк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810702"
---
# <a name="enrollcustomcmc"></a><span data-ttu-id="297f5-103">енроллкустомкмк</span><span class="sxs-lookup"><span data-stu-id="297f5-103">enrollCustomCMC</span></span>

<span data-ttu-id="297f5-104">Пример Енроллкустомкмк создает запрос на сертификат CMC и регистрирует компьютер в иерархии сертификатов.</span><span class="sxs-lookup"><span data-stu-id="297f5-104">The enrollCustomCMC sample creates a CMC certificate request and enrolls a computer in a certificate hierarchy.</span></span>

## <a name="location"></a><span data-ttu-id="297f5-105">Расположение</span><span class="sxs-lookup"><span data-stu-id="297f5-105">Location</span></span>

<span data-ttu-id="297f5-106">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ енроллкустомкмк.</span><span class="sxs-lookup"><span data-stu-id="297f5-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="297f5-107">Разговор</span><span class="sxs-lookup"><span data-stu-id="297f5-107">Discussion</span></span>

<span data-ttu-id="297f5-108">Пример Енроллкустомкмк:</span><span class="sxs-lookup"><span data-stu-id="297f5-108">The enrollCustomCMC sample:</span></span>

1.  <span data-ttu-id="297f5-109">Обрабатывает следующие аргументы командной строки:</span><span class="sxs-lookup"><span data-stu-id="297f5-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="297f5-110">Пользовательская пара "имя-значение", добавляемая в запрос сертификата.</span><span class="sxs-lookup"><span data-stu-id="297f5-110">A custom name/value pair to add to the certificate request.</span></span>
    -   <span data-ttu-id="297f5-111">Альтернативное имя субъекта.</span><span class="sxs-lookup"><span data-stu-id="297f5-111">An alternative subject name.</span></span>
    -   <span data-ttu-id="297f5-112">Идентификатор объекта (OID) для расширения расширенного использования ключа (EKU).</span><span class="sxs-lookup"><span data-stu-id="297f5-112">An object identifier (OID) for the Enhanced Key Usage (EKU) extension.</span></span>
2.  <span data-ttu-id="297f5-113">Создает объект запроса [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и инициализирует его с помощью контекста компьютера.</span><span class="sxs-lookup"><span data-stu-id="297f5-113">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) request object and initializes it by using the computer context.</span></span>
3.  <span data-ttu-id="297f5-114">Использует запрос PKCS \# 10 для инициализации объекта [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="297f5-114">Uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
4.  <span data-ttu-id="297f5-115">Создает объект [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) , используя идентификатор объекта, указанный в командной строке, и добавляет его в коллекцию Extensions для запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="297f5-115">Creates an [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) object by using the OID specified on the command line and adds it to the extensions collection for the CMC request.</span></span>
5.  <span data-ttu-id="297f5-116">Создает объект [**иалтернативенаме**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) , используя имя, указанное в командной строке, добавляет его в коллекцию [**иалтернативенамес**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , использует коллекцию для инициализации расширения [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) и добавляет его в коллекцию Extensions для запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="297f5-116">Creates [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) object by using the name specified on the command line, adds it to the [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) collection, uses the collection to initialize an [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) extension and adds this to the extensions collection for the CMC request.</span></span>
6.  <span data-ttu-id="297f5-117">Создает объект [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) , используя имя и значение, указанные в командной строке, и добавляет его в коллекцию [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="297f5-117">Creates an [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) object by using the name and value specified on the command line, and adds it to the [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection on the CMC request.</span></span>
7.  <span data-ttu-id="297f5-118">Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , инициализирует его с помощью объекта запроса CMC и получает строку, содержащую запрос в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="297f5-118">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request object, and retrieves a string that contains a base64-encoded request.</span></span>
8.  <span data-ttu-id="297f5-119">Создает объект [**ицертконфиг**](/windows/desktop/api/certcli/nn-certcli-icertconfig) и использует его для получения строки, СОДЕРЖАЩЕЙ конфигурацию ЦС.</span><span class="sxs-lookup"><span data-stu-id="297f5-119">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
9.  <span data-ttu-id="297f5-120">Создает объект CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) и использует его вместе со строками, содержащими конфигурацию ЦС и запросом сертификата для отправки запроса в ЦС.</span><span class="sxs-lookup"><span data-stu-id="297f5-120">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
10. <span data-ttu-id="297f5-121">Проверяет состояние отправки и, при успешном выполнении, устанавливает сертификат в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="297f5-121">Checks the submission status and, if successful, installs the certificate to the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="297f5-122">См. также</span><span class="sxs-lookup"><span data-stu-id="297f5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="297f5-123">Запрос CMC</span><span class="sxs-lookup"><span data-stu-id="297f5-123">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="297f5-124">\#Запрос PKCS 10</span><span class="sxs-lookup"><span data-stu-id="297f5-124">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="297f5-125">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="297f5-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
