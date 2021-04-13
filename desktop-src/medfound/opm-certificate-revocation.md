---
description: .
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Отзыв сертификата ОПМ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b20dc00b0bd23644ef9dca22558a304ca9438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543879"
---
# <a name="opm-certificate-revocation"></a><span data-ttu-id="d6de4-103">Отзыв сертификата ОПМ</span><span class="sxs-lookup"><span data-stu-id="d6de4-103">OPM Certificate Revocation</span></span>

<span data-ttu-id="d6de4-104">Сертификат диспетчера выходной защиты (ОПМ) может быть отозван корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d6de4-104">An output protection manager (OPM) certificate can be revoked by Microsoft.</span></span> <span data-ttu-id="d6de4-105">Список отозванных сертификатов хранится в глобальном списке отзыва (GRL).</span><span class="sxs-lookup"><span data-stu-id="d6de4-105">The list of revoked certificates is stored in a global revocation list (GRL).</span></span> <span data-ttu-id="d6de4-106">GRL имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="d6de4-106">The GRL has the following format:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6de4-107">Section</span><span class="sxs-lookup"><span data-stu-id="d6de4-107">Section</span></span></th>
<th><span data-ttu-id="d6de4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d6de4-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6de4-109">Header</span><span class="sxs-lookup"><span data-stu-id="d6de4-109">Header</span></span></td>
<td><span data-ttu-id="d6de4-110">Структура <a href="grl-header.md"><strong>GRL_HEADER</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d6de4-110">A <a href="grl-header.md"><strong>GRL_HEADER</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6de4-111">Основные сведения</span><span class="sxs-lookup"><span data-stu-id="d6de4-111">Core</span></span></td>
<td><span data-ttu-id="d6de4-112">Содержит следующие списки отзыва:</span><span class="sxs-lookup"><span data-stu-id="d6de4-112">Contains the following revocation lists:</span></span>
<ul>
<li><span data-ttu-id="d6de4-113">Двоичные вызовы ядра</span><span class="sxs-lookup"><span data-stu-id="d6de4-113">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="d6de4-114">Двоичные отзыва пользовательского режима</span><span class="sxs-lookup"><span data-stu-id="d6de4-114">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="d6de4-115">Отзыв сертификатов</span><span class="sxs-lookup"><span data-stu-id="d6de4-115">Certificate revocations</span></span></li>
<li><span data-ttu-id="d6de4-116">Доверенные корни (зарезервированные)</span><span class="sxs-lookup"><span data-stu-id="d6de4-116">Trusted roots (reserved)</span></span></li>
</ul>
<span data-ttu-id="d6de4-117">Список доверенных корневых каталогов в настоящее время не используется и зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="d6de4-117">The list of trusted roots is currently not used, and is reserved for future use.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6de4-118">Расширяемые записи</span><span class="sxs-lookup"><span data-stu-id="d6de4-118">Extensible entries</span></span></td>
<td><span data-ttu-id="d6de4-119">Содержит сведения, используемые другими компонентами.</span><span class="sxs-lookup"><span data-stu-id="d6de4-119">Contains information used by other components.</span></span> <span data-ttu-id="d6de4-120">Этот раздел не относится к ОПМ.</span><span class="sxs-lookup"><span data-stu-id="d6de4-120">This section is not relevant to OPM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6de4-121">Обновления</span><span class="sxs-lookup"><span data-stu-id="d6de4-121">Renewals:</span></span></td>
<td><span data-ttu-id="d6de4-122">Содержит идентификаторы GUID, определяющие идентификаторы Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="d6de4-122">Contains GUIDs that define Windows Update identifiers.</span></span> <span data-ttu-id="d6de4-123">Этот раздел содержит идентификаторы для следующих списков.</span><span class="sxs-lookup"><span data-stu-id="d6de4-123">This section contains identifiers for the following lists:</span></span>
<ul>
<li><span data-ttu-id="d6de4-124">Двоичные вызовы ядра</span><span class="sxs-lookup"><span data-stu-id="d6de4-124">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="d6de4-125">Двоичные отзыва пользовательского режима</span><span class="sxs-lookup"><span data-stu-id="d6de4-125">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="d6de4-126">Отзыв сертификатов</span><span class="sxs-lookup"><span data-stu-id="d6de4-126">Certificate revocations</span></span></li>
</ul>
<span data-ttu-id="d6de4-127">Приложение может использовать эти идентификаторы для запроса обновленной версии отозванного двоичного файла, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="d6de4-127">An application can use these identifiers to request a renewed version of a revoked binary, if one is available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6de4-128">Подпись: раздел Core</span><span class="sxs-lookup"><span data-stu-id="d6de4-128">Signature: Core section</span></span></td>
<td><span data-ttu-id="d6de4-129">Подписывает разделы заголовка и ядра.</span><span class="sxs-lookup"><span data-stu-id="d6de4-129">Signs the header and core sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6de4-130">Сигнатура: расширяемый раздел</span><span class="sxs-lookup"><span data-stu-id="d6de4-130">Signature: Extensible section</span></span></td>
<td><span data-ttu-id="d6de4-131">Подписывает заголовки и расширяемые разделы.</span><span class="sxs-lookup"><span data-stu-id="d6de4-131">Signs the header and extensible sections.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d6de4-132">Заголовок GRL — это структура [**\_ заголовка GRL**](grl-header.md) .</span><span class="sxs-lookup"><span data-stu-id="d6de4-132">The GRL header is a [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="d6de4-133">Элемент **двсекуенценумбер** структуры содержит номер версии GRL.</span><span class="sxs-lookup"><span data-stu-id="d6de4-133">The **dwSequenceNumber** member of the structure contains the GRL version number.</span></span> <span data-ttu-id="d6de4-134">Это число увеличивается при каждом обновлении GRL и последующей версии, размещенной на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="d6de4-134">This number is incremented whenever the GRL is updated and a new version placed on the user's computer.</span></span>

<span data-ttu-id="d6de4-135">Отозванные сертификаты ОПМ перечислены в списке отзыва сертификатов в разделе Основные.</span><span class="sxs-lookup"><span data-stu-id="d6de4-135">Revoked OPM certificates are listed in the certificate revocations list of the Core section.</span></span> <span data-ttu-id="d6de4-136">Каждая основная запись в GRL — это 20-байтовый массив, который содержит хэш SHA-1 открытого ключа отозванного сертификата.</span><span class="sxs-lookup"><span data-stu-id="d6de4-136">Each Core entry in the GRL is a 20-byte array that contains the SHA-1 hash of the public key of the revoked certificate.</span></span>

<span data-ttu-id="d6de4-137">Разделы подписей содержат подписи, которые можно использовать для проверки того, что GRL не был изменен.</span><span class="sxs-lookup"><span data-stu-id="d6de4-137">The Signature sections contains signatures that can be used to verify that the GRL has not been tampered with.</span></span> <span data-ttu-id="d6de4-138">Каждая из разделов подписей [**содержит \_ MF**](mf-signature.md) .</span><span class="sxs-lookup"><span data-stu-id="d6de4-138">Each Signature sections contains am [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="d6de4-139">Первая сигнатура подписывает заголовок и основной раздел.</span><span class="sxs-lookup"><span data-stu-id="d6de4-139">The first signature signs the header plus the Core section.</span></span> <span data-ttu-id="d6de4-140">Вторая сигнатура подписывает заголовок и расширяемый раздел; Эта сигнатура не относится к ОПМ.</span><span class="sxs-lookup"><span data-stu-id="d6de4-140">The second signature signs the header plus the Extensible section; this signature is not relevant to OPM.</span></span>

<span data-ttu-id="d6de4-141">Чтобы убедиться, что сам GRL не был изменен, проверьте сигнатуру следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d6de4-141">To ensure that the GRL itself has not been tampered with, verify the signature as follows:</span></span>

1.  <span data-ttu-id="d6de4-142">Найдите начало структуры [**\_ сигнатуры MF**](mf-signature.md) .</span><span class="sxs-lookup"><span data-stu-id="d6de4-142">Find the start of the [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="d6de4-143">Расположение структуры **\_ сигнатуры MF** указывается в элементе **кбсигнатурекореоффсет** структуры [**\_ заголовка GRL**](grl-header.md) .</span><span class="sxs-lookup"><span data-stu-id="d6de4-143">The location of the **MF\_SIGNATURE** structure is given in the **cbSignatureCoreOffset** member of the [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="d6de4-144">Расположение указывается в виде смещения в байтах от начала GRL.</span><span class="sxs-lookup"><span data-stu-id="d6de4-144">The location is specified as an offset in bytes from the start of the GRL.</span></span>
2.  <span data-ttu-id="d6de4-145">Проанализируйте [**структуру \_ сигнатуры MF**](mf-signature.md) как \# подпись PKCS 7 с цепочкой сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d6de4-145">Parse the [**MF\_SIGNATURE**](mf-signature.md) structure as a PKCS \#7 signature with a certificate chain.</span></span>
3.  <span data-ttu-id="d6de4-146">Проверьте цепочку сертификатов до доверенного корня.</span><span class="sxs-lookup"><span data-stu-id="d6de4-146">Verify the certificate chain up to a trusted root.</span></span>
4.  <span data-ttu-id="d6de4-147">Убедитесь, что конечный сертификат имеет следующий идентификатор объекта в EKU: "1.3.6.1.4.1.311.10.5.4".</span><span class="sxs-lookup"><span data-stu-id="d6de4-147">Verify that the leaf certificate has the following object identifier in the EKU: "1.3.6.1.4.1.311.10.5.4".</span></span>
5.  <span data-ttu-id="d6de4-148">Вычислите хэш байтов, содержащих заголовок, и основные разделы GRL.</span><span class="sxs-lookup"><span data-stu-id="d6de4-148">Compute a hash of the bytes that include the header and the core sections of the GRL.</span></span>
6.  <span data-ttu-id="d6de4-149">Убедитесь, что хэш совпадает с подписью в конечном сертификате.</span><span class="sxs-lookup"><span data-stu-id="d6de4-149">Verify that the hash matches the signature in the leaf certificate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6de4-150">См. также</span><span class="sxs-lookup"><span data-stu-id="d6de4-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6de4-151">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="d6de4-151">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="d6de4-152">**\_заголовок GRL**</span><span class="sxs-lookup"><span data-stu-id="d6de4-152">**GRL\_HEADER**</span></span>](grl-header.md)
</dt> <dt>

[<span data-ttu-id="d6de4-153">**\_подпись MF**</span><span class="sxs-lookup"><span data-stu-id="d6de4-153">**MF\_SIGNATURE**</span></span>](mf-signature.md)
</dt> </dl>

 

 



