---
description: В таблице Мсидигиталцертификате хранятся сертификаты в двоичном формате потока и каждый сертификат связывается с первичным ключом.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Таблица Мсидигиталцертификате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4765dee433cfab989e79c7ef4663d8939381ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812712"
---
# <a name="msidigitalcertificate-table"></a><span data-ttu-id="f3418-103">Таблица Мсидигиталцертификате</span><span class="sxs-lookup"><span data-stu-id="f3418-103">MsiDigitalCertificate Table</span></span>

<span data-ttu-id="f3418-104">В таблице Мсидигиталцертификате хранятся сертификаты в двоичном формате потока и каждый сертификат связывается с первичным ключом.</span><span class="sxs-lookup"><span data-stu-id="f3418-104">The MsiDigitalCertificate table stores certificates in binary stream format and associates each certificate with a primary key.</span></span> <span data-ttu-id="f3418-105">Первичный ключ используется для обмена сертификатами между несколькими объектами с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="f3418-105">The primary key is used to share certificates among multiple digitally signed objects.</span></span> <span data-ttu-id="f3418-106">Цифровой сертификат — это учетные данные, которые предоставляют средства для проверки удостоверения.</span><span class="sxs-lookup"><span data-stu-id="f3418-106">A digital certificate is a credential that provides a means to verify identity.</span></span> <span data-ttu-id="f3418-107">Дополнительные сведения см. в статье [цифровые сертификаты](../seccrypto/digital-certificates.md) в разделе [Криптография](../seccrypto/cryptography-portal.md) пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f3418-107">For more information, see [Digital Certificates](../seccrypto/digital-certificates.md) in the [Cryptography](../seccrypto/cryptography-portal.md) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="f3418-108">Таблицы [мсидигиталсигнатуре](msidigitalsignature-table.md) и мсидигиталцертификате доступны начиная с установщик Windows версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="f3418-108">The [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="f3418-109">Установщик Windows могут использовать цифровые подписи в качестве средства для обнаружения поврежденных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3418-109">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="f3418-110">Установщик Windows версии 2,0 может проверять только цифровые подписи внешних ящиков и только с помощью таблиц [мсидигиталсигнатуре](msidigitalsignature-table.md) и мсидигиталцертификате.</span><span class="sxs-lookup"><span data-stu-id="f3418-110">Windows Installer version 2.0 can only verify the digital signatures of external cabinets, and only by the use of the [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables.</span></span>

<span data-ttu-id="f3418-111">Начиная с версии установщик Windows 3,0, установщик Windows может проверять цифровые подписи исправлений (MSP-файлы) с помощью таблиц [мсипатчцертификате](msipatchcertificate-table.md) и мсидигиталцертификате.</span><span class="sxs-lookup"><span data-stu-id="f3418-111">Beginning with Windows Installer version 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="f3418-112">Дополнительные сведения см. в разделе [рекомендации по разработке безопасных установок](guidelines-for-authoring-secure-installations.md) и [исправления контроля учетных записей (UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="f3418-112">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="f3418-113">Таблица Мсидигиталцертификате содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="f3418-113">The MsiDigitalCertificate table has the following columns.</span></span>



| <span data-ttu-id="f3418-114">Столбец</span><span class="sxs-lookup"><span data-stu-id="f3418-114">Column</span></span>             | <span data-ttu-id="f3418-115">Type</span><span class="sxs-lookup"><span data-stu-id="f3418-115">Type</span></span>                         | <span data-ttu-id="f3418-116">Ключ</span><span class="sxs-lookup"><span data-stu-id="f3418-116">Key</span></span> | <span data-ttu-id="f3418-117">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="f3418-117">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="f3418-118">дигиталцертификате</span><span class="sxs-lookup"><span data-stu-id="f3418-118">DigitalCertificate</span></span> | [<span data-ttu-id="f3418-119">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="f3418-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="f3418-120">Да</span><span class="sxs-lookup"><span data-stu-id="f3418-120">Y</span></span>   | <span data-ttu-id="f3418-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f3418-121">N</span></span>        |
| <span data-ttu-id="f3418-122">цертдата</span><span class="sxs-lookup"><span data-stu-id="f3418-122">CertData</span></span>           | [<span data-ttu-id="f3418-123">Двоичный</span><span class="sxs-lookup"><span data-stu-id="f3418-123">Binary</span></span>](binary.md)         | <span data-ttu-id="f3418-124">Нет</span><span class="sxs-lookup"><span data-stu-id="f3418-124">N</span></span>   | <span data-ttu-id="f3418-125">Нет</span><span class="sxs-lookup"><span data-stu-id="f3418-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f3418-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="f3418-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f3418-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>дигиталцертификате</span><span class="sxs-lookup"><span data-stu-id="f3418-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="f3418-128">Идентифицирует сертификат цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="f3418-128">Identifies the digital signature certificate.</span></span> <span data-ttu-id="f3418-129">Первичный ключ таблицы.</span><span class="sxs-lookup"><span data-stu-id="f3418-129">Primary key of table.</span></span>

</dd> <dt>

<span data-ttu-id="f3418-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>цертдата</span><span class="sxs-lookup"><span data-stu-id="f3418-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span></span>
</dt> <dd>

<span data-ttu-id="f3418-131">Двоичное представление цифрового сертификата.</span><span class="sxs-lookup"><span data-stu-id="f3418-131">The binary representation of the digital certificate.</span></span> <span data-ttu-id="f3418-132">Столбец Цертдата содержит закодированный байтовый массив контекста сертификата.</span><span class="sxs-lookup"><span data-stu-id="f3418-132">The CertData column contains the encoded byte array of a certificate context.</span></span> <span data-ttu-id="f3418-133">Это элемент **пбцертенкодед** структуры [**\_ контекста CERT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="f3418-133">This is the **pbCertEncoded** member of the [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="f3418-134">Контекст сертификата можно получить, вызвав [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**мсижетфилесигнатуреинформатион**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)или импортировав CER-файл.</span><span class="sxs-lookup"><span data-stu-id="f3418-134">The certificate context can be obtained by calling [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), or by importing a .cer file.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="f3418-135">Проверка</span><span class="sxs-lookup"><span data-stu-id="f3418-135">Validation</span></span>

<dl>

[<span data-ttu-id="f3418-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="f3418-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f3418-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="f3418-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f3418-138">ICE29</span><span class="sxs-lookup"><span data-stu-id="f3418-138">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="f3418-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="f3418-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f3418-140">ICE66</span><span class="sxs-lookup"><span data-stu-id="f3418-140">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="f3418-141">ICE81</span><span class="sxs-lookup"><span data-stu-id="f3418-141">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="f3418-142">См. также</span><span class="sxs-lookup"><span data-stu-id="f3418-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3418-143">**мсижетфилесигнатуреинформатион**</span><span class="sxs-lookup"><span data-stu-id="f3418-143">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="f3418-144">Таблица Мсидигиталсигнатуре</span><span class="sxs-lookup"><span data-stu-id="f3418-144">MsiDigitalSignature table</span></span>](msidigitalsignature-table.md)
</dt> <dt>

[<span data-ttu-id="f3418-145">Цифровые подписи и установщик Windows</span><span class="sxs-lookup"><span data-stu-id="f3418-145">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
