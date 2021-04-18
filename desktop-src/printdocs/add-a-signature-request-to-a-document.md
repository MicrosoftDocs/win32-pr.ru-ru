---
description: В этом разделе описывается добавление запроса подписи в документ XPS.
ms.assetid: 95eb1887-8754-43e0-8886-1f23653bff26
title: Добавление запроса подписи в документ XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db0d3a899dd49f141adf5cd23ea8c837c8b12d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693421"
---
# <a name="add-a-signature-request-to-an-xps-document"></a><span data-ttu-id="552df-103">Добавление запроса подписи в документ XPS</span><span class="sxs-lookup"><span data-stu-id="552df-103">Add a Signature Request to an XPS Document</span></span>

<span data-ttu-id="552df-104">В этом разделе описывается добавление запроса подписи в документ XPS.</span><span class="sxs-lookup"><span data-stu-id="552df-104">This topic describes how to add a signature request to an XPS document.</span></span> <span data-ttu-id="552df-105">Запрос подписи предлагает пользователю подписать документ, если он соглашается с намерением подписи.</span><span class="sxs-lookup"><span data-stu-id="552df-105">A signature request prompts a user to sign a document if he or she agrees with the signature intent.</span></span>

<span data-ttu-id="552df-106">Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования цифровых подписей](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="552df-106">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="552df-107">Чтобы добавить запрос подписи в документ XPS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="552df-107">To add a signature request to an XPS Document:</span></span>

1.  <span data-ttu-id="552df-108">Загрузите документ XPS в диспетчер подписей, как описано в разделе [Инициализация диспетчера подписей](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="552df-108">Load the XPS document into a signature manager, as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>
2.  <span data-ttu-id="552df-109">Добавьте блок подписи в диспетчер подписей.</span><span class="sxs-lookup"><span data-stu-id="552df-109">Add a signature block to the signature manager.</span></span>
3.  <span data-ttu-id="552df-110">Создайте запрос подписи в новом блоке сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="552df-110">Create a signature request in the new signature block.</span></span>
4.  <span data-ttu-id="552df-111">Задайте свойства запроса подписи:</span><span class="sxs-lookup"><span data-stu-id="552df-111">Set the properties of the signature request:</span></span>
    1.  <span data-ttu-id="552df-112">Задайте цель подписи.</span><span class="sxs-lookup"><span data-stu-id="552df-112">Set the signature intent.</span></span>
    2.  <span data-ttu-id="552df-113">Задайте имя пользователя, подпись которого запрошена (запрошенный подписывающий).</span><span class="sxs-lookup"><span data-stu-id="552df-113">Set the name of the person whose signature is requested (the requested signer).</span></span>
    3.  <span data-ttu-id="552df-114">Задайте дату, которая является обязательной для подписи.</span><span class="sxs-lookup"><span data-stu-id="552df-114">Set the date the signature is required.</span></span>
    4.  <span data-ttu-id="552df-115">При необходимости задайте другие свойства подписи.</span><span class="sxs-lookup"><span data-stu-id="552df-115">Set other signature properties as required.</span></span>

<span data-ttu-id="552df-116">В следующем примере кода показано, как добавить запрос подписи в документ XPS.</span><span class="sxs-lookup"><span data-stu-id="552df-116">The following code example illustrates how to add a signature request to an XPS document.</span></span>


```C++
HRESULT 
AddSignatureRequestToDocument (
    __in IXpsSignatureManager    *signatureManager,
    __in LPCWSTR                reasonForSignatureRequest,
    __in LPCWSTR                nameOfRequestedSigner,
    __in LPCWSTR                requestSignByDate
)
{
    HRESULT                  hr = S_OK;
    IXpsSignatureBlock       *signatureDefinition = NULL;
    IXpsSignatureRequest     *signatureRequest = NULL;
    
    // Create a new signature block and get a pointer to it
    hr = signatureManager->AddSignatureBlock (NULL, 0, &signatureDefinition);
    
    if (SUCCEEDED(hr)) {
        // Create a new signature request to use for this signature block
        hr = signatureDefinition->CreateRequest(NULL, &signatureRequest);
    }

    if (SUCCEEDED(hr)) {
        // Initialize the properties of the signature request

        //  Set the string that describes the purpose of the signature
        //  to the person who will sign the document.
        hr = signatureRequest->SetIntent(reasonForSignatureRequest);
    }

    if (SUCCEEDED(hr)) {
        //  Set the name of the person whose signature is requested.
        hr = signatureRequest->SetRequestedSigner(nameOfRequestedSigner);
    }

    if (SUCCEEDED(hr)) {
        //  Set the date that the person should sign the document.
        //  The person is requested to sign the document on or before
        //   the date specified in this field. Refer to the help text
        //   for the correct format of this string.
        hr = signatureRequest->SetRequestSignByDate(requestSignByDate);
    }

    if (NULL != signatureDefinition) signatureDefinition->Release();
    if (NULL != signatureRequest) signatureRequest->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="552df-117">См. также</span><span class="sxs-lookup"><span data-stu-id="552df-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="552df-118">**Используется в этом разделе**</span><span class="sxs-lookup"><span data-stu-id="552df-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="552df-119">**икспссигнатуреблокк**</span><span class="sxs-lookup"><span data-stu-id="552df-119">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[<span data-ttu-id="552df-120">**Икспссигнатуреблокк:: Креатерекуест**</span><span class="sxs-lookup"><span data-stu-id="552df-120">**IXpsSignatureBlock::CreateRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[<span data-ttu-id="552df-121">**икспссигнатуреманажер**</span><span class="sxs-lookup"><span data-stu-id="552df-121">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="552df-122">**Икспссигнатуреманажер:: Аддсигнатуреблокк**</span><span class="sxs-lookup"><span data-stu-id="552df-122">**IXpsSignatureManager::AddSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[<span data-ttu-id="552df-123">**икспссигнатуререкуест**</span><span class="sxs-lookup"><span data-stu-id="552df-123">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[<span data-ttu-id="552df-124">**Икспссигнатуререкуест:: Сетинтент**</span><span class="sxs-lookup"><span data-stu-id="552df-124">**IXpsSignatureRequest::SetIntent**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[<span data-ttu-id="552df-125">**Икспссигнатуререкуест:: Сетрекуестедсигнер**</span><span class="sxs-lookup"><span data-stu-id="552df-125">**IXpsSignatureRequest::SetRequestedSigner**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[<span data-ttu-id="552df-126">**Икспссигнатуререкуест:: Сетрекуестсигнбидате**</span><span class="sxs-lookup"><span data-stu-id="552df-126">**IXpsSignatureRequest::SetRequestSignByDate**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

<span data-ttu-id="552df-127">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="552df-127">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="552df-128">Ошибки API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="552df-128">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="552df-129">Ошибки документа XPS</span><span class="sxs-lookup"><span data-stu-id="552df-129">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="552df-130">XPS</span><span class="sxs-lookup"><span data-stu-id="552df-130">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



