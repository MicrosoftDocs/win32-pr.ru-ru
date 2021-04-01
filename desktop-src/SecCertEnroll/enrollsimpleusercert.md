---
description: Регистрация конечного пользователя в центре сертификации (ЦС) с помощью шаблона, имени субъекта и длины (в битах) ключа.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: енроллсимплеусерцерт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081014"
---
# <a name="enrollsimpleusercert"></a><span data-ttu-id="85d53-103">енроллсимплеусерцерт</span><span class="sxs-lookup"><span data-stu-id="85d53-103">enrollSimpleUserCert</span></span>

<span data-ttu-id="85d53-104">Пример Енроллсимплеусерцерт регистрирует конечного пользователя в центре сертификации (ЦС) с помощью шаблона, имени субъекта и длины ключа в битах.</span><span class="sxs-lookup"><span data-stu-id="85d53-104">The enrollSimpleUserCert sample enrolls an end user with a certification authority (CA) by using a template, the subject name, and the length, in bits, of the key.</span></span>

## <a name="location"></a><span data-ttu-id="85d53-105">Расположение</span><span class="sxs-lookup"><span data-stu-id="85d53-105">Location</span></span>

<span data-ttu-id="85d53-106">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows устанавливается версия C++ образца по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ енроллсимплеусерцерт.</span><span class="sxs-lookup"><span data-stu-id="85d53-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollSimpleUserCert folder.</span></span> <span data-ttu-id="85d53-107">Версия C# установлена в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 Samples, посвященной \\ \\ регистрации сертификата X509 \\ \\ енроллсимплеусерцерт CSharp.</span><span class="sxs-lookup"><span data-stu-id="85d53-107">A C# version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\CSharp\\EnrollSimpleUserCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="85d53-108">Разговор</span><span class="sxs-lookup"><span data-stu-id="85d53-108">Discussion</span></span>

<span data-ttu-id="85d53-109">Пример Енроллсимплеусерцерт:</span><span class="sxs-lookup"><span data-stu-id="85d53-109">The enrollSimpleUserCert sample:</span></span>

1.  <span data-ttu-id="85d53-110">Обрабатывает аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="85d53-110">Processes the command line arguments.</span></span> <span data-ttu-id="85d53-111">Командная строка должна содержать имя шаблона, имя субъекта и длину ключа.</span><span class="sxs-lookup"><span data-stu-id="85d53-111">The command line should contain the name of the template, the subject name, and the key length.</span></span>
2.  <span data-ttu-id="85d53-112">Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) и инициализирует его с помощью шаблона.</span><span class="sxs-lookup"><span data-stu-id="85d53-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template.</span></span>
3.  <span data-ttu-id="85d53-113">Извлекает объект запроса внутреннего сертификата из объекта регистрации и запрашивает его для объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="85d53-113">Retrieves the inner certificate request object from the enrollment object and queries it for the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span> <span data-ttu-id="85d53-114">Самый внутренний запрос всегда является \# запросом PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="85d53-114">The innermost request is always a PKCS \#10 request.</span></span>
4.  <span data-ttu-id="85d53-115">Извлекает объект [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) из \# запроса PKCS 10 и задает длину ключа, указанную в командной строке.</span><span class="sxs-lookup"><span data-stu-id="85d53-115">Retrieves the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object from the PKCS \#10 request and sets the key length specified on the command line.</span></span>
5.  <span data-ttu-id="85d53-116">Создает объект [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , использует его для кодирования имени субъекта X. 500 и добавляет имя в \# запрос PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="85d53-116">Creates an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, uses it to encode the X.500 subject name, and adds the name to the PKCS \#10 request.</span></span>
6.  <span data-ttu-id="85d53-117">Пытается зарегистрировать конечного пользователя в центре сертификации и отслеживать ход процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="85d53-117">Attempts to enroll the end user with the CA and monitors the progress of the enrollment process.</span></span> <span data-ttu-id="85d53-118">Функция Чеккенроллстатус определена в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="85d53-118">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85d53-119">См. также</span><span class="sxs-lookup"><span data-stu-id="85d53-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85d53-120">\#Запрос PKCS 10</span><span class="sxs-lookup"><span data-stu-id="85d53-120">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="85d53-121">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="85d53-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



