---
description: Формат сертификата X. 509 версии 3 определяет несколько расширений, которые могут быть добавлены к сертификату.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Расширения (API регистрации сертификатов)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647503"
---
# <a name="extensions-certificate-enrollment-api"></a><span data-ttu-id="de87b-103">Расширения (API регистрации сертификатов)</span><span class="sxs-lookup"><span data-stu-id="de87b-103">Extensions (Certificate Enrollment API)</span></span>

<span data-ttu-id="de87b-104">Формат сертификата X. 509 версии 3 определяет несколько расширений, которые могут быть добавлены к сертификату.</span><span class="sxs-lookup"><span data-stu-id="de87b-104">The X.509 version 3 certificate format identifies multiple extensions that can be added to a certificate.</span></span> <span data-ttu-id="de87b-105">Расширения предоставляют расширенные сведения об использовании ключа, политиках сертификатов и ограничениях, альтернативных формах имен и многом другом.</span><span class="sxs-lookup"><span data-stu-id="de87b-105">The extensions provide enhanced information about key usage, certificate policies and constraints, alternative name forms, and more.</span></span> <span data-ttu-id="de87b-106">Для определения значения расширения можно использовать интерфейс [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .</span><span class="sxs-lookup"><span data-stu-id="de87b-106">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an extension value.</span></span> <span data-ttu-id="de87b-107">Многие из распространенных расширений можно создать с помощью стандартных интерфейсов, производных от **IX509Extension**.</span><span class="sxs-lookup"><span data-stu-id="de87b-107">Many of the common extensions can be created by using predefined interfaces derived from **IX509Extension**.</span></span> <span data-ttu-id="de87b-108">Коллекция расширений добавляется в запрос сертификата путем включения коллекции в атрибуты запроса.</span><span class="sxs-lookup"><span data-stu-id="de87b-108">A collection of extensions is added to a certificate request by including the collection in the request attributes.</span></span> <span data-ttu-id="de87b-109">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="de87b-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="de87b-110">Поддерживаемые расширения</span><span class="sxs-lookup"><span data-stu-id="de87b-110">Supported Extensions</span></span>](supported-extensions.md)
-   [<span data-ttu-id="de87b-111">\#Расширения PKCS 10</span><span class="sxs-lookup"><span data-stu-id="de87b-111">PKCS \#10 Extensions</span></span>](pkcs--10-extensions.md)
-   [<span data-ttu-id="de87b-112">Расширения CMC</span><span class="sxs-lookup"><span data-stu-id="de87b-112">CMC Extensions</span></span>](cmc-extensions.md)

 

 



