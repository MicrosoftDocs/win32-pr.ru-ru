---
description: Создает объект запроса CMC из внутреннего вложенного запроса PKCS \# 10.
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: креатекнгкустомкмк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342732"
---
# <a name="createcngcustomcmc"></a><span data-ttu-id="0d4a4-103">креатекнгкустомкмк</span><span class="sxs-lookup"><span data-stu-id="0d4a4-103">createCNGCustomCMC</span></span>

<span data-ttu-id="0d4a4-104">В примере Креатекнгкустомкмк создается объект запроса CMC из внутреннего вложенного запроса PKCS \# 10.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-104">The createCNGCustomCMC sample creates a CMC request object from an inner nested PKCS \#10 request.</span></span> <span data-ttu-id="0d4a4-105">Внутренний запрос создается с помощью асимметричного [*закрытого ключа*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="0d4a4-105">The inner request is created by using an asymmetric [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="0d4a4-106">Закрытый ключ создается с помощью поставщика криптографии API шифрования: следующего поколения (CNG) и алгоритма, указанного в командной строке.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-106">The private key is created by using the Cryptography API: Next Generation (CNG) cryptographic provider and the algorithm specified on the command line.</span></span> <span data-ttu-id="0d4a4-107">Для закрытого ключа также устанавливаются настраиваемые параметры, такие как экспорт политики и уровень защиты ключей.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-107">Custom options such as export policy and key protection level are also set on the private key.</span></span>

## <a name="location"></a><span data-ttu-id="0d4a4-108">Расположение</span><span class="sxs-lookup"><span data-stu-id="0d4a4-108">Location</span></span>

<span data-ttu-id="0d4a4-109">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ креатекнгкустомкмк.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-109">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\createCNGCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="0d4a4-110">Разговор</span><span class="sxs-lookup"><span data-stu-id="0d4a4-110">Discussion</span></span>

<span data-ttu-id="0d4a4-111">Пример Креатекнгкустомкмк:</span><span class="sxs-lookup"><span data-stu-id="0d4a4-111">The createCNGCustomCMC sample:</span></span>

1.  <span data-ttu-id="0d4a4-112">Обрабатывает следующие аргументы командной строки:</span><span class="sxs-lookup"><span data-stu-id="0d4a4-112">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="0d4a4-113">Имя [*поставщика служб шифрования*](/windows/desktop/SecGloss/c-gly) CNG (CSP).</span><span class="sxs-lookup"><span data-stu-id="0d4a4-113">The name of a CNG [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span>
    -   <span data-ttu-id="0d4a4-114">Имя алгоритма, используемого для создания асимметричного закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-114">The name of the algorithm used to generate an asymmetric private key.</span></span>
    -   <span data-ttu-id="0d4a4-115">Имя алгоритма, используемого для [*хэширования*](/windows/desktop/SecGloss/h-gly) [*запроса сертификата*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="0d4a4-115">The name of the algorithm used to [*hash*](/windows/desktop/SecGloss/h-gly) the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>
    -   <span data-ttu-id="0d4a4-116">Выходной файл, в котором сохраняется запрос на сертификат.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-116">An output file in which to save the certificate request.</span></span>
    -   <span data-ttu-id="0d4a4-117">Необязательная строка (Алтернатесигнатуре), если она есть, указывает, что используется дискретный, а не Объединенный алгоритм подписи.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-117">An optional string (AlternateSignature) which, if present, specifies that a discrete rather than a combined signature algorithm be used.</span></span> <span data-ttu-id="0d4a4-118">Дополнительные сведения см. в описании свойства [**алтернатесигнатуреалгорисм**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) .</span><span class="sxs-lookup"><span data-stu-id="0d4a4-118">For more information, see the [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) property.</span></span>
2.  <span data-ttu-id="0d4a4-119">Создает объект [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) и задает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="0d4a4-119">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object and sets the following properties:</span></span>
    -   [<span data-ttu-id="0d4a4-120">**легациксп**</span><span class="sxs-lookup"><span data-stu-id="0d4a4-120">**LegacyCsp**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [<span data-ttu-id="0d4a4-121">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="0d4a4-121">**ProviderName**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [<span data-ttu-id="0d4a4-122">**Алгоритм**</span><span class="sxs-lookup"><span data-stu-id="0d4a4-122">**Algorithm**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [<span data-ttu-id="0d4a4-123">**кэйпротектион**</span><span class="sxs-lookup"><span data-stu-id="0d4a4-123">**KeyProtection**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [<span data-ttu-id="0d4a4-124">**експортполици**</span><span class="sxs-lookup"><span data-stu-id="0d4a4-124">**ExportPolicy**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  <span data-ttu-id="0d4a4-125">Создает асимметричный закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-125">Creates an asymmetric private key.</span></span>
4.  <span data-ttu-id="0d4a4-126">Создает объект [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и инициализирует его с помощью закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-126">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the private key.</span></span>
5.  <span data-ttu-id="0d4a4-127">Создает объект [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) и инициализирует его с помощью \# объекта запроса PKCS 10, созданного на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-127">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object created in step 4.</span></span>
6.  <span data-ttu-id="0d4a4-128">Устанавливает для флага альтернативного алгоритма подписи значение **Variant \_ true** или **Variant \_ false** в зависимости от того, указана ли в командной строке альтернативная строка подписи.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-128">Sets the alternate signature algorithm flag to **VARIANT\_TRUE** or **VARIANT\_FALSE** depending on whether an alternate signature string is specified on the command line.</span></span> <span data-ttu-id="0d4a4-129">Дополнительные сведения см. в разделе [**алтернатесигнатуреалгорисм**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span><span class="sxs-lookup"><span data-stu-id="0d4a4-129">For more information, see [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span></span>
7.  <span data-ttu-id="0d4a4-130">Создает [*идентификатор объекта*](/windows/desktop/SecGloss/o-gly) (OID) [*алгоритма хэширования*](/windows/desktop/SecGloss/h-gly) из имени алгоритма, указанного в командной строке, и задает идентификатор объекта для объекта запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-130">Creates a [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) from the algorithm name specified on the command line and sets the OID on the CMC request object.</span></span>
8.  <span data-ttu-id="0d4a4-131">Подписывает запрос на сертификат и кодирует его с помощью [*distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (Der).</span><span class="sxs-lookup"><span data-stu-id="0d4a4-131">Signs the certificate request and encodes it by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
9.  <span data-ttu-id="0d4a4-132">Извлекает строку, содержащую закодированный запрос сертификата CMC, и сохраняет его в файл.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-132">Retrieves a string that contains the encoded CMC certificate request and saves it to a file.</span></span> <span data-ttu-id="0d4a4-133">Функция Енкодетофилев определена в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-133">The EncodeToFileW function is defined in EnrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d4a4-134">См. также</span><span class="sxs-lookup"><span data-stu-id="0d4a4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d4a4-135">Запрос CMC</span><span class="sxs-lookup"><span data-stu-id="0d4a4-135">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="0d4a4-136">\#Запрос PKCS 10</span><span class="sxs-lookup"><span data-stu-id="0d4a4-136">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="0d4a4-137">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="0d4a4-137">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> <dt>

[<span data-ttu-id="0d4a4-138">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="0d4a4-138">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
