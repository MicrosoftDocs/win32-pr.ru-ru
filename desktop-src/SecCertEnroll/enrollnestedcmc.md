---
description: Считывает существующий запрос сертификата CMC из файла, заключает его в другой запрос CMC, подписывает этот внешний запрос, отправляет его в центр сертификации (ЦС) и сохраняет ответ сертификата из ЦС в файл.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: енроллнестедкмк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1df25a1bc7f6ce16a67f66ff58dc371a526813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262883"
---
# <a name="enrollnestedcmc"></a><span data-ttu-id="c2b4f-103">енроллнестедкмк</span><span class="sxs-lookup"><span data-stu-id="c2b4f-103">enrollNestedCMC</span></span>

<span data-ttu-id="c2b4f-104">Пример Енроллнестедкмк считывает существующий запрос сертификата CMC из файла, заключает его в другой запрос CMC, подписывает этот внешний запрос, отправляет его в центр сертификации (ЦС) и сохраняет ответ сертификата из ЦС в файл.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-104">The enrollNestedCMC sample reads an existing CMC certificate request from a file, wraps it in another CMC request, signs this outer request, submits it to a certification authority (CA), and saves the certificate response from the CA to a file.</span></span>

## <a name="location"></a><span data-ttu-id="c2b4f-105">Расположение</span><span class="sxs-lookup"><span data-stu-id="c2b4f-105">Location</span></span>

<span data-ttu-id="c2b4f-106">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ пакетов SDK Microsoft \\ Windows \\ v 7.0 \\ Samples \\ Certificate енроллнестедкмк сертификата \\ X509 \\ .</span><span class="sxs-lookup"><span data-stu-id="c2b4f-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\VC\\enrollNestedCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="c2b4f-107">Разговор</span><span class="sxs-lookup"><span data-stu-id="c2b4f-107">Discussion</span></span>

<span data-ttu-id="c2b4f-108">Пример Енроллнестедкмк:</span><span class="sxs-lookup"><span data-stu-id="c2b4f-108">The enrollNestedCMC sample:</span></span>

1.  <span data-ttu-id="c2b4f-109">Обрабатывает следующие аргументы командной строки:</span><span class="sxs-lookup"><span data-stu-id="c2b4f-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="c2b4f-110">Имя входного файла.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-110">The name of the input file.</span></span>
    -   <span data-ttu-id="c2b4f-111">Имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-111">The name of the output file.</span></span>
    -   <span data-ttu-id="c2b4f-112">Необязательный шаблон запроса.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-112">An optional request template.</span></span>
2.  <span data-ttu-id="c2b4f-113">Считывает существующий запрос CMC из файла в виде массива байтов с base63 кодировкой, преобразует массив байтов в **BSTR**, создает объект [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) и использует **BSTR** для инициализации объекта запроса.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-113">Reads an existing CMC request from a file as a base63-encoded byte array, converts the byte array to a **BSTR**, creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object, and uses the **BSTR** to initialize the request object.</span></span> <span data-ttu-id="c2b4f-114">Инициализированный объект станет внутренним запросом.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-114">The initialized object becomes the inner request.</span></span>
3.  <span data-ttu-id="c2b4f-115">Использует объект внутреннего запроса, созданный и инициализированный на предыдущем шаге, для инициализации другого запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-115">Uses the inner request object created and initialized in the preceding step to initialize another CMC request.</span></span>
4.  <span data-ttu-id="c2b4f-116">Извлекает существующий сертификат подписи или, если его не удается найти, создает запрос сертификата из шаблона, указанного в командной строке, и пытается его зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-116">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="c2b4f-117">Функции Финдцертбитемплате и Енроллцертбитемплате определены в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-117">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
5.  <span data-ttu-id="c2b4f-118">Извлекает коллекцию [**исигнерцертификатес**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) из внешнего запроса CMC, создает новый объект [**исигнерцертификате**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , инициализирует его, используя полученный сертификат подписи, и добавляет его в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-118">Retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the outer CMC request, creates a new [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the retrieved signing certificate, and adds it to the collection.</span></span>
6.  <span data-ttu-id="c2b4f-119">Кодирует запрос CMC с помощью Distinguished Encoding Rules (DER) и получает запрос в виде **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-119">Encodes the CMC request by using Distinguished Encoding Rules (DER) and retrieves the request as a **BSTR**.</span></span>
7.  <span data-ttu-id="c2b4f-120">Создает объект [**ицертконфиг**](/windows/desktop/api/certcli/nn-certcli-icertconfig) и использует его для получения строки, СОДЕРЖАЩЕЙ конфигурацию ЦС.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-120">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
8.  <span data-ttu-id="c2b4f-121">Создает объект CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) и использует его вместе со строками, содержащими конфигурацию ЦС и запросом сертификата для отправки запроса в ЦС.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-121">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
9.  <span data-ttu-id="c2b4f-122">Проверяет состояние процесса регистрации и сохраняет ответ сертификата из ЦС в файл.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-122">Checks the status of the enrollment process and saves the certificate response from the CA to a file.</span></span> <span data-ttu-id="c2b4f-123">Функция Енкодетофилев определена в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="c2b4f-123">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2b4f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c2b4f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2b4f-125">Запрос CMC</span><span class="sxs-lookup"><span data-stu-id="c2b4f-125">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="c2b4f-126">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="c2b4f-126">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
