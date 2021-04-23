---
description: Таблица Мсидигиталсигнатуре содержит сведения о подписи для каждого объекта с цифровой подписью в базе данных установки.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Таблица Мсидигиталсигнатуре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650674"
---
# <a name="msidigitalsignature-table"></a><span data-ttu-id="026ff-103">Таблица Мсидигиталсигнатуре</span><span class="sxs-lookup"><span data-stu-id="026ff-103">MsiDigitalSignature Table</span></span>

<span data-ttu-id="026ff-104">Таблица Мсидигиталсигнатуре содержит сведения о подписи для каждого объекта с цифровой подписью в базе данных установки.</span><span class="sxs-lookup"><span data-stu-id="026ff-104">The MsiDigitalSignature table contains the signature information for every digitally signed object in the installation database.</span></span>

<span data-ttu-id="026ff-105">Таблицы Мсидигиталсигнатуре и [мсидигиталцертификате](msidigitalcertificate-table.md) доступны начиная с установщик Windows версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="026ff-105">The MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="026ff-106">Установщик Windows версия может использовать цифровые подписи в качестве средства для обнаружения поврежденных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="026ff-106">Windows Installer version can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="026ff-107">Установщик Windows 2,0 может проверять только цифровые подписи внешних ящиков и только с помощью таблиц Мсидигиталсигнатуре и [мсидигиталцертификате](msidigitalcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="026ff-107">Windows Installer 2.0 can only verify the digital signatures of external cabinets, and only by the use of the MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="026ff-108">Начиная с установщик Windows 3,0, установщик Windows может проверять цифровые подписи исправлений (MSP-файлы) с помощью таблиц [мсипатчцертификате](msipatchcertificate-table.md) и мсидигиталцертификате.</span><span class="sxs-lookup"><span data-stu-id="026ff-108">Beginning with Windows Installer 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="026ff-109">Дополнительные сведения см. в разделе [рекомендации по разработке безопасных установок](guidelines-for-authoring-secure-installations.md) и [исправления контроля учетных записей (UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="026ff-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="026ff-110">Таблица Мсидигиталсигнатуре содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="026ff-110">The MsiDigitalSignature table has the following columns.</span></span>



| <span data-ttu-id="026ff-111">Столбец</span><span class="sxs-lookup"><span data-stu-id="026ff-111">Column</span></span>               | <span data-ttu-id="026ff-112">Type</span><span class="sxs-lookup"><span data-stu-id="026ff-112">Type</span></span>                         | <span data-ttu-id="026ff-113">Ключ</span><span class="sxs-lookup"><span data-stu-id="026ff-113">Key</span></span> | <span data-ttu-id="026ff-114">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="026ff-114">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="026ff-115">Таблица</span><span class="sxs-lookup"><span data-stu-id="026ff-115">Table</span></span>                | [<span data-ttu-id="026ff-116">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="026ff-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="026ff-117">Да</span><span class="sxs-lookup"><span data-stu-id="026ff-117">Y</span></span>   | <span data-ttu-id="026ff-118">Нет</span><span class="sxs-lookup"><span data-stu-id="026ff-118">N</span></span>        |
| <span data-ttu-id="026ff-119">сигнобжект</span><span class="sxs-lookup"><span data-stu-id="026ff-119">SignObject</span></span>           | [<span data-ttu-id="026ff-120">Text</span><span class="sxs-lookup"><span data-stu-id="026ff-120">Text</span></span>](text.md)             | <span data-ttu-id="026ff-121">Да</span><span class="sxs-lookup"><span data-stu-id="026ff-121">Y</span></span>   | <span data-ttu-id="026ff-122">Нет</span><span class="sxs-lookup"><span data-stu-id="026ff-122">N</span></span>        |
| <span data-ttu-id="026ff-123">дигиталцертификате\_</span><span class="sxs-lookup"><span data-stu-id="026ff-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="026ff-124">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="026ff-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="026ff-125">Нет</span><span class="sxs-lookup"><span data-stu-id="026ff-125">N</span></span>   | <span data-ttu-id="026ff-126">Нет</span><span class="sxs-lookup"><span data-stu-id="026ff-126">N</span></span>        |
| <span data-ttu-id="026ff-127">Хэш</span><span class="sxs-lookup"><span data-stu-id="026ff-127">Hash</span></span>                 | [<span data-ttu-id="026ff-128">Двоичный</span><span class="sxs-lookup"><span data-stu-id="026ff-128">Binary</span></span>](binary.md)         | <span data-ttu-id="026ff-129">Нет</span><span class="sxs-lookup"><span data-stu-id="026ff-129">N</span></span>   | <span data-ttu-id="026ff-130">Да</span><span class="sxs-lookup"><span data-stu-id="026ff-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="026ff-131">Столбцы</span><span class="sxs-lookup"><span data-stu-id="026ff-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="026ff-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Таблица</span><span class="sxs-lookup"><span data-stu-id="026ff-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="026ff-133">В установщик Windows версии 2,0 запись в этом поле должна иметь значение "Media" для [таблицы Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="026ff-133">With the Windows Installer version 2.0, the entry in this field must be "Media" for the [Media table](media-table.md).</span></span> <span data-ttu-id="026ff-134">Установщик проверяет только цифровые подписи записей на внешних носителях CAB-файлов.</span><span class="sxs-lookup"><span data-stu-id="026ff-134">The installer only verifies the digital signatures on external cabinet media entries.</span></span> <span data-ttu-id="026ff-135">Этот столбец и столбец Сигнобжект вместе указывают ресурс с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="026ff-135">This column and the SignObject column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="026ff-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>сигнобжект</span><span class="sxs-lookup"><span data-stu-id="026ff-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span></span>
</dt> <dd>

<span data-ttu-id="026ff-137">Внешний ключ в первичный ключ таблицы, заданный столбцом таблицы.</span><span class="sxs-lookup"><span data-stu-id="026ff-137">A foreign key into the primary key of the table specified by the Table column.</span></span> <span data-ttu-id="026ff-138">Этот столбец и столбец таблицы вместе указывают ресурс с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="026ff-138">This column and the Table column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="026ff-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>дигиталцертификате\_</span><span class="sxs-lookup"><span data-stu-id="026ff-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span></span>
</dt> <dd>

<span data-ttu-id="026ff-140">Внешний ключ в [таблице мсидигиталцертификате](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="026ff-140">A foreign key into the [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="026ff-141">Определяет сертификат, который должен существовать в файле для того, чтобы связанное действие было успешным.</span><span class="sxs-lookup"><span data-stu-id="026ff-141">This identifies the certificate that must exist on the file for the associated action to succeed.</span></span> <span data-ttu-id="026ff-142">Ресурс (или объект) всегда должен соответствовать этому сертификату в таблице Мсидигиталцертификате.</span><span class="sxs-lookup"><span data-stu-id="026ff-142">The resource (or object) is always required to match this certificate in the MsiDigitalCertificate table.</span></span>

</dd> <dt>

<span data-ttu-id="026ff-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Функции</span><span class="sxs-lookup"><span data-stu-id="026ff-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash</span></span>
</dt> <dd>

<span data-ttu-id="026ff-144">В этом поле введите ссылочный хэш ресурса (или объекта), который должен быть проверен на соответствие фактического хэша ресурса (или объекта), полученного во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="026ff-144">In this field enter the reference hash of the resource (or object) that is to be checked against the actual hash of the resource (or object) obtained at run-time.</span></span> <span data-ttu-id="026ff-145">Если необходимо проверить только сертификат, хэш-поле может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="026ff-145">If only the certificate needs to be verified, the Hash field may be null.</span></span> <span data-ttu-id="026ff-146">Обратите внимание, что формат хэша зависит от типа подписанного ресурса (или объекта).</span><span class="sxs-lookup"><span data-stu-id="026ff-146">Note that the format of the hash depends on the type of the resource (or object) being signed.</span></span>

<span data-ttu-id="026ff-147">Хэш-столбец содержит двоичное представление хэша.</span><span class="sxs-lookup"><span data-stu-id="026ff-147">The Hash column contains the binary representation of the hash.</span></span> <span data-ttu-id="026ff-148">Реальное содержимое является членом **pbData** структуры [**\_ \_ BLOB-объекта шифрования**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , которая является частью структуры **\_ больших двоичных объектов CRYPTOAPI** .</span><span class="sxs-lookup"><span data-stu-id="026ff-148">The actual content is the **pbData** member of the [**CRYPT\_HASH\_BLOB**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure, which is part of the **CRYPTOAPI\_BLOB** structure.</span></span> <span data-ttu-id="026ff-149">Это можно получить путем вызова [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) или [**мсижетфилесигнатуреинформатион**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span><span class="sxs-lookup"><span data-stu-id="026ff-149">This may be obtained by calling [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) or [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="026ff-150">Проверка</span><span class="sxs-lookup"><span data-stu-id="026ff-150">Validation</span></span>

<dl>

[<span data-ttu-id="026ff-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="026ff-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="026ff-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="026ff-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="026ff-153">ICE29</span><span class="sxs-lookup"><span data-stu-id="026ff-153">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="026ff-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="026ff-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="026ff-155">ICE66</span><span class="sxs-lookup"><span data-stu-id="026ff-155">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="026ff-156">ICE81</span><span class="sxs-lookup"><span data-stu-id="026ff-156">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="026ff-157">См. также</span><span class="sxs-lookup"><span data-stu-id="026ff-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="026ff-158">**мсижетфилесигнатуреинформатион**</span><span class="sxs-lookup"><span data-stu-id="026ff-158">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="026ff-159">Таблица Мсидигиталцертификате</span><span class="sxs-lookup"><span data-stu-id="026ff-159">MsiDigitalCertificate table</span></span>](msidigitalcertificate-table.md)
</dt> <dt>

[<span data-ttu-id="026ff-160">Цифровые подписи и установщик Windows</span><span class="sxs-lookup"><span data-stu-id="026ff-160">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
