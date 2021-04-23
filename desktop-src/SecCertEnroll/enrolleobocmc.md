---
description: Создает запрос на сертификат CMC от имени другого пользователя и регистрирует пользователя в иерархии сертификатов.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: енроллеобокмк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542682"
---
# <a name="enrolleobocmc"></a><span data-ttu-id="c248d-103">енроллеобокмк</span><span class="sxs-lookup"><span data-stu-id="c248d-103">enrollEOBOCMC</span></span>

<span data-ttu-id="c248d-104">Пример Енроллеобокмк создает запрос сертификата CMC от имени другого пользователя и регистрирует пользователя в иерархии сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c248d-104">The enrollEOBOCMC sample creates a CMC certificate request on behalf of another user and enrolls the user in a certificate hierarchy.</span></span> <span data-ttu-id="c248d-105">Регистрация от имени другого пользователя требует, чтобы запрос сертификата был подписан с помощью сертификата агента регистрации.</span><span class="sxs-lookup"><span data-stu-id="c248d-105">Enrollment on behalf of another user requires that the certificate request be signed by using an enrollment agent certificate.</span></span>

## <a name="location"></a><span data-ttu-id="c248d-106">Расположение</span><span class="sxs-lookup"><span data-stu-id="c248d-106">Location</span></span>

<span data-ttu-id="c248d-107">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ енроллеобокмк.</span><span class="sxs-lookup"><span data-stu-id="c248d-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollEOBOCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="c248d-108">Разговор</span><span class="sxs-lookup"><span data-stu-id="c248d-108">Discussion</span></span>

<span data-ttu-id="c248d-109">Пример Енроллеобокмк:</span><span class="sxs-lookup"><span data-stu-id="c248d-109">The enrollEOBOCMC sample:</span></span>

1.  <span data-ttu-id="c248d-110">Обрабатывает следующие аргументы командной строки:</span><span class="sxs-lookup"><span data-stu-id="c248d-110">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="c248d-111">Имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="c248d-111">The name of a certificate template.</span></span>
    -   <span data-ttu-id="c248d-112">Имя пользователя, запросившего сертификат.</span><span class="sxs-lookup"><span data-stu-id="c248d-112">The name of the user requesting the certificate.</span></span>
    -   <span data-ttu-id="c248d-113">Имя файла обмена личной информацией (PFX), в котором необходимо сохранить запрос.</span><span class="sxs-lookup"><span data-stu-id="c248d-113">The name of a Personal Information Exchange (PFX) file in which to save the request.</span></span>
    -   <span data-ttu-id="c248d-114">Пароль для использования с PFX-файлом.</span><span class="sxs-lookup"><span data-stu-id="c248d-114">A password to use with the PFX file.</span></span>
    -   <span data-ttu-id="c248d-115">Необязательное имя шаблона агента регистрации.</span><span class="sxs-lookup"><span data-stu-id="c248d-115">An optional enrollment agent template name.</span></span> <span data-ttu-id="c248d-116">Шаблон используется для создания сертификата агента регистрации, если он отсутствует в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c248d-116">The template is used to create an enrollment agent certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="c248d-117">Создает объект [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) и инициализирует его с помощью шаблона сертификата, указанного в командной строке.</span><span class="sxs-lookup"><span data-stu-id="c248d-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the certificate template specified on the command line.</span></span>
3.  <span data-ttu-id="c248d-118">Добавляет имя запросившего в объект запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="c248d-118">Adds the name of the requester to the CMC request object.</span></span>
4.  <span data-ttu-id="c248d-119">Извлекает существующий сертификат агента регистрации или, если он не найден, создает запрос сертификата из шаблона агента регистрации, указанного в командной строке, и пытается его зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="c248d-119">Retrieves an existing enrollment agent certificate or, if one cannot be found, creates a certificate request from the enrollment agent template specified on the command line and attempts to enroll it.</span></span>
5.  <span data-ttu-id="c248d-120">Проверяет цепочку сертификатов, содержащую сертификат агента регистрации.</span><span class="sxs-lookup"><span data-stu-id="c248d-120">Verifies the certificate chain that contains the enrollment agent certificate.</span></span>
6.  <span data-ttu-id="c248d-121">Создает объект [**исигнерцертификате**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , инициализирует его с помощью сертификата агента регистрации, получает коллекцию [**исигнерцертификатес**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) из объекта запроса CMC и добавляет объект сертификата подписи агента регистрации в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="c248d-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the enrollment agent certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the enrollment agent signing certificate object to the collection.</span></span> <span data-ttu-id="c248d-122">Объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , который обсуждается на следующем шаге, использует сертификат для подписи запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="c248d-122">The [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object discussed in the next step uses the certificate to sign the CMC request.</span></span>
7.  <span data-ttu-id="c248d-123">Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , инициализирует его с помощью запроса CMC, пытается зарегистрировать его и проверяет ход выполнения процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="c248d-123">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, attempts to enroll it, and checks the progress of the enrollment process.</span></span>
8.  <span data-ttu-id="c248d-124">Экспортирует установленный сертификат в PFX-файл.</span><span class="sxs-lookup"><span data-stu-id="c248d-124">Exports the installed certificate to a PFX file.</span></span> <span data-ttu-id="c248d-125">Файл защищен с помощью пароля, указанного в командной строке.</span><span class="sxs-lookup"><span data-stu-id="c248d-125">The file is protected by using the password specified on the command line.</span></span> <span data-ttu-id="c248d-126">Функция Енкодетофилев определена в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="c248d-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>
9.  <span data-ttu-id="c248d-127">Удаляет сертификат из хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c248d-127">Deletes the certificate from the certificate store.</span></span> <span data-ttu-id="c248d-128">Функции, используемые в следующем примере кода, можно найти в документации по CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="c248d-128">The functions used in the following code example can be found in the CryptoAPI documentation.</span></span>
10. <span data-ttu-id="c248d-129">Удаляет закрытый ключ с компьютера.</span><span class="sxs-lookup"><span data-stu-id="c248d-129">Deletes the private key from the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c248d-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c248d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c248d-131">Запрос ЕОБО CMC</span><span class="sxs-lookup"><span data-stu-id="c248d-131">CMC EOBO Request</span></span>](cmc-eobo-request.md)
</dt> <dt>

[<span data-ttu-id="c248d-132">\#Запрос PKCS 10</span><span class="sxs-lookup"><span data-stu-id="c248d-132">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="c248d-133">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="c248d-133">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



