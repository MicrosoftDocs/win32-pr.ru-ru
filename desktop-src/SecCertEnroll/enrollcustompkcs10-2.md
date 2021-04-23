---
description: Создает пользовательский запрос PKCS \# 10 и пытается зарегистрировать его в центре сертификации (ЦС) предприятия.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682898"
---
# <a name="enrollcustompkcs10_2"></a><span data-ttu-id="e27b8-103">enrollCustomPKCS10 \_ 2</span><span class="sxs-lookup"><span data-stu-id="e27b8-103">enrollCustomPKCS10\_2</span></span>

<span data-ttu-id="e27b8-104">Пример enrollCustomPKCS10 \_ 2 создает пользовательский \# запрос PKCS 10 и пытается зарегистрировать его в [*центре сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС) предприятия.</span><span class="sxs-lookup"><span data-stu-id="e27b8-104">The enrollCustomPKCS10\_2 sample creates a custom PKCS \#10 request and attempts to enroll it in an enterprise [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span>

## <a name="location"></a><span data-ttu-id="e27b8-105">Расположение</span><span class="sxs-lookup"><span data-stu-id="e27b8-105">Location</span></span>

<span data-ttu-id="e27b8-106">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот пример устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples Security SSL \\ \\ Certificate \\ \\ enrollCustomPKCS10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="e27b8-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomPKCS10\_2 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="e27b8-107">Разговор</span><span class="sxs-lookup"><span data-stu-id="e27b8-107">Discussion</span></span>

<span data-ttu-id="e27b8-108">Пример enrollCustomPKCS10 \_ 2:</span><span class="sxs-lookup"><span data-stu-id="e27b8-108">The enrollCustomPKCS10\_2 sample:</span></span>

1.  <span data-ttu-id="e27b8-109">Обрабатывает аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="e27b8-109">Processes the command line arguments.</span></span> <span data-ttu-id="e27b8-110">Командная строка должна содержать имя шаблона и имя поставщика служб шифрования.</span><span class="sxs-lookup"><span data-stu-id="e27b8-110">The command line should contain the name of a template and the name of a cryptographic provider.</span></span>
2.  <span data-ttu-id="e27b8-111">Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) и инициализирует его с помощью имени шаблона, указанного в командной строке.</span><span class="sxs-lookup"><span data-stu-id="e27b8-111">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the name of the template specified on the command line.</span></span>
3.  <span data-ttu-id="e27b8-112">Получает [*запрос сертификата*](/windows/desktop/SecGloss/c-gly) из объекта регистрации.</span><span class="sxs-lookup"><span data-stu-id="e27b8-112">Retrieves the [*certificate request*](/windows/desktop/SecGloss/c-gly) from the enrollment object.</span></span>
4.  <span data-ttu-id="e27b8-113">Извлекает \# из объекта запроса сертификата самый внутренний запрос PKCS 10, полученный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="e27b8-113">Retrieves the innermost PKCS\#10 request from the certificate request object obtained in step 3.</span></span>
5.  <span data-ttu-id="e27b8-114">Извлекает [*закрытый ключ*](/windows/desktop/SecGloss/p-gly) из \# запроса PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="e27b8-114">Retrieves a [*private key*](/windows/desktop/SecGloss/p-gly) from the PKCS\#10 request.</span></span>
6.  <span data-ttu-id="e27b8-115">Создает коллекцию [**икспинформатионс**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) и добавляет доступные в нее поставщики служб шифрования, а затем извлекает объект [**икспстатус**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) для поставщика, указанного в командной строке.</span><span class="sxs-lookup"><span data-stu-id="e27b8-115">Creates an [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) collection and adds the available cryptographic providers to the collection and then retrieves an [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) object for the provider specified on the command line.</span></span>
7.  <span data-ttu-id="e27b8-116">Задает объект состояния для закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="e27b8-116">Sets the status object on the private key.</span></span>
8.  <span data-ttu-id="e27b8-117">Пытается зарегистрировать [*запрос на сертификат*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="e27b8-117">Attempts to enroll the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e27b8-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e27b8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e27b8-119">\#Запрос PKCS 10</span><span class="sxs-lookup"><span data-stu-id="e27b8-119">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="e27b8-120">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="e27b8-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
