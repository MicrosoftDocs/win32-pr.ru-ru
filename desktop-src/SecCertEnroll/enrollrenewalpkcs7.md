---
description: Создает \# объект запроса PKCS 7 для продления существующего сертификата. Объект запроса использует новую пару ключей, но удерживает поставщик служб шифрования, связанный с обновляемым сертификатом.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545879"
---
# <a name="enrollrenewalpkcs7"></a><span data-ttu-id="6e789-104">enrollRenewalPKCS7</span><span class="sxs-lookup"><span data-stu-id="6e789-104">enrollRenewalPKCS7</span></span>

<span data-ttu-id="6e789-105">Пример enrollRenewalPKCS7 создает \# объект запроса PKCS 7 для продления существующего сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e789-105">The enrollRenewalPKCS7 sample creates a PKCS \#7 request object to renew an existing certificate.</span></span> <span data-ttu-id="6e789-106">Объект запроса использует новую пару ключей, но удерживает поставщик служб шифрования, связанный с обновляемым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="6e789-106">The request object uses a new key pair but retains the cryptographic provider associated with the certificate being renewed.</span></span>

## <a name="location"></a><span data-ttu-id="6e789-107">Расположение</span><span class="sxs-lookup"><span data-stu-id="6e789-107">Location</span></span>

<span data-ttu-id="6e789-108">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="6e789-108">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollRenewalPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="6e789-109">Разговор</span><span class="sxs-lookup"><span data-stu-id="6e789-109">Discussion</span></span>

<span data-ttu-id="6e789-110">Пример enrollRenewalPKCS7:</span><span class="sxs-lookup"><span data-stu-id="6e789-110">The enrollRenewalPKCS7 sample:</span></span>

1.  <span data-ttu-id="6e789-111">Обрабатывает аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="6e789-111">Processes the command line arguments.</span></span> <span data-ttu-id="6e789-112">Командная строка должна содержать имя шаблона, используемого для создания запроса на сертификат.</span><span class="sxs-lookup"><span data-stu-id="6e789-112">The command line should contain the name of the template used to create the certificate request.</span></span>
2.  <span data-ttu-id="6e789-113">Извлекает существующий сертификат с использованием имени шаблона, указанного в командной строке, или, если сертификат не найден, пытается зарегистрировать его с помощью шаблона.</span><span class="sxs-lookup"><span data-stu-id="6e789-113">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll one by using the template.</span></span> <span data-ttu-id="6e789-114">Функции Финдцертбитемплате и Енроллцертбитемплате определены в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="6e789-114">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="6e789-115">Проверяет цепочку сертификатов и преобразует сертификат в **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="6e789-115">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="6e789-116">Создает объект [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) и инициализирует его с помощью существующего сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e789-116">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="6e789-117">Поскольку параметр *инхеритоптионс* имеет значение инхеритдефаулт, для запроса создается новая пара ключей, но используется поставщик служб шифрования в существующем сертификате.</span><span class="sxs-lookup"><span data-stu-id="6e789-117">Because the *inheritOptions* parameter is set to InheritDefault, a new key pair is created for the request but the cryptographic provider in the existing certificate is used.</span></span> <span data-ttu-id="6e789-118">Дополнительные сведения см. в описании метода [**инитиализефромцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .</span><span class="sxs-lookup"><span data-stu-id="6e789-118">For more information, see the [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) method.</span></span>
5.  <span data-ttu-id="6e789-119">Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , инициализирует его с помощью \# объекта запроса PKCS 7, пытается зарегистрировать его в центре сертификации и отслеживает состояние процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="6e789-119">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="6e789-120">Функция Чеккенроллстатус определена в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="6e789-120">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e789-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6e789-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e789-122">Запрос CMC</span><span class="sxs-lookup"><span data-stu-id="6e789-122">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="6e789-123">\#Запрос на продление PKCS 7</span><span class="sxs-lookup"><span data-stu-id="6e789-123">PKCS \#7 Renewal Request</span></span>](pkcs--7--renewal-request.md)
</dt> <dt>

[<span data-ttu-id="6e789-124">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="6e789-124">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



