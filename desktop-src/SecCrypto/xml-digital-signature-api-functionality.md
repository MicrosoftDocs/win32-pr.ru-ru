---
description: Криптксмл предоставляет набор интерфейсов API низкого уровня, позволяющих приложениям создавать и проверять запечатанные, запечатывание и отсоединенные подписи. Криптксмл можно использовать для создания и проверки содержимого, хранящегося в элементах объекта подписи, включая манифесты.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: Функциональность API цифровых подписей XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663435"
---
# <a name="xml-digital-signature-api-functionality"></a><span data-ttu-id="3b90a-104">Функциональность API цифровых подписей XML</span><span class="sxs-lookup"><span data-stu-id="3b90a-104">XML Digital Signature API Functionality</span></span>

<span data-ttu-id="3b90a-105">Криптксмл предоставляет набор интерфейсов API низкого уровня, позволяющих приложениям создавать и проверять запечатанные, запечатывание и отсоединенные подписи.</span><span class="sxs-lookup"><span data-stu-id="3b90a-105">CryptXML provides a low level set of APIs that allow applications to create and verify enveloped, enveloping, and detached signatures.</span></span> <span data-ttu-id="3b90a-106">Криптксмл можно использовать для создания и проверки содержимого, хранящегося в элементах объекта подписи, включая манифесты.</span><span class="sxs-lookup"><span data-stu-id="3b90a-106">You can use CryptXML to create and verify content stored in signature object elements, including manifests.</span></span> <span data-ttu-id="3b90a-107">Для подписания и проверки [*цифровой подписи*](../secgloss/d-gly.md)XML можно использовать открытый/частный, общий ключ или сертификат [*X. 509*](../secgloss/x-gly.md) или цепочку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="3b90a-107">A public/private, shared key, or an [*X.509*](../secgloss/x-gly.md) certificate or certificate chain can be used to sign and verify the XML [*digital signature*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="3b90a-108">Приложения, использующие Криптксмл для проверки внешних ссылок (ссылки, предназначенные для внешнего документа или файла вне контекста документа), должны разрешать внешние URI и извлекать данные для пократкой обработки.</span><span class="sxs-lookup"><span data-stu-id="3b90a-108">Applications that use CryptXML to verify external references (references that target an external document or file outside of the document context) must resolve the external URIs and retrieve the data to be digested.</span></span>

<span data-ttu-id="3b90a-109">Дополнительные сведения о алгоритмах шифрования, поддерживаемых Криптксмл, см. в разделе [алгоритмы шифрования цифровых подписей XML](xml-digital-signature-cryptographic-algorithms.md).</span><span class="sxs-lookup"><span data-stu-id="3b90a-109">For information about the cryptographic algorithms supported by CryptXML, see [XML Digital Signature Cryptographic Algorithms](xml-digital-signature-cryptographic-algorithms.md).</span></span>

<span data-ttu-id="3b90a-110">Криптксмл обеспечивает поддержку алгоритмов канонизации со следующими идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="3b90a-110">CryptXML provides support for the canonicalization algorithms with the following identifiers.</span></span>



| <span data-ttu-id="3b90a-111">Константа</span><span class="sxs-lookup"><span data-stu-id="3b90a-111">Constant</span></span>                                              | <span data-ttu-id="3b90a-112">Значение URI</span><span class="sxs-lookup"><span data-stu-id="3b90a-112">URI value</span></span>                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="3b90a-113">\_C14N канонизации всзури \_</span><span class="sxs-lookup"><span data-stu-id="3b90a-113">wszURI\_CANONICALIZATION\_C14N</span></span><br/>             | <span data-ttu-id="3b90a-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span><span class="sxs-lookup"><span data-stu-id="3b90a-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span></span><br/>               |
| <span data-ttu-id="3b90a-115">\_C14NC канонизации всзури \_</span><span class="sxs-lookup"><span data-stu-id="3b90a-115">wszURI\_CANONICALIZATION\_C14NC</span></span><br/>            | <span data-ttu-id="3b90a-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="3b90a-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span></span><br/> |
| <span data-ttu-id="3b90a-117">Всзури \_ канонизации \_ ексслусиве \_ C14N</span><span class="sxs-lookup"><span data-stu-id="3b90a-117">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14N</span></span><br/>  | <span data-ttu-id="3b90a-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span><span class="sxs-lookup"><span data-stu-id="3b90a-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span></span><br/>                      |
| <span data-ttu-id="3b90a-119">Всзури \_ канонизации \_ ексслусиве \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="3b90a-119">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14NC</span></span><br/> | <span data-ttu-id="3b90a-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="3b90a-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span></span><br/>          |



 

<span data-ttu-id="3b90a-121">Криптксмл обеспечивает поддержку преобразования запечатанной подписи.</span><span class="sxs-lookup"><span data-stu-id="3b90a-121">CryptXML provides support for the enveloped signature transform.</span></span>



| <span data-ttu-id="3b90a-122">Константа</span><span class="sxs-lookup"><span data-stu-id="3b90a-122">Constant</span></span>                                       | <span data-ttu-id="3b90a-123">Значение URI</span><span class="sxs-lookup"><span data-stu-id="3b90a-123">URI value</span></span>                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="3b90a-124">\_Преобразование всзури xmlns в \_ \_ конверт</span><span class="sxs-lookup"><span data-stu-id="3b90a-124">wszURI\_XMLNS\_TRANSFORM\_ENVELOPED</span></span><br/> | <span data-ttu-id="3b90a-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span><span class="sxs-lookup"><span data-stu-id="3b90a-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span></span><br/> |



 

<span data-ttu-id="3b90a-126">По умолчанию Криптксмл не поддерживает преобразования XPath или XSLT.</span><span class="sxs-lookup"><span data-stu-id="3b90a-126">By default, CryptXML does not support XPath or XSLT transforms.</span></span> <span data-ttu-id="3b90a-127">При необходимости приложения могут реализовать эти преобразования поверх Криптксмл.</span><span class="sxs-lookup"><span data-stu-id="3b90a-127">If required, applications can implement these transforms on top of CryptXML.</span></span>

 

 
