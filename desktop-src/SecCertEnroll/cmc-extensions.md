---
description: Расширения включаются в запрос CMC путем добавления их в структуру Тагжедаттрибутес, показанную в следующем примере синтаксиса ASN. 1. Дополнительные сведения см. в разделе атрибуты.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: Расширения CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b104af2b28470627ea593321627ae5e5076b1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265636"
---
# <a name="cmc-extensions"></a><span data-ttu-id="7b4f3-104">Расширения CMC</span><span class="sxs-lookup"><span data-stu-id="7b4f3-104">CMC Extensions</span></span>

<span data-ttu-id="7b4f3-105">Расширения включаются в запрос CMC путем добавления их в структуру **тагжедаттрибутес** , показанную в следующем примере синтаксиса ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="7b4f3-105">Extensions are included in a CMC request by adding them to the **TaggedAttributes** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="7b4f3-106">Дополнительные сведения см. в разделе [атрибуты](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="7b4f3-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

<span data-ttu-id="7b4f3-107">Каждая структура в коллекции **тагжедаттрибутес** содержит целочисленный идентификатор, идентификатор объекта ASN. 1 и набор значений.</span><span class="sxs-lookup"><span data-stu-id="7b4f3-107">Each structure in the **TaggedAttributes** collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="7b4f3-108">Расширения включаются в запрос путем добавления структуры **кмкаддекстенсионс** в поле **Values** .</span><span class="sxs-lookup"><span data-stu-id="7b4f3-108">Extensions are incorporated into a request by adding a **CmcAddExtensions** structure to the **values** field.</span></span> <span data-ttu-id="7b4f3-109">Синтаксис структуры ASN. 1 показан в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="7b4f3-109">The ASN.1 structure syntax is shown in the following example.</span></span> <span data-ttu-id="7b4f3-110">Идентификатор объекта — **кскн \_ OID \_ CMC \_ Add \_ Extensions** (1.3.6.1.5.5.7.7.8).</span><span class="sxs-lookup"><span data-stu-id="7b4f3-110">The object identifier is **XCN\_OID\_CMC\_ADD\_EXTENSIONS** (1.3.6.1.5.5.7.7.8).</span></span>

``` syntax
CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
```

<span data-ttu-id="7b4f3-111">В следующей процедуре описывается, как использовать API регистрации сертификатов для добавления расширений в запрос сертификата CMC.</span><span class="sxs-lookup"><span data-stu-id="7b4f3-111">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a CMC certificate request.</span></span>

<span data-ttu-id="7b4f3-112">**Использование API регистрации сертификатов для добавления расширений в запрос сертификата CMC**</span><span class="sxs-lookup"><span data-stu-id="7b4f3-112">**To use the Certificate Enrollment API to add extensions to a CMC certificate request**</span></span>

1.  <span data-ttu-id="7b4f3-113">Создайте расширение с помощью любого из доступных интерфейсов, производных от интерфейса [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) , или непосредственно используйте объект **IX509Extension** для создания пользовательских расширений.</span><span class="sxs-lookup"><span data-stu-id="7b4f3-113">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface or use the **IX509Extension** object directly to create custom extensions.</span></span>
2.  <span data-ttu-id="7b4f3-114">Вызовите свойство [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) объекта [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) , чтобы получить коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .</span><span class="sxs-lookup"><span data-stu-id="7b4f3-114">Call the [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) property on the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object to retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
3.  <span data-ttu-id="7b4f3-115">Добавьте расширения, созданные на шаге 1, в коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .</span><span class="sxs-lookup"><span data-stu-id="7b4f3-115">Add the extensions created in step 1 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
4.  <span data-ttu-id="7b4f3-116">Вызовите [**регистрацию**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) , чтобы автоматически выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7b4f3-116">Call [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) to automatically perform the following actions:</span></span>
    -   <span data-ttu-id="7b4f3-117">Извлеките объект [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) из объекта [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="7b4f3-117">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) object from the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
    -   <span data-ttu-id="7b4f3-118">Создайте и инициализируйте объект [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) с помощью коллекции [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) , полученной на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="7b4f3-118">Create and initialize an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object by using the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 2.</span></span>
    -   <span data-ttu-id="7b4f3-119">Создайте коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) и добавьте в нее объект [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="7b4f3-119">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection and add the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object to it.</span></span>
    -   <span data-ttu-id="7b4f3-120">Используйте коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) для инициализации объекта [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="7b4f3-120">Use the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object.</span></span>
    -   <span data-ttu-id="7b4f3-121">Добавьте объект [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) в коллекцию [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .</span><span class="sxs-lookup"><span data-stu-id="7b4f3-121">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b4f3-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7b4f3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b4f3-123">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b4f3-123">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="7b4f3-124">Архитектура атрибута</span><span class="sxs-lookup"><span data-stu-id="7b4f3-124">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="7b4f3-125">Атрибуты CMC</span><span class="sxs-lookup"><span data-stu-id="7b4f3-125">CMC Attributes</span></span>](cmc-attributes.md)
</dt> <dt>

[<span data-ttu-id="7b4f3-126">Расширения</span><span class="sxs-lookup"><span data-stu-id="7b4f3-126">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



