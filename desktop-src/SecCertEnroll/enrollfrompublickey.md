---
description: Инициализирует \# объект запроса сертификата PKCS 10, заключает его в объект запроса CMC, отправляет запрос CMC в центр сертификации (ЦС) предприятия и сохраняет сертификат, возвращенный ЦС, в файле.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: енроллфромпубликкэй
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810696"
---
# <a name="enrollfrompublickey"></a><span data-ttu-id="a5f69-103">енроллфромпубликкэй</span><span class="sxs-lookup"><span data-stu-id="a5f69-103">enrollFromPublicKey</span></span>

<span data-ttu-id="a5f69-104">Пример Енроллфромпубликкэй инициализирует \# объект запроса сертификата PKCS 10, заключает его в объект запроса CMC, отправляет запрос CMC в центр сертификации предприятия (CA) и сохраняет сертификат, возвращенный ЦС, в файле.</span><span class="sxs-lookup"><span data-stu-id="a5f69-104">The enrollFromPublicKey sample initializes a PKCS \#10 certificate request object, wraps it in a CMC request object, submits the CMC request to an enterprise certification authority (CA), and saves the certificate returned by the CA in a file.</span></span>

## <a name="location"></a><span data-ttu-id="a5f69-105">Расположение</span><span class="sxs-lookup"><span data-stu-id="a5f69-105">Location</span></span>

<span data-ttu-id="a5f69-106">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ енроллфромпубликкэй.</span><span class="sxs-lookup"><span data-stu-id="a5f69-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollFromPublicKey folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="a5f69-107">Разговор</span><span class="sxs-lookup"><span data-stu-id="a5f69-107">Discussion</span></span>

<span data-ttu-id="a5f69-108">Пример Енроллфромпубликкэй:</span><span class="sxs-lookup"><span data-stu-id="a5f69-108">The enrollFromPublicKey sample:</span></span>

1.  <span data-ttu-id="a5f69-109">Обрабатывает следующие аргументы командной строки:</span><span class="sxs-lookup"><span data-stu-id="a5f69-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="a5f69-110">Имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="a5f69-110">The name of a certificate template.</span></span>
    -   <span data-ttu-id="a5f69-111">Имя файла, в котором следует сохранить установленный сертификат в виде массива байтов в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="a5f69-111">The name of a file in which to save the installed certificate as a base64-encoded byte array.</span></span>
    -   <span data-ttu-id="a5f69-112">Необязательное имя шаблона сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="a5f69-112">An optional signing certificate template name.</span></span> <span data-ttu-id="a5f69-113">Шаблон используется для создания сертификата подписи, если он отсутствует в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a5f69-113">The template is used to create a signing certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="a5f69-114">Создает объект закрытого ключа [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) и вызывает метод [**CREATE**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) для создания асимметричного закрытого ключа с использованием поставщика служб шифрования по умолчанию, размера ключа и значений [**keySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) для текущего компьютера.</span><span class="sxs-lookup"><span data-stu-id="a5f69-114">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) private key object and calls the [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) method to create an asymmetric private key using the default cryptographic provider, key size, and [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) values for the current computer.</span></span>
3.  <span data-ttu-id="a5f69-115">Возвращает часть открытого ключа объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .</span><span class="sxs-lookup"><span data-stu-id="a5f69-115">Retrieves the public key portion of the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object.</span></span>
4.  <span data-ttu-id="a5f69-116">Создает объект [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и инициализирует его с помощью шаблона, указанного в командной строке и открытом ключе.</span><span class="sxs-lookup"><span data-stu-id="a5f69-116">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the template specified on the command line and the public key.</span></span>
5.  <span data-ttu-id="a5f69-117">Создает объект [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) и инициализирует его с помощью \# объекта запроса PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="a5f69-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object.</span></span>
6.  <span data-ttu-id="a5f69-118">Извлекает существующий сертификат подписи или, если его не удается найти, создает запрос сертификата из шаблона, указанного в командной строке, и пытается его зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="a5f69-118">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="a5f69-119">Финдцертбикэйусаже определяется в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="a5f69-119">The findCertByKeyUsage is defined in enrollCommon.cpp.</span></span>
7.  <span data-ttu-id="a5f69-120">Проверяет цепочку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a5f69-120">Verifies the certificate chain.</span></span>
8.  <span data-ttu-id="a5f69-121">Создает объект [**исигнерцертификате**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , инициализирует его с помощью сертификата для подписи, получает коллекцию [**исигнерцертификатес**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) из объекта запроса CMC и добавляет объект сертификата подписи в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="a5f69-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the signing certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the signing certificate object to the collection.</span></span>
9.  <span data-ttu-id="a5f69-122">Кодирует запрос CMC с помощью [*distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (Der).</span><span class="sxs-lookup"><span data-stu-id="a5f69-122">Encodes the CMC request by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
10. <span data-ttu-id="a5f69-123">Создает объект [**ицертконфиг**](/windows/desktop/api/certcli/nn-certcli-icertconfig) и использует его для получения строки, СОДЕРЖАЩЕЙ конфигурацию ЦС.</span><span class="sxs-lookup"><span data-stu-id="a5f69-123">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
11. <span data-ttu-id="a5f69-124">Создает объект CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) и использует его вместе со строками, содержащими конфигурацию ЦС и запросом сертификата для отправки запроса в ЦС.</span><span class="sxs-lookup"><span data-stu-id="a5f69-124">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
12. <span data-ttu-id="a5f69-125">Проверяет состояние процесса регистрации и сохраняет установленный сертификат в файл.</span><span class="sxs-lookup"><span data-stu-id="a5f69-125">Checks the status of the enrollment process and saves the installed certificate to a file.</span></span> <span data-ttu-id="a5f69-126">Функция Енкодетофилев определена в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="a5f69-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5f69-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a5f69-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5f69-128">Запрос CMC</span><span class="sxs-lookup"><span data-stu-id="a5f69-128">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="a5f69-129">\#Запрос PKCS 10</span><span class="sxs-lookup"><span data-stu-id="a5f69-129">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="a5f69-130">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="a5f69-130">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
