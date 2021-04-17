---
description: Создает запрос на сертификат CMC для архивации закрытого ключа в центре сертификации (ЦС).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: енроллкэйарчивалкмк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682894"
---
# <a name="enrollkeyarchivalcmc"></a><span data-ttu-id="c01d0-103">енроллкэйарчивалкмк</span><span class="sxs-lookup"><span data-stu-id="c01d0-103">enrollKeyArchivalCMC</span></span>

<span data-ttu-id="c01d0-104">Пример Енроллкэйарчивалкмк создает запрос на сертификат CMC для архивации закрытого ключа в центре сертификации (ЦС).</span><span class="sxs-lookup"><span data-stu-id="c01d0-104">The enrollKeyArchivalCMC sample creates a CMC certificate request to archive a private key on a certification authority (CA).</span></span> <span data-ttu-id="c01d0-105">Дополнительные сведения см. в разделе [запрос на архивирование ключа CMC](cmc-key-archival-request.md).</span><span class="sxs-lookup"><span data-stu-id="c01d0-105">For more information, see [CMC Key Archival Request](cmc-key-archival-request.md).</span></span>

## <a name="location"></a><span data-ttu-id="c01d0-106">Расположение</span><span class="sxs-lookup"><span data-stu-id="c01d0-106">Location</span></span>

<span data-ttu-id="c01d0-107">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ енроллкэйарчивалкмк.</span><span class="sxs-lookup"><span data-stu-id="c01d0-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollKeyArchivalCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="c01d0-108">Разговор</span><span class="sxs-lookup"><span data-stu-id="c01d0-108">Discussion</span></span>

<span data-ttu-id="c01d0-109">Пример Енроллкэйарчивалкмк:</span><span class="sxs-lookup"><span data-stu-id="c01d0-109">The enrollKeyArchivalCMC sample:</span></span>

1.  <span data-ttu-id="c01d0-110">Обрабатывает аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="c01d0-110">Processes the command line arguments.</span></span> <span data-ttu-id="c01d0-111">Командная строка должна содержать имя шаблона сертификата, который будет использоваться для регистрации.</span><span class="sxs-lookup"><span data-stu-id="c01d0-111">The command line should contain the name of the certificate template to use for enrollment.</span></span>
2.  <span data-ttu-id="c01d0-112">Создает объект запроса сертификата [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) и инициализирует его для контекста конечного пользователя с помощью имени шаблона.</span><span class="sxs-lookup"><span data-stu-id="c01d0-112">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) certificate request object and initializes it for an end-user context by using the template name.</span></span>
3.  <span data-ttu-id="c01d0-113">Задает свойство [**арчивеприватекэй**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) для запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="c01d0-113">Sets the [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) property on the CMC request.</span></span>
4.  <span data-ttu-id="c01d0-114">Создает объект [**ицертконфиг**](/windows/desktop/api/certcli/nn-certcli-icertconfig) и использует его для получения строки, СОДЕРЖАЩЕЙ конфигурацию ЦС.</span><span class="sxs-lookup"><span data-stu-id="c01d0-114">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
5.  <span data-ttu-id="c01d0-115">Создает объект CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) и использует его для получения сертификата Exchange для центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="c01d0-115">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it to retrieve the exchange certificate for the CA.</span></span>
6.  <span data-ttu-id="c01d0-116">Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , инициализирует его с помощью запроса CMC, создает строку в кодировке Base64, содержащую запрос на архивацию ключа, и отправляет его в центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="c01d0-116">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, creates a base64 encoded string that contains the key archival request, and submits it to the CA.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c01d0-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c01d0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c01d0-118">Запрос на архивацию ключа CMC</span><span class="sxs-lookup"><span data-stu-id="c01d0-118">CMC Key Archival Request</span></span>](cmc-key-archival-request.md)
</dt> <dt>

[<span data-ttu-id="c01d0-119">Запрос CMC</span><span class="sxs-lookup"><span data-stu-id="c01d0-119">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="c01d0-120">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="c01d0-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
