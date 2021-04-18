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
# <a name="add-a-signature-request-to-an-xps-document"></a>Добавление запроса подписи в документ XPS

В этом разделе описывается добавление запроса подписи в документ XPS. Запрос подписи предлагает пользователю подписать документ, если он соглашается с намерением подписи.

Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования цифровых подписей](basic-digital-signature-programming-tasks.md).

Чтобы добавить запрос подписи в документ XPS, выполните следующие действия.

1.  Загрузите документ XPS в диспетчер подписей, как описано в разделе [Инициализация диспетчера подписей](initialize-the-signature-manager.md).
2.  Добавьте блок подписи в диспетчер подписей.
3.  Создайте запрос подписи в новом блоке сигнатуры.
4.  Задайте свойства запроса подписи:
    1.  Задайте цель подписи.
    2.  Задайте имя пользователя, подпись которого запрошена (запрошенный подписывающий).
    3.  Задайте дату, которая является обязательной для подписи.
    4.  При необходимости задайте другие свойства подписи.

В следующем примере кода показано, как добавить запрос подписи в документ XPS.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

**Используется в этом разделе**
</dt> <dt>

[**икспссигнатуреблокк**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[**Икспссигнатуреблокк:: Креатерекуест**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[**икспссигнатуреманажер**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**Икспссигнатуреманажер:: Аддсигнатуреблокк**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[**икспссигнатуререкуест**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[**Икспссигнатуререкуест:: Сетинтент**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[**Икспссигнатуререкуест:: Сетрекуестедсигнер**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[**Икспссигнатуререкуест:: Сетрекуестсигнбидате**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[Ошибки API цифровой подписи XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Ошибки документа XPS](xps-document-errors.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



