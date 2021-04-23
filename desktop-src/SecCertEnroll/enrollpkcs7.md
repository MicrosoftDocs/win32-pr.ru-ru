---
description: Создает запрос PKCS \# 7 из существующего сертификата, наследуя открытый и закрытый ключи и шаблон сертификата.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808663"
---
# <a name="enrollpkcs7"></a><span data-ttu-id="fe034-103">enrollPKCS7</span><span class="sxs-lookup"><span data-stu-id="fe034-103">enrollPKCS7</span></span>

<span data-ttu-id="fe034-104">В примере enrollPKCS7 создается запрос PKCS \# 7 из существующего сертификата путем наследования открытого и закрытого ключей и шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="fe034-104">The enrollPKCS7 sample creates a PKCS \#7 request from an existing certificate by inheriting the public and private keys and the certificate template.</span></span> <span data-ttu-id="fe034-105">Для подписания запроса используется существующий сертификат.</span><span class="sxs-lookup"><span data-stu-id="fe034-105">The existing certificate is used to sign the request.</span></span> <span data-ttu-id="fe034-106">Этот пример регистрирует пользователя в иерархии сертификатов и устанавливает ответ на сертификат.</span><span class="sxs-lookup"><span data-stu-id="fe034-106">This sample enrolls the user in a certificate hierarchy and installs the certificate response.</span></span> <span data-ttu-id="fe034-107">В примере используется существующий сертификат для регистрации и установки нового сертификата.</span><span class="sxs-lookup"><span data-stu-id="fe034-107">The sample uses an existing certificate to enroll and install a new one.</span></span> <span data-ttu-id="fe034-108">Дополнительные сведения об обновлении существующего сертификата см. в разделе [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span><span class="sxs-lookup"><span data-stu-id="fe034-108">For more information about renewing an existing certificate, see [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span></span>

## <a name="location"></a><span data-ttu-id="fe034-109">Расположение</span><span class="sxs-lookup"><span data-stu-id="fe034-109">Location</span></span>

<span data-ttu-id="fe034-110">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ enrollPKCS7.</span><span class="sxs-lookup"><span data-stu-id="fe034-110">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="fe034-111">Разговор</span><span class="sxs-lookup"><span data-stu-id="fe034-111">Discussion</span></span>

<span data-ttu-id="fe034-112">Пример enrollPKCS7:</span><span class="sxs-lookup"><span data-stu-id="fe034-112">The enrollPKCS7 sample:</span></span>

1.  <span data-ttu-id="fe034-113">Обрабатывает аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="fe034-113">Processes the command line arguments.</span></span> <span data-ttu-id="fe034-114">Командная строка должна содержать имя шаблона сертификата, используемого для поиска существующего сертификата.</span><span class="sxs-lookup"><span data-stu-id="fe034-114">The command line should contain the name of the certificate template used to find an existing certificate.</span></span>
2.  <span data-ttu-id="fe034-115">Извлекает существующий сертификат с использованием имени шаблона, указанного в командной строке, или, если сертификат не найден, пытается зарегистрировать новый, созданный с помощью шаблона.</span><span class="sxs-lookup"><span data-stu-id="fe034-115">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll a new one created by using the template.</span></span> <span data-ttu-id="fe034-116">Функции Финдцертбитемплате и Енроллцертбитемплате определены в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="fe034-116">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="fe034-117">Проверяет цепочку сертификатов и преобразует сертификат в **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="fe034-117">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="fe034-118">Создает объект [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) и инициализирует его с помощью существующего сертификата.</span><span class="sxs-lookup"><span data-stu-id="fe034-118">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="fe034-119">Новый \# объект запроса PKCS 7 наследует закрытые и открытые ключи и шаблон из существующего сертификата.</span><span class="sxs-lookup"><span data-stu-id="fe034-119">The new PKCS \#7 request object inherits the private and public keys and template from the existing certificate.</span></span>
5.  <span data-ttu-id="fe034-120">Создает объект [**исигнерцертификате**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , инициализирует его с помощью существующего сертификата и добавляет его в \# объект запроса PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="fe034-120">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the existing certificate, and adds it to the PKCS \#7 request object.</span></span>
6.  <span data-ttu-id="fe034-121">Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , инициализирует его с помощью \# объекта запроса PKCS 7, пытается зарегистрировать его в центре сертификации и отслеживает состояние процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="fe034-121">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="fe034-122">Функция Чеккенроллстатус определена в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="fe034-122">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe034-123">См. также</span><span class="sxs-lookup"><span data-stu-id="fe034-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe034-124">Запрос CMC</span><span class="sxs-lookup"><span data-stu-id="fe034-124">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="fe034-125">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="fe034-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



