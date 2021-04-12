---
description: В запрос на сертификат можно добавить атрибуты, чтобы предоставить центр сертификации (ЦС) с дополнительными сведениями, которые он может использовать при создании и выдаче сертификата.
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: Функции атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6413da0d43c142373e6f3cabe3d8e31636b82ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264352"
---
# <a name="attribute-functions"></a><span data-ttu-id="0c8be-103">Функции атрибутов</span><span class="sxs-lookup"><span data-stu-id="0c8be-103">Attribute Functions</span></span>

<span data-ttu-id="0c8be-104">В запрос на сертификат можно добавить атрибуты, чтобы предоставить [*центр сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС) с дополнительными сведениями, которые он может использовать при создании и выдаче сертификата.</span><span class="sxs-lookup"><span data-stu-id="0c8be-104">Attributes can be added to a certificate request to provide a [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) with additional information that it can use when creating and issuing a certificate.</span></span>

<span data-ttu-id="0c8be-105">CertEnroll.dll реализует следующие интерфейсы для определения атрибутов и коллекций атрибутов:</span><span class="sxs-lookup"><span data-stu-id="0c8be-105">CertEnroll.dll implements the following interfaces to define attributes and attribute collections:</span></span>

-   [<span data-ttu-id="0c8be-106">**икриптаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="0c8be-106">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [<span data-ttu-id="0c8be-107">**икриптаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="0c8be-107">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [<span data-ttu-id="0c8be-108">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="0c8be-108">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [<span data-ttu-id="0c8be-109">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="0c8be-109">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [<span data-ttu-id="0c8be-110">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="0c8be-110">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [<span data-ttu-id="0c8be-111">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="0c8be-111">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [<span data-ttu-id="0c8be-112">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="0c8be-112">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [<span data-ttu-id="0c8be-113">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="0c8be-113">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [<span data-ttu-id="0c8be-114">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="0c8be-114">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [<span data-ttu-id="0c8be-115">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="0c8be-115">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [<span data-ttu-id="0c8be-116">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="0c8be-116">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

<span data-ttu-id="0c8be-117">В следующих разделах указываются функции, экспортированные Xenroll.dll, чтобы связать криптографические атрибуты с запросами на сертификаты и обсудить использование CertEnroll.dll для замены функции или указания на отсутствие сопоставления между двумя библиотеками:</span><span class="sxs-lookup"><span data-stu-id="0c8be-117">The following sections identify functions exported by Xenroll.dll to associate cryptographic attributes with certificate requests and discuss how to use CertEnroll.dll to replace the function or indicate that no mapping between the two libraries exists:</span></span>

-   [<span data-ttu-id="0c8be-118">аддаттрибутеторекуествстр</span><span class="sxs-lookup"><span data-stu-id="0c8be-118">addAttributeToRequestWStr</span></span>](#addattributetorequestwstr)
-   [<span data-ttu-id="0c8be-119">AddAuthenticatedAttributesToPKCS7Request</span><span class="sxs-lookup"><span data-stu-id="0c8be-119">AddAuthenticatedAttributesToPKCS7Request</span></span>](#addauthenticatedattributestopkcs7request)
-   [<span data-ttu-id="0c8be-120">адднамевалуепаирторекуествстр</span><span class="sxs-lookup"><span data-stu-id="0c8be-120">addNameValuePairToRequestWStr</span></span>](#addnamevaluepairtorequestwstr)
-   [<span data-ttu-id="0c8be-121">адднамевалуепаиртосигнатуревстр</span><span class="sxs-lookup"><span data-stu-id="0c8be-121">AddNameValuePairToSignatureWStr</span></span>](#addnamevaluepairtosignaturewstr)
-   [<span data-ttu-id="0c8be-122">ClientId</span><span class="sxs-lookup"><span data-stu-id="0c8be-122">ClientId</span></span>](#clientid)
-   [<span data-ttu-id="0c8be-123">реневалцертификате</span><span class="sxs-lookup"><span data-stu-id="0c8be-123">RenewalCertificate</span></span>](#renewalcertificate)
-   [<span data-ttu-id="0c8be-124">ресетаттрибутес</span><span class="sxs-lookup"><span data-stu-id="0c8be-124">resetAttributes</span></span>](#resetattributes)
-   [<span data-ttu-id="0c8be-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0c8be-125">Related topics</span></span>](#related-topics)

## <a name="addattributetorequestwstr"></a><span data-ttu-id="0c8be-126">аддаттрибутеторекуествстр</span><span class="sxs-lookup"><span data-stu-id="0c8be-126">addAttributeToRequestWStr</span></span>

<span data-ttu-id="0c8be-127">Функция [**аддаттрибутеторекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) в Xenroll.dll добавляет атрибут к запросу на сертификат.</span><span class="sxs-lookup"><span data-stu-id="0c8be-127">The [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) function in Xenroll.dll adds an attribute to a certificate request.</span></span>

<span data-ttu-id="0c8be-128">Как правило, чтобы добавить атрибут к запросу с помощью объектов, реализованных в CertEnroll.dll, можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0c8be-128">In general, to add an attribute to a request by using the objects implemented in CertEnroll.dll, you can perform the following actions:</span></span>

1.  <span data-ttu-id="0c8be-129">Создайте объект коллекции [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-129">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection object.</span></span>
2.  <span data-ttu-id="0c8be-130">Создайте объект [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) и вызовите метод [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) , чтобы создать атрибут из идентификатора объекта и значения атрибута или использовать любой из перечисленных выше интерфейсов, чтобы определить один из более общих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0c8be-130">Create an [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) object and call the [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) method to create an attribute from an object identifier and attribute value or use any of the interfaces listed earlier to define one of the more common attributes.</span></span>
3.  <span data-ttu-id="0c8be-131">Добавьте каждый новый атрибут, созданный на предыдущем шаге, в коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) с помощью метода [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-131">Add each new attribute created in the preceding step to the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection by using the [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) method.</span></span>
4.  <span data-ttu-id="0c8be-132">Создайте объект [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) и инициализируйте его, вызвав метод [**инитиализефромвалуес**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) и указав коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) во входных данных.</span><span class="sxs-lookup"><span data-stu-id="0c8be-132">Create an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object and initialize it by calling the [**InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) method and specifying the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection on input.</span></span>
5.  <span data-ttu-id="0c8be-133">Получите объект коллекции [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) , вызвав свойство [**криптаттрибутес**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) для существующего объекта запроса [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) или [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-133">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection object by calling the [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) property on an existing [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) or [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) request object.</span></span>
6.  <span data-ttu-id="0c8be-134">Добавьте объект [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) в коллекцию [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-134">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection.</span></span>

## <a name="addauthenticatedattributestopkcs7request"></a><span data-ttu-id="0c8be-135">AddAuthenticatedAttributesToPKCS7Request</span><span class="sxs-lookup"><span data-stu-id="0c8be-135">AddAuthenticatedAttributesToPKCS7Request</span></span>

<span data-ttu-id="0c8be-136">Прошедшие проверку атрибуты — это пары "имя-значение", которые подписываются и добавляются в сигнатуру.</span><span class="sxs-lookup"><span data-stu-id="0c8be-136">Authenticated attributes are name-value pairs that are signed by and added to a signature.</span></span> <span data-ttu-id="0c8be-137">Функция [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) в Xenroll.dll Добавляет массив атрибутов, прошедших проверку подлинности, к запросу [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-137">The [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) function in Xenroll.dll adds an array of authenticated attributes to a [*PKCS \#7*](/windows/desktop/SecGloss/p-gly) request.</span></span>

<span data-ttu-id="0c8be-138">Как обсуждалось выше для функции [**аддаттрибутеторекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) , можно использовать CertEnroll.dll, чтобы легко определить и добавить коллекцию атрибутов в запрос на сертификат.</span><span class="sxs-lookup"><span data-stu-id="0c8be-138">As discussed above for the [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) function, you can use CertEnroll.dll to easily define and add a collection of attributes to a certificate request.</span></span> <span data-ttu-id="0c8be-139">Однако нельзя выбрать, прошел ли атрибут проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="0c8be-139">You cannot, however, choose whether the attribute is authenticated.</span></span> <span data-ttu-id="0c8be-140">Процесс регистрации автоматически принимает это решение.</span><span class="sxs-lookup"><span data-stu-id="0c8be-140">The enrollment process automatically makes this decision.</span></span>

## <a name="addnamevaluepairtorequestwstr"></a><span data-ttu-id="0c8be-141">адднамевалуепаирторекуествстр</span><span class="sxs-lookup"><span data-stu-id="0c8be-141">addNameValuePairToRequestWStr</span></span>

<span data-ttu-id="0c8be-142">Функция [**адднамевалуепаирторекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) в Xenroll.dll добавляет в запрос пару "имя-значение", не прошедшее проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="0c8be-142">The [**addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) function in Xenroll.dll adds an unauthenticated name-value pair to a request.</span></span>

<span data-ttu-id="0c8be-143">Вы можете использовать интерфейс [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) в CertEnroll.dll для определения пары "имя-значение", а также добавить коллекцию пар "имя-значение" в объект запроса CMC, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0c8be-143">You can use the [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) interface in CertEnroll.dll to define a name-value pair, and you can add a collection of name-value pairs to a CMC request object by performing the following actions:</span></span>

1.  <span data-ttu-id="0c8be-144">Создание и инициализация объекта [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-144">Create and initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span> <span data-ttu-id="0c8be-145">Процесс инициализации создает пустую коллекцию [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-145">The initialization process creates an empty [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection.</span></span>
2.  <span data-ttu-id="0c8be-146">Вызовите свойство [**намевалуепаирс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) для существующего объекта запроса CMC, чтобы получить коллекцию.</span><span class="sxs-lookup"><span data-stu-id="0c8be-146">Call the [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) property on an existing CMC request object to retrieve the collection.</span></span>
3.  <span data-ttu-id="0c8be-147">Создание и инициализация объекта [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-147">Create and initialize an [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) object.</span></span>
4.  <span data-ttu-id="0c8be-148">Добавьте каждую новую пару "имя-значение" в коллекцию [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) , вызвав метод [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-148">Add each new name-value pair to the [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection by calling the [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) method.</span></span>

<span data-ttu-id="0c8be-149">Процесс регистрации помещает коллекцию пар "имя-значение" в структуру **тагжедаттрибуте** запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="0c8be-149">The enrollment process places the collection of name-value pairs in the **TaggedAttribute** structure of the CMC request.</span></span>

## <a name="addnamevaluepairtosignaturewstr"></a><span data-ttu-id="0c8be-150">адднамевалуепаиртосигнатуревстр</span><span class="sxs-lookup"><span data-stu-id="0c8be-150">AddNameValuePairToSignatureWStr</span></span>

<span data-ttu-id="0c8be-151">Функция [**адднамевалуепаиртосигнатуревстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) в Xenroll.dll добавляет к запросу пару "имя-значение", прошедшее проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="0c8be-151">The [**AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) function in Xenroll.dll adds an authenticated name-value pair to a request.</span></span> <span data-ttu-id="0c8be-152">Обычно это используется для указания имени инициатора запроса в запросе на регистрацию (ЕОБО).</span><span class="sxs-lookup"><span data-stu-id="0c8be-152">This is typically used to specify the requester name in an enroll-on-behalf-of (EOBO) request.</span></span>

<span data-ttu-id="0c8be-153">В CertEnroll.dll используйте свойство [**рекуестернаме**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) , чтобы указать имя в запросе еобо.</span><span class="sxs-lookup"><span data-stu-id="0c8be-153">In CertEnroll.dll, use the [**RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) property to specify the name in an EOBO request.</span></span>

## <a name="clientid"></a><span data-ttu-id="0c8be-154">ClientId</span><span class="sxs-lookup"><span data-stu-id="0c8be-154">ClientId</span></span>

<span data-ttu-id="0c8be-155">Функция [**ClientID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) в Xenroll.dll указывает или получает атрибут **ClientID** .</span><span class="sxs-lookup"><span data-stu-id="0c8be-155">The [**ClientId**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) function in Xenroll.dll specifies or retrieves a **ClientId** attribute.</span></span>

<span data-ttu-id="0c8be-156">Используйте свойство [**ClientID**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) в CertEnroll.dll, чтобы добавить этот атрибут в запрос CMC или PKCS \# 10.</span><span class="sxs-lookup"><span data-stu-id="0c8be-156">Use the [**ClientId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) property in CertEnroll.dll to add this attribute to a CMC or PKCS \#10 request.</span></span>

## <a name="renewalcertificate"></a><span data-ttu-id="0c8be-157">реневалцертификате</span><span class="sxs-lookup"><span data-stu-id="0c8be-157">RenewalCertificate</span></span>

<span data-ttu-id="0c8be-158">Функция [**реневалцертификате**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) в Xenroll.dll указывает или получает атрибут **реневалцертификате** .</span><span class="sxs-lookup"><span data-stu-id="0c8be-158">The [**RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) function in Xenroll.dll specifies or retrieves a **RenewalCertificate** attribute.</span></span>

<span data-ttu-id="0c8be-159">В CertEnroll.dll при вызове [**инитиализефромцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) для \# объекта PKCS 7 или PKCS) автоматически создается.</span><span class="sxs-lookup"><span data-stu-id="0c8be-159">In CertEnroll.dll, when you call [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) on a PKCS \#7 or PKCS ) object is automatically created.</span></span>

## <a name="resetattributes"></a><span data-ttu-id="0c8be-160">ресетаттрибутес</span><span class="sxs-lookup"><span data-stu-id="0c8be-160">resetAttributes</span></span>

<span data-ttu-id="0c8be-161">Функция [**ресетаттрибутес**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) в Xenroll.dll удаляет коллекцию атрибутов из запроса.</span><span class="sxs-lookup"><span data-stu-id="0c8be-161">The [**resetAttributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) function in Xenroll.dll removes the attribute collection from a request.</span></span>

<span data-ttu-id="0c8be-162">Чтобы удалить атрибут из запроса по индексу с помощью CertEnroll.dll, вызовите метод [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) в коллекции [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-162">To remove an attribute from a request by index using CertEnroll.dll, call the [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) method on the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection.</span></span> <span data-ttu-id="0c8be-163">Чтобы удалить все атрибуты из запроса, вызовите метод [**clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) .</span><span class="sxs-lookup"><span data-stu-id="0c8be-163">To remove all attributes from a request, call the [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c8be-164">См. также</span><span class="sxs-lookup"><span data-stu-id="0c8be-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c8be-165">Сопоставление Xenroll.dll CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="0c8be-165">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="0c8be-166">**икриптаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="0c8be-166">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[<span data-ttu-id="0c8be-167">**икриптаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="0c8be-167">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[<span data-ttu-id="0c8be-168">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="0c8be-168">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[<span data-ttu-id="0c8be-169">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="0c8be-169">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[<span data-ttu-id="0c8be-170">**IX509NameValuePair**</span><span class="sxs-lookup"><span data-stu-id="0c8be-170">**IX509NameValuePair**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[<span data-ttu-id="0c8be-171">**IX509NameValuePairs**</span><span class="sxs-lookup"><span data-stu-id="0c8be-171">**IX509NameValuePairs**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 
