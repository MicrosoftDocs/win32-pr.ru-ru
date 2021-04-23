---
description: Данные в сертификате, списке отзыва сертификатов (CRL) или контексте списка доверия сертификатов (CTL), включая любые расширения, доступны только для чтения и не могут быть изменены.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Расширенные свойства сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29853736433cb143a201ca352fceff0141cc96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155898"
---
# <a name="certificate-extended-properties"></a><span data-ttu-id="4ecaf-103">Расширенные свойства сертификата</span><span class="sxs-lookup"><span data-stu-id="4ecaf-103">Certificate Extended Properties</span></span>

<span data-ttu-id="4ecaf-104">Данные в [*сертификате*](../secgloss/c-gly.md), [*списке отзыва сертификатов*](../secgloss/c-gly.md) (CRL) или [*контексте*](../secgloss/c-gly.md) [*списка доверия сертификатов*](../secgloss/c-gly.md) (CTL), включая любые расширения, доступны только для чтения и не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="4ecaf-104">The data in a [*certificate*](../secgloss/c-gly.md), [*certificate revocation list*](../secgloss/c-gly.md) (CRL), or [*certificate trust list*](../secgloss/c-gly.md) (CTL) [*context*](../secgloss/c-gly.md), including any extensions, is read-only and cannot be changed.</span></span> <span data-ttu-id="4ecaf-105">Однако на платформах Майкрософт сертификаты CryptoAPI также имеют динамические расширенные свойства, которые можно добавлять и изменять.</span><span class="sxs-lookup"><span data-stu-id="4ecaf-105">However, on Microsoft platforms, CryptoAPI certificates also have dynamic extended properties that can be added and changed.</span></span>

> [!Note]  
> <span data-ttu-id="4ecaf-106">Расширенные свойства связаны с сертификатом и не являются частью сертификата, выданного [*центром сертификации*](../secgloss/c-gly.md) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="4ecaf-106">Extended properties are associated with a certificate and are not part of a certificate as issued by a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span> <span data-ttu-id="4ecaf-107">Расширенные свойства недоступны для сертификата, если он используется на платформе, отличной от Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="4ecaf-107">Extended properties are not available on a certificate when it is used on a non-Microsoft platform.</span></span>

 

<span data-ttu-id="4ecaf-108">Эти свойства включают данные, которые:</span><span class="sxs-lookup"><span data-stu-id="4ecaf-108">These properties include data that:</span></span>

-   <span data-ttu-id="4ecaf-109">Относится к закрытому ключу, который будет использоваться с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="4ecaf-109">Pertains to the private key to be used with the certificate.</span></span>
-   <span data-ttu-id="4ecaf-110">Указывает тип хэшей, которые будут выполняться в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4ecaf-110">Indicates the type of hashes to be performed on the certificate.</span></span>
-   <span data-ttu-id="4ecaf-111">Предоставляет определяемые пользователем сведения, связанные с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="4ecaf-111">Provides user-defined information associated with the certificate.</span></span>

<span data-ttu-id="4ecaf-112">На платформах Майкрософт значения этих свойств присоединяются к сертификату и перемещаются вместе с ним.</span><span class="sxs-lookup"><span data-stu-id="4ecaf-112">On Microsoft platforms, values for these properties are attached to and move with the certificate.</span></span> <span data-ttu-id="4ecaf-113">В настоящее время предопределенные свойства, идентифицируемые идентификаторами свойств, включают следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="4ecaf-113">Currently predefined properties identified with property IDs include the following properties:</span></span>

-   <span data-ttu-id="4ecaf-114">Эти свойства применяют сертификат к определенному закрытому ключу CSP и в пределах этого CSP:</span><span class="sxs-lookup"><span data-stu-id="4ecaf-114">These properties tie a certificate to a particular CSP and, within that CSP, to a particular private key:</span></span>
    -   <span data-ttu-id="4ecaf-115">\_идентификатор свойства \_ Prov для ключа \_ \_ сертификата \_</span><span class="sxs-lookup"><span data-stu-id="4ecaf-115">CERT\_KEY\_PROV\_HANDLE\_PROP\_ID</span></span>
    -   <span data-ttu-id="4ecaf-116">\_идентификатор свойства \_ \_ сведений о \_ \_ ключе сертификата Prov</span><span class="sxs-lookup"><span data-stu-id="4ecaf-116">CERT\_KEY\_PROV\_INFO\_PROP\_ID</span></span>
    -   <span data-ttu-id="4ecaf-117">\_ \_ \_ идентификатор Prop контекста ключа \_ сертификата</span><span class="sxs-lookup"><span data-stu-id="4ecaf-117">CERT\_KEY\_CONTEXT\_PROP\_ID</span></span>
-   <span data-ttu-id="4ecaf-118">Эти свойства указывают алгоритм хэширования, используемый при выполнении операции хэширования.</span><span class="sxs-lookup"><span data-stu-id="4ecaf-118">These properties indicate the hashing algorithm to be used when a hashing operation is performed:</span></span>
    -   <span data-ttu-id="4ecaf-119">\_ИД свойства \_ ХЭША \_ SHA1 \_ сертификата</span><span class="sxs-lookup"><span data-stu-id="4ecaf-119">CERT\_SHA1\_HASH\_PROP\_ID</span></span>
    -   <span data-ttu-id="4ecaf-120">\_Идентификатор свойства \_ ХЭША \_ MD5 \_ сертификата</span><span class="sxs-lookup"><span data-stu-id="4ecaf-120">CERT\_MD5\_HASH\_PROP\_ID</span></span>

<span data-ttu-id="4ecaf-121">Полный список заданных в настоящее время расширенных свойств сертификата и описания значения и использования каждого свойства см. в разделе [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) и [**цертсетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span><span class="sxs-lookup"><span data-stu-id="4ecaf-121">For complete lists of currently defined extended certificate properties and descriptions of the meaning and use of each property, see [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ecaf-122">См. также</span><span class="sxs-lookup"><span data-stu-id="4ecaf-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ecaf-123">**цертжеткрлконтекстпроперти**</span><span class="sxs-lookup"><span data-stu-id="4ecaf-123">**CertGetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="4ecaf-124">**цертжетктлконтекстпроперти**</span><span class="sxs-lookup"><span data-stu-id="4ecaf-124">**CertGetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[<span data-ttu-id="4ecaf-125">**цертсеткрлконтекстпроперти**</span><span class="sxs-lookup"><span data-stu-id="4ecaf-125">**CertSetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="4ecaf-126">**цертсетктлконтекстпроперти**</span><span class="sxs-lookup"><span data-stu-id="4ecaf-126">**CertSetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
