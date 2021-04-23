---
description: Каждое свойство управления регистрацией сертификатов доступно для чтения и записи и имеет инициализированное значение по умолчанию, а также набор допустимых значений.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Использование свойств управления регистрацией сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811225"
---
# <a name="using-the-certificate-enrollment-control-properties"></a><span data-ttu-id="8c78a-103">Использование свойств управления регистрацией сертификатов</span><span class="sxs-lookup"><span data-stu-id="8c78a-103">Using the Certificate Enrollment Control Properties</span></span>

<span data-ttu-id="8c78a-104">Каждое свойство управления регистрацией сертификатов доступно для чтения и записи и имеет инициализированное значение по умолчанию, а также набор допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="8c78a-104">Each Certificate Enrollment Control property is read/write and has an initialized default as well as a set of acceptable values.</span></span> <span data-ttu-id="8c78a-105">Можно задать для свойства любое значение в этом наборе, чтобы изменить поведение методов, использующих свойство.</span><span class="sxs-lookup"><span data-stu-id="8c78a-105">You can set a property to any value within this set in order to modify the behavior of methods that use the property.</span></span> <span data-ttu-id="8c78a-106">Чтобы получить требуемое поведение, задайте свойство перед вызовом метода, который использует значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8c78a-106">To get a desired behavior, set the property before you call the method that uses that property's value.</span></span>

<span data-ttu-id="8c78a-107">Однако обратите внимание, что после вызова следующих методов</span><span class="sxs-lookup"><span data-stu-id="8c78a-107">Note, however, that after calling the following methods</span></span>

-   [<span data-ttu-id="8c78a-108">**acceptPKCS7**</span><span class="sxs-lookup"><span data-stu-id="8c78a-108">**acceptPKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [<span data-ttu-id="8c78a-109">**acceptFilePKCS7**</span><span class="sxs-lookup"><span data-stu-id="8c78a-109">**acceptFilePKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [<span data-ttu-id="8c78a-110">**createPKCS10**</span><span class="sxs-lookup"><span data-stu-id="8c78a-110">**createPKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [<span data-ttu-id="8c78a-111">**createFilePKCS10**</span><span class="sxs-lookup"><span data-stu-id="8c78a-111">**createFilePKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

<span data-ttu-id="8c78a-112">Сброс следующих свойств заблокирован</span><span class="sxs-lookup"><span data-stu-id="8c78a-112">the following properties are blocked from being reset</span></span>

-   [<span data-ttu-id="8c78a-113">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="8c78a-113">**ProviderType**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [<span data-ttu-id="8c78a-114">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="8c78a-114">**KeySpec**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [<span data-ttu-id="8c78a-115">**провидерфлагс**</span><span class="sxs-lookup"><span data-stu-id="8c78a-115">**ProviderFlags**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [<span data-ttu-id="8c78a-116">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="8c78a-116">**ContainerName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [<span data-ttu-id="8c78a-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="8c78a-117">**ProviderName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

<span data-ttu-id="8c78a-118">Если не вызывается метод [**ICEnroll4:: Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) .</span><span class="sxs-lookup"><span data-stu-id="8c78a-118">unless the [**ICEnroll4::Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) method is called.</span></span>

<span data-ttu-id="8c78a-119">Сведения об отдельных свойствах и методах см. в справочных разделах, посвященных этим свойствам и методам в [справочнике по шифрованию](cryptography-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8c78a-119">For information about individual properties and methods, see the reference topics for those properties and methods in the [Cryptography Reference](cryptography-reference.md).</span></span>

<span data-ttu-id="8c78a-120">В следующих разделах содержатся сведения, относящиеся к языку, для настройки и получения свойств управления регистрацией сертификатов.</span><span class="sxs-lookup"><span data-stu-id="8c78a-120">The following sections contain language-specific information for setting and retrieving the Certificate Enrollment Control properties:</span></span>

-   [<span data-ttu-id="8c78a-121">Свойства управления регистрацией сертификатов в C++</span><span class="sxs-lookup"><span data-stu-id="8c78a-121">Certificate Enrollment Control Properties in C++</span></span>](certificate-enrollment-control-properties-in-c-.md)

 

 
