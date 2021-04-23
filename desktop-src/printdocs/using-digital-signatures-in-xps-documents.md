---
description: В этом разделе приведены рекомендации по использованию API цифровой подписи XPS для добавления цифровых подписей в документ XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Использование API цифровых подписей XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909572"
---
# <a name="using-xps-digital-signature-api"></a><span data-ttu-id="df8d2-103">Использование API цифровых подписей XPS</span><span class="sxs-lookup"><span data-stu-id="df8d2-103">Using XPS Digital Signature API</span></span>

<span data-ttu-id="df8d2-104">В этом разделе приведены рекомендации по использованию API цифровой подписи XPS для добавления цифровых подписей в документ XPS.</span><span class="sxs-lookup"><span data-stu-id="df8d2-104">This topic lists considerations for using the XPS Digital Signature API to add digital signatures to an XPS document.</span></span>

<span data-ttu-id="df8d2-105">API цифровой подписи XPS позволяет приложениям запрашивать у пользователей подписывать XPS-документы и проверять подписи, найденные в документах XPS.</span><span class="sxs-lookup"><span data-stu-id="df8d2-105">The XPS Digital Signature API enables applications to request users to sign XPS documents and to verify signatures that are found in XPS documents.</span></span> <span data-ttu-id="df8d2-106">API цифровой подписи XPS можно применить к документу XPS, не загружая его в модель XPS, и его можно использовать в потоках документов XPS, сериализуемых из OM-объекта XPS.</span><span class="sxs-lookup"><span data-stu-id="df8d2-106">The XPS Digital Signature API can be applied to an XPS document without loading it into an XPS OM, and it can be used on XPS document streams that are serialized from an XPS OM.</span></span>

<span data-ttu-id="df8d2-107">В разделе [задачи программирования API цифровых подписей XPS](#xps-digital-signature-api-programming-tasks) содержатся разделы, в которых описывается программирование с помощью API цифровой подписи XPS.</span><span class="sxs-lookup"><span data-stu-id="df8d2-107">The [XPS Digital Signature API Programming Tasks](#xps-digital-signature-api-programming-tasks) section contains topics that describe how to program with the XPS Digital Signature API.</span></span> <span data-ttu-id="df8d2-108">В этом разделе приведены рекомендации по использованию API цифровой подписи XPS при добавлении поддержки цифровых подписей в приложение.</span><span class="sxs-lookup"><span data-stu-id="df8d2-108">This topic lists the following considerations for using the XPS Digital Signature API when adding digital signature support to an application.</span></span>

-   [<span data-ttu-id="df8d2-109">Задачи программирования API цифровых подписей XPS</span><span class="sxs-lookup"><span data-stu-id="df8d2-109">XPS Digital Signature API Programming Tasks</span></span>](#xps-digital-signature-api-programming-tasks)
-   [<span data-ttu-id="df8d2-110">Специальные примечания о программировании API цифровых подписей XPS</span><span class="sxs-lookup"><span data-stu-id="df8d2-110">Special Notes about XPS Digital Signature API Programming</span></span>](#special-notes-about-xps-digital-signature-api-programming)
    -   [<span data-ttu-id="df8d2-111">Проверка цифровых подписей в документе XPS</span><span class="sxs-lookup"><span data-stu-id="df8d2-111">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
    -   [<span data-ttu-id="df8d2-112">Политика подписи цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="df8d2-112">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
    -   [<span data-ttu-id="df8d2-113">Внедрение цепочки сертификатов</span><span class="sxs-lookup"><span data-stu-id="df8d2-113">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
    -   [<span data-ttu-id="df8d2-114">Использование \_ структуры контекста CERT</span><span class="sxs-lookup"><span data-stu-id="df8d2-114">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)
-   [<span data-ttu-id="df8d2-115">См. также</span><span class="sxs-lookup"><span data-stu-id="df8d2-115">Related topics</span></span>](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a><span data-ttu-id="df8d2-116">Задачи программирования API цифровых подписей XPS</span><span class="sxs-lookup"><span data-stu-id="df8d2-116">XPS Digital Signature API Programming Tasks</span></span>

<span data-ttu-id="df8d2-117">В этом разделе содержатся разделы, в которых описывается выполнение задач по программированию с помощью API цифровой подписи XPS.</span><span class="sxs-lookup"><span data-stu-id="df8d2-117">This section contains topics that describe how to perform programming tasks by using the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="df8d2-118">Распространенные задачи по программированию цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="df8d2-118">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="df8d2-119">Инициализация диспетчера сигнатур</span><span class="sxs-lookup"><span data-stu-id="df8d2-119">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)  
    [<span data-ttu-id="df8d2-120">Подписать документ</span><span class="sxs-lookup"><span data-stu-id="df8d2-120">Sign a Document</span></span>](sign-a-document.md)  
    [<span data-ttu-id="df8d2-121">Добавление запроса подписи в документ XPS</span><span class="sxs-lookup"><span data-stu-id="df8d2-121">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)  
    [<span data-ttu-id="df8d2-122">Проверка подписей документов</span><span class="sxs-lookup"><span data-stu-id="df8d2-122">Verify Document Signatures</span></span>](verify-document-signatures.md)  
    </dl>
-   [<span data-ttu-id="df8d2-123">Дополнительные задачи по программированию цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="df8d2-123">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="df8d2-124">Загрузка сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="df8d2-124">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)  
    [<span data-ttu-id="df8d2-125">Убедитесь, что сертификат поддерживает метод подписи.</span><span class="sxs-lookup"><span data-stu-id="df8d2-125">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)  
    [<span data-ttu-id="df8d2-126">Проверка того, что система поддерживает метод дайджеста</span><span class="sxs-lookup"><span data-stu-id="df8d2-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)  
    [<span data-ttu-id="df8d2-127">Внедрение цепочек сертификатов в документ</span><span class="sxs-lookup"><span data-stu-id="df8d2-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a><span data-ttu-id="df8d2-128">Специальные примечания о программировании API цифровых подписей XPS</span><span class="sxs-lookup"><span data-stu-id="df8d2-128">Special Notes about XPS Digital Signature API Programming</span></span>

<span data-ttu-id="df8d2-129">В следующих разделах при использовании API цифровых подписей XPS необходимо учитывать некоторые особенности.</span><span class="sxs-lookup"><span data-stu-id="df8d2-129">The following topics require some special consideration when you use the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="df8d2-130">Проверка цифровых подписей в документе XPS</span><span class="sxs-lookup"><span data-stu-id="df8d2-130">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
-   [<span data-ttu-id="df8d2-131">Политика подписи цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="df8d2-131">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
-   [<span data-ttu-id="df8d2-132">Внедрение цепочки сертификатов</span><span class="sxs-lookup"><span data-stu-id="df8d2-132">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
-   [<span data-ttu-id="df8d2-133">Использование \_ структуры контекста CERT</span><span class="sxs-lookup"><span data-stu-id="df8d2-133">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a><span data-ttu-id="df8d2-134">Проверка цифровых подписей в документе XPS</span><span class="sxs-lookup"><span data-stu-id="df8d2-134">Verifying Digital Signatures in an XPS Document</span></span>

<span data-ttu-id="df8d2-135">[**Икспссигнатуре:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) проверяет только подписанное содержимое, чтобы определить, что оно не изменилось с момента подписания.</span><span class="sxs-lookup"><span data-stu-id="df8d2-135">[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) checks only the signed content to determine that it has not changed since it was signed.</span></span> <span data-ttu-id="df8d2-136">**Икспссигнатуре:: Verify** не проверяет сертификаты, которые использовались для подписания содержимого документа.</span><span class="sxs-lookup"><span data-stu-id="df8d2-136">**IXpsSignature::Verify** does not verify any of the certificates that were used to sign the document content.</span></span>

<span data-ttu-id="df8d2-137">Дополнительные сведения о сертификатах и криптографии см. в статье [о шифровании](/windows/desktop/SecCrypto/about-cryptography).</span><span class="sxs-lookup"><span data-stu-id="df8d2-137">For more information about certificates and cryptography, see [About Cryptography](/windows/desktop/SecCrypto/about-cryptography).</span></span>

<span data-ttu-id="df8d2-138">Пример проверки подписей документов в программе см. в разделе [Проверка подписей документов и сертификатов](verify-document-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="df8d2-138">For an example of how to verify document signatures in a program, see [Verify Document Signatures and Certificates](verify-document-signatures.md).</span></span>

### <a name="digital-signature-signing-policy"></a><span data-ttu-id="df8d2-139">Политика подписи цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="df8d2-139">Digital Signature Signing Policy</span></span>

<span data-ttu-id="df8d2-140">Политика подписи цифровых подписей определяет, какие части документа XPS подписаны.</span><span class="sxs-lookup"><span data-stu-id="df8d2-140">The digital signature signing policy determines which parts of an XPS document are signed.</span></span> <span data-ttu-id="df8d2-141">Одним из политик подписывания является подписывание связей подписей, начинающихся с части источника подписи.</span><span class="sxs-lookup"><span data-stu-id="df8d2-141">One signing policy option is to sign the signature relationships that start from the signature origin part.</span></span> <span data-ttu-id="df8d2-142">Так как связи сигнатур меняются при каждой добавляемой подписи, при добавлении новых подписей подписи, сделанные в этой политике, будут нарушены.</span><span class="sxs-lookup"><span data-stu-id="df8d2-142">Because the signature relationships change with each signature that is added, signatures that are made under this policy will break when new signatures are added.</span></span> <span data-ttu-id="df8d2-143">Убедитесь, что вы четко понимаете последствия и последствия установки этой политики. в противном случае может возникнуть непредвиденное или нежелательное поведение.</span><span class="sxs-lookup"><span data-stu-id="df8d2-143">Make sure that you understand clearly the implications and effects of setting this policy; otherwise, unexpected or undesired behavior might result.</span></span>

<span data-ttu-id="df8d2-144">Дополнительные сведения о политиках подписывания см. в статье о [**\_ \_ политике подписания XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).</span><span class="sxs-lookup"><span data-stu-id="df8d2-144">For more information about signing policies, see [**XPS\_SIGN\_POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).</span></span>

### <a name="embedding-a-certificate-chain"></a><span data-ttu-id="df8d2-145">Внедрение цепочки сертификатов</span><span class="sxs-lookup"><span data-stu-id="df8d2-145">Embedding a Certificate Chain</span></span>

<span data-ttu-id="df8d2-146">Сертификаты, составляющие цепочку доверия определенного сертификата, можно добавить в документ XPS.</span><span class="sxs-lookup"><span data-stu-id="df8d2-146">The certificates that make up the trust chain of a specific certificate can be added to an XPS document.</span></span> <span data-ttu-id="df8d2-147">Внедрение этих сертификатов упрощает работу в автономных сценариях, чтобы приложение проверяло сертификаты, используемые цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="df8d2-147">Embedding these certificates can make it easier, in off-line scenarios, for an application to verify the certificates that a digital signature uses.</span></span>

<span data-ttu-id="df8d2-148">Дополнительные сведения о внедрении сертификатов в документ XPS см. [в разделе внедрение цепочек сертификатов в документ](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="df8d2-148">For more information about how to embed certificates in an XPS document, see [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>

### <a name="using-the-cert_context-structure"></a><span data-ttu-id="df8d2-149">Использование \_ структуры контекста CERT</span><span class="sxs-lookup"><span data-stu-id="df8d2-149">Using the CERT\_CONTEXT Structure</span></span>

<span data-ttu-id="df8d2-150">[**\_ Контекст сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) и структуры [**\_ сведений о**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) сертификатах являются основными структурами данных, которые содержат сведения о сертификате.</span><span class="sxs-lookup"><span data-stu-id="df8d2-150">The [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) and [**CERT\_INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) structures are the main data structures that hold certificate information.</span></span> <span data-ttu-id="df8d2-151">Дополнительные сведения об использовании этих структур см. в разделе [использование \_ структуры данных о сертификатах](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span><span class="sxs-lookup"><span data-stu-id="df8d2-151">For more information about using these structures, see [Using a CERT\_INFO Data Structure](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span></span>

<span data-ttu-id="df8d2-152">[**Сертификат \_ Структуры контекста**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) , возвращаемые ФУНКЦИЯМИ API шифрования, должны освобождаться, если они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="df8d2-152">[**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures that are returned by Crypto API functions must be released when they are no longer needed.</span></span> <span data-ttu-id="df8d2-153">Чтобы освободить структуру **\_ контекста сертификата** , вызовите функцию [**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="df8d2-153">To release a **CERT\_CONTEXT** structure, call the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df8d2-154">См. также</span><span class="sxs-lookup"><span data-stu-id="df8d2-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df8d2-155">Распространенные задачи по программированию цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="df8d2-155">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="df8d2-156">Дополнительные задачи по программированию цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="df8d2-156">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="df8d2-157">**\_контекст сертификата**</span><span class="sxs-lookup"><span data-stu-id="df8d2-157">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="df8d2-158">**\_сведения о сертификате**</span><span class="sxs-lookup"><span data-stu-id="df8d2-158">**CERT\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[<span data-ttu-id="df8d2-159">**цертфрицертификатеконтекст**</span><span class="sxs-lookup"><span data-stu-id="df8d2-159">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="df8d2-160">**\_Политика подписывания XPS \_**</span><span class="sxs-lookup"><span data-stu-id="df8d2-160">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[<span data-ttu-id="df8d2-161">XPS</span><span class="sxs-lookup"><span data-stu-id="df8d2-161">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
