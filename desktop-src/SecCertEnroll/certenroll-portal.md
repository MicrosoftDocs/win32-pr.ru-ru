---
description: Пример сертификата. Создайте приложения для сертификации API, установите SSL-сертификат, сертификат сервера, создайте сертификат на носителе, например в Интернете или интрасети, которые не являются безопасными по своей природе.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API регистрации сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541807"
---
# <a name="certificate-enrollment-api"></a><span data-ttu-id="784d1-104">API регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="784d1-104">Certificate Enrollment API</span></span>

## <a name="purpose"></a><span data-ttu-id="784d1-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="784d1-105">Purpose</span></span>

<span data-ttu-id="784d1-106">API регистрации сертификатов можно использовать для создания клиентского приложения, запрашивающего сертификат и установки ответа на сертификат.</span><span class="sxs-lookup"><span data-stu-id="784d1-106">The Certificate Enrollment API can be used to create a client application to request a certificate and install a certificate response.</span></span> <span data-ttu-id="784d1-107">Этот API реализован в CertEnroll.dll, начиная с Windows Vista; Он заменяет Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="784d1-107">This API is implemented in CertEnroll.dll beginning with Windows Vista; it replaces Xenroll.dll.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="784d1-108">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="784d1-108">Developer audience</span></span>

<span data-ttu-id="784d1-109">API регистрации сертификатов предназначен для использования разработчиками приложений, которые позволяют пользователям создавать, запрашивать и получать сертификаты на носителе, например в Интернете или интрасети, которые не являются безопасными по своей природе.</span><span class="sxs-lookup"><span data-stu-id="784d1-109">The Certificate Enrollment API is for use by developers of applications that will enable users to create, request, and retrieve certificates over media, such as the Internet or an intranet, that are not inherently secure.</span></span> <span data-ttu-id="784d1-110">Разработчики должны быть знакомы с языками программирования C и C++, моделью COM и средой программирования на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="784d1-110">Developers should be familiar with the C and C++ programming languages, the Component Object Model (COM), and the Windows-based programming environment.</span></span> <span data-ttu-id="784d1-111">Хотя это и не является обязательным, рекомендуется понимать принципы шифрования и инфраструктуры открытых ключей.</span><span class="sxs-lookup"><span data-stu-id="784d1-111">Although not required, an understanding of cryptography and public key infrastructure is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="784d1-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="784d1-112">Run-time requirements</span></span>

<span data-ttu-id="784d1-113">API регистрации сертификатов поддерживается начиная с Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="784d1-113">The Certificate Enrollment API is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="784d1-114">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="784d1-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="784d1-115">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="784d1-115">In this section</span></span>



| <span data-ttu-id="784d1-116">Раздел</span><span class="sxs-lookup"><span data-stu-id="784d1-116">Topic</span></span>                                                                                       | <span data-ttu-id="784d1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="784d1-117">Description</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="784d1-118">Сведения об API регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="784d1-118">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="784d1-119">Обсуждаются основные понятия о запросах сертификатов.</span><span class="sxs-lookup"><span data-stu-id="784d1-119">Key concepts about certificate requests are discussed.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="784d1-120">Использование API регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="784d1-120">Using the Certificate Enrollment API</span></span>](using-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="784d1-121">Использование API регистрации сертификатов для расширения возможностей Active Directory служб сертификации.</span><span class="sxs-lookup"><span data-stu-id="784d1-121">How to use the Certificate Enrollment API to extend the capabilities of Active Directory Certificate Services.</span></span><br/>                                              |
| [<span data-ttu-id="784d1-122">Справочник по API регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="784d1-122">Certificate Enrollment API Reference</span></span>](certificate-enrollment-api-reference.md)<br/> | <span data-ttu-id="784d1-123">Подробное описание интерфейсов, перечислений и других элементов программирования, которые можно использовать для регистрации пользователя или компьютера в иерархии сертификатов.</span><span class="sxs-lookup"><span data-stu-id="784d1-123">Detailed descriptions of interfaces, enumerations, and other programming elements that can be used to enroll a user or computer in a certificate hierarchy.</span></span><br/> |



 

 

 




