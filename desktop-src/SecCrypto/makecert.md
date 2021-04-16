---
description: Создает сертификат X. 509, подписанный с помощью тестового корневого ключа или другого указанного ключа, который привязывает ваше имя к открытой части пары ключей. Сертификат сохраняется в файл, в хранилище системных сертификатов или в обоих случаях.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: Программой
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980ba379688f2dc61c44b06d66ed5255e5b2e988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682779"
---
# <a name="makecert"></a><span data-ttu-id="5b0ea-104">Программой</span><span class="sxs-lookup"><span data-stu-id="5b0ea-104">MakeCert</span></span>

> [!Note]  
> <span data-ttu-id="5b0ea-105">Мы не рекомендуем использовать MakeCert.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-105">MakeCert is deprecated.</span></span> <span data-ttu-id="5b0ea-106">Чтобы создать самозаверяющие сертификаты, используйте командлет PowerShell [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span><span class="sxs-lookup"><span data-stu-id="5b0ea-106">To create self-signed certificates, use the Powershell Cmdlet [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span></span>

 

<span data-ttu-id="5b0ea-107">Средство MakeCert создает сертификат [*X. 509*](../secgloss/x-gly.md) , подписанный с помощью тестового корневого ключа или другого указанного ключа, который привязывает ваше имя к открытой части пары ключей.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-107">The MakeCert tool creates an [*X.509*](../secgloss/x-gly.md) certificate, signed by the test root key or other specified key, that binds your name to the public part of the key pair.</span></span> <span data-ttu-id="5b0ea-108">Сертификат сохраняется в файл, в хранилище системных сертификатов или в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-108">The certificate is saved to a file, a system certificate store, or both.</span></span> <span data-ttu-id="5b0ea-109">Средство устанавливается в \\ папку bin пути установки пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-109">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="5b0ea-110">Средство MakeCert использует следующий синтаксис команды:</span><span class="sxs-lookup"><span data-stu-id="5b0ea-110">The MakeCert tool uses the following command syntax:</span></span>

<span data-ttu-id="5b0ea-111">**MakeCert** \[ *Басикоптионс* \| *Екстендедоптионс* \] *Выходной_файл*</span><span class="sxs-lookup"><span data-stu-id="5b0ea-111">**MakeCert** \[*BasicOptions*\|*ExtendedOptions*\] *OutputFile*</span></span>

<span data-ttu-id="5b0ea-112">*Выходной_файл* — это имя файла, в который будет записан сертификат.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-112">*OutputFile* is the name of the file where the certificate will be written.</span></span> <span data-ttu-id="5b0ea-113">Если сертификат не должен записываться в файл, можно опустить *выходной_файл* .</span><span class="sxs-lookup"><span data-stu-id="5b0ea-113">You can omit *OutputFile* if the certificate is not to be written to a file.</span></span>

## <a name="options"></a><span data-ttu-id="5b0ea-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b0ea-114">Options</span></span>

<span data-ttu-id="5b0ea-115">В состав MakeCert входят базовые и расширенные параметры.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-115">MakeCert includes basic and extended options.</span></span> <span data-ttu-id="5b0ea-116">Основные параметры используются при создании сертификатов чаще всего.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-116">Basic options are those most commonly used to create a certificate.</span></span> <span data-ttu-id="5b0ea-117">Дополнительные параметры обеспечивают более гибкое использование программы.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-117">Extended options provide more flexibility.</span></span>

<span data-ttu-id="5b0ea-118">Параметры для MakeCert также делятся на три функциональные группы:</span><span class="sxs-lookup"><span data-stu-id="5b0ea-118">The options for MakeCert are also divided into three functional groups:</span></span>

-   <span data-ttu-id="5b0ea-119">Основные параметры, относящиеся только к технологии хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-119">Basic options specific to certificate store technology only.</span></span>
-   <span data-ttu-id="5b0ea-120">Расширенные параметры, характерные только для технологии SPC-File и закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-120">Extended options specific to SPC-file and private key technology only.</span></span>
-   <span data-ttu-id="5b0ea-121">Расширенные параметры, применимые к технологии файлов SPC, закрытого ключа и хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-121">Extended options applicable to SPC-file, private key, and certificate store technology.</span></span>

<span data-ttu-id="5b0ea-122">Параметры, приведенные в следующих таблицах, можно использовать только в Internet Explorer 4,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-122">Options given in the following tables can be used only with Internet Explorer 4.0 or later.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b0ea-123">Базовый параметр</span><span class="sxs-lookup"><span data-stu-id="5b0ea-123">Basic option</span></span></th>
<th><span data-ttu-id="5b0ea-124">Описание</span><span class="sxs-lookup"><span data-stu-id="5b0ea-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b0ea-125"><strong>-a</strong> <strong></strong> <em>Алгоритм</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-125"><strong>-a</strong> <strong></strong> <em>Algorithm</em></span></span></td>
<td><span data-ttu-id="5b0ea-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Хэш-</em></a> алгоритм.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> algorithm.</span></span> <span data-ttu-id="5b0ea-127">Необходимо задать значение <strong>SHA-1</strong> или <strong>MD5</strong> (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="5b0ea-127">Must be set to either <strong>SHA-1</strong> or <strong>MD5</strong> (default).</span></span> <span data-ttu-id="5b0ea-128">Сведения о MD5 см. в разделе <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-128">For information about MD5, see <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-129"><strong>-б</strong> <strong></strong> <em>DateStart</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span></span></td>
<td><span data-ttu-id="5b0ea-130">Дата, когда сертификат был первым действителен.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-130">Date the certificate first becomes valid.</span></span> <span data-ttu-id="5b0ea-131">Значение по умолчанию — при создании сертификата.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-131">The default is when the certificate is created.</span></span> <span data-ttu-id="5b0ea-132">Формат <em>DateStart</em> — mm/дд/гггг.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-132">The format of <em>DateStart</em> is mm/dd/yyyy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-133"><strong>-CY</strong> <strong></strong> <em>Цертификатетипес</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span></span></td>
<td><span data-ttu-id="5b0ea-134">Тип сертификата.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-134">Certificate type.</span></span> <span data-ttu-id="5b0ea-135"><em>Цертификатетипес</em> может быть <strong>закончена</strong> для конечного субъекта или <strong>центра</strong> <a href="/windows/desktop/SecGloss/c-gly"><em>сертификации</em></a>.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-135"><em>CertificateTypes</em> can be <strong>end</strong> for end-entity, or <strong>authority</strong> for <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span></span></td>
<td><span data-ttu-id="5b0ea-137">Дата окончания периода действия.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-137">Date when the validity period ends.</span></span> <span data-ttu-id="5b0ea-138">Значение по умолчанию — год 2039.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-138">The default is the year 2039.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-139"><strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</span><span class="sxs-lookup"><span data-stu-id="5b0ea-139"><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> …</span></span></td>
<td><span data-ttu-id="5b0ea-140">Вставляет в сертификат список из одного или нескольких <a href="/windows/desktop/SecGloss/e-gly"><em></em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>идентификаторов объектов</em></a> с разделителями-запятыми (OID).</span><span class="sxs-lookup"><span data-stu-id="5b0ea-140">Inserts a list of one or more comma-separated, <a href="/windows/desktop/SecGloss/e-gly"><em>enhanced key usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>object identifiers</em></a> (OIDs) into the certificate.</span></span> <span data-ttu-id="5b0ea-141">Например, параметр <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> вставляет OID проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-141">For example, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserts the client authentication OID.</span></span> <span data-ttu-id="5b0ea-142">Определения допустимых OID см. в файле Винкрипт. h в CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-142">For definitions of allowable OIDs, see the Wincrypt.h file in CryptoAPI 2.0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-143"><strong>-h</strong> <strong></strong> <em>Нумчилдрен</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span></span></td>
<td><span data-ttu-id="5b0ea-144">Максимальная высота дерева ниже этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-144">Maximum height of the tree below this certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-145"><strong>-l</strong> <strong></strong> <em>Полицилинк</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span></span></td>
<td><span data-ttu-id="5b0ea-146">Ссылка на сведения о политике Агентства SPC (например, URL-адрес).</span><span class="sxs-lookup"><span data-stu-id="5b0ea-146">Link to SPC agency policy information (for example, a URL).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-147"><strong>-m</strong> <strong></strong> <em>нмонсс</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span></span></td>
<td><span data-ttu-id="5b0ea-148">Длительность периода действия.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-148">Duration of the validity period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-149"><strong>-n</strong> <strong>&quot;</strong> <em>Имя</em><strong>&quot;</strong></span><span class="sxs-lookup"><span data-stu-id="5b0ea-149"><strong>-n</strong> <strong>&quot;</strong><em>Name</em><strong>&quot;</strong></span></span></td>
<td><span data-ttu-id="5b0ea-150">Имя сертификата издателя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-150">Name for the publisher's certificate.</span></span> <span data-ttu-id="5b0ea-151">Это имя должно соответствовать стандарту <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> .</span><span class="sxs-lookup"><span data-stu-id="5b0ea-151">This name must conform to the <a href="/windows/desktop/SecGloss/x-gly"><em>X.500</em></a> standard.</span></span> <span data-ttu-id="5b0ea-152">Самый простой способ — использовать &quot; Формат CN =<em>myname</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="5b0ea-152">The simplest method is to use the &quot;CN=<em>MyName</em>&quot; format.</span></span> <span data-ttu-id="5b0ea-153">Например: <strong>-n &quot; CN = test &quot; </strong>.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-153">For example: <strong>-n &quot;CN=Test&quot;</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-154"><strong>-НСКП</strong></span><span class="sxs-lookup"><span data-stu-id="5b0ea-154"><strong>-nscp</strong></span></span></td>
<td><span data-ttu-id="5b0ea-155">Необходимо добавить модуль проверки подлинности клиента Netscape.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-155">The Netscape client authentication extension should be included.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-156"><strong>-PE</strong></span><span class="sxs-lookup"><span data-stu-id="5b0ea-156"><strong>-pe</strong></span></span></td>
<td><span data-ttu-id="5b0ea-157">Помечает закрытый ключ как экспортируемый.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-157">Marks the private key as exportable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-158"><strong>-r</strong></span><span class="sxs-lookup"><span data-stu-id="5b0ea-158"><strong>-r</strong></span></span></td>
<td><span data-ttu-id="5b0ea-159">создает самозаверяющий сертификат;</span><span class="sxs-lookup"><span data-stu-id="5b0ea-159">Creates a self-signed certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-160"><strong>-SC</strong> <strong></strong> <em>Субжектцертфиле</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span></span></td>
<td><span data-ttu-id="5b0ea-161">Имя файла сертификата с существующим открытым ключом субъекта для использования.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-161">Certificate file name with the existing subject public key to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-162"><strong>-SK</strong> <strong></strong> <em>Субжекткэй</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-162"><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></span></span></td>
<td><span data-ttu-id="5b0ea-163">Расположение контейнера ключей субъекта, содержащего <a href="/windows/desktop/SecGloss/p-gly"><em>закрытый ключ</em></a>.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-163">Location of the subject's key container which holds the <a href="/windows/desktop/SecGloss/p-gly"><em>private key</em></a>.</span></span> <span data-ttu-id="5b0ea-164">Если контейнер ключей не существует, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-164">If a key container does not exist, one is created.</span></span> <span data-ttu-id="5b0ea-165">Если ни один из параметров <strong>-SK</strong> или <strong>-SV</strong> не используется, по умолчанию создается и используется контейнер ключей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-165">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-166"><strong>-Небесный</strong> <strong></strong> <em>Субжекткэйспек</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span></span></td>
<td><span data-ttu-id="5b0ea-167">Спецификация ключа субъекта.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-167">Subject's key specification.</span></span> <span data-ttu-id="5b0ea-168"><em>Субжекткэйспек</em> должно иметь одно из трех возможных значений:</span><span class="sxs-lookup"><span data-stu-id="5b0ea-168"><em>SubjectKeySpec</em> must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="5b0ea-169"><strong>Signature</strong> (спецификация ключа AT_SIGNATURE)</span><span class="sxs-lookup"><span data-stu-id="5b0ea-169"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="5b0ea-170"><strong>Exchange</strong> (спецификация ключа AT_KEYEXCHANGE)</span><span class="sxs-lookup"><span data-stu-id="5b0ea-170"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="5b0ea-171">Целое число, например <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="5b0ea-171">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="5b0ea-172">Дополнительные сведения см. в заметке, следующей за таблицей.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-172">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-173"><strong>— SP</strong> <strong></strong> <em>Субжектпровидернаме</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span></span></td>
<td><span data-ttu-id="5b0ea-174">Поставщик CryptoAPI для субъекта.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-174">CryptoAPI provider for subject.</span></span> <span data-ttu-id="5b0ea-175">По умолчанию используется поставщик пользователя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-175">The default is the user's provider.</span></span> <span data-ttu-id="5b0ea-176">Дополнительные сведения о поставщиках CryptoAPI см. в документации по CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-176">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-177"><strong>-SR</strong> <strong></strong> <em>Субжектцертсторелокатион</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span></span></td>
<td><span data-ttu-id="5b0ea-178">Расположение в реестре хранилища сертификатов субъекта.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-178">Registry location of the subject's certificate store.</span></span> <span data-ttu-id="5b0ea-179"><em>Субжектцертсторелокатион</em> должен иметь значение <strong>LocalMachine</strong> (раздел реестра HKEY_LOCAL_MACHINE) или <strong>CurrentUser</strong> (раздел реестра HKEY_CURRENT_USER).</span><span class="sxs-lookup"><span data-stu-id="5b0ea-179"><em>SubjectCertStoreLocation</em> must be either <strong>LocalMachine</strong> (registry key HKEY_LOCAL_MACHINE) or <strong>CurrentUser</strong> (registry key HKEY_CURRENT_USER).</span></span> <span data-ttu-id="5b0ea-180">Параметр <strong>CurrentUser</strong> используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-180"><strong>CurrentUser</strong> is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-181"><strong>-СС</strong> <strong></strong> <em>Субжектцертсторенаме</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span></span></td>
<td><span data-ttu-id="5b0ea-182">Имя хранилища сертификатов субъекта, в котором будет сохранен созданный сертификат.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-182">Name of the subject's certificate store where the generated certificate will be stored.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-183"><strong>-ОКП</strong> <strong></strong> <em>Субжекткэйфиле</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span></span></td>
<td><span data-ttu-id="5b0ea-184">Имя файла. PVK субъекта.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-184">Name of the subject's .pvk file.</span></span> <span data-ttu-id="5b0ea-185">Если ни один из параметров <strong>-SK</strong> или <strong>-SV</strong> не используется, по умолчанию создается и используется контейнер ключей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-185">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-186"><strong>-SY</strong> <strong></strong> <em>нсубжектпровидертипе</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span></span></td>
<td><span data-ttu-id="5b0ea-187">Тип поставщика CryptoAPI для субъекта.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-187">CryptoAPI provider type for subject.</span></span> <span data-ttu-id="5b0ea-188">Значение по умолчанию — <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-188">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="5b0ea-189">Дополнительные сведения о типах поставщиков CryptoAPI см. в документации по CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-189">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-190"><strong>-#</strong><strong></strong> <em>Серийный</em> номер</span><span class="sxs-lookup"><span data-stu-id="5b0ea-190"><strong>-#</strong> <strong></strong> <em>SerialNumber</em></span></span></td>
<td><span data-ttu-id="5b0ea-191">Серийный номер сертификата.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-191">Serial number of the certificate.</span></span> <span data-ttu-id="5b0ea-192">Максимальное значение равно 2 ^ 31.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-192">The maximum value is 2^31.</span></span> <span data-ttu-id="5b0ea-193">По умолчанию это значение, создаваемое средством, которое гарантированно уникально.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-193">The default is a value generated by the tool that is guaranteed to be unique.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-194"><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-194"><strong>-$</strong> <strong></strong> <em>CertificateAuthority</em></span></span></td>
<td><span data-ttu-id="5b0ea-195">Тип <a href="/windows/desktop/SecGloss/c-gly"><em>центра сертификации</em></a>.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-195">Type of <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span> <span data-ttu-id="5b0ea-196">Для <em>CertificateAuthority</em> должно быть задано значение <strong>коммерческая</strong> (для сертификатов, используемых коммерческими издателями) или <strong>индивидуально</strong> (для сертификатов, используемых отдельными издателями программного обеспечения).</span><span class="sxs-lookup"><span data-stu-id="5b0ea-196"><em>CertificateAuthority</em> must be set to either <strong>commercial</strong> (for certificates to be used by commercial software publishers) or <strong>individual</strong> (for certificates to be used by individual software publishers).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-197"><strong>-?</strong></span><span class="sxs-lookup"><span data-stu-id="5b0ea-197"><strong>-?</strong></span></span></td>
<td><span data-ttu-id="5b0ea-198">Отображает основные параметры.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-198">Displays the basic options.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-199"><strong>-!</strong></span><span class="sxs-lookup"><span data-stu-id="5b0ea-199"><strong>-!</strong></span></span></td>
<td><span data-ttu-id="5b0ea-200">Отображает расширенные параметры.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-200">Displays the extended options.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="5b0ea-201">Если в Internet Explorer версии 4,0 или более поздней используется параметр " **-Небесная** Спецификация ключа", спецификация должна соответствовать спецификации ключа, указанной в файле [*закрытого ключа*](../secgloss/p-gly.md) или в [*контейнере*](../secgloss/k-gly.md)закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-201">If the **-sky** key specification option is used in Internet Explorer version 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="5b0ea-202">Если параметр спецификации ключа не используется, будет использоваться ключевая спецификация, указанная в файле закрытого ключа или контейнере закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-202">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="5b0ea-203">Если в контейнере ключей содержится более одной ключевой спецификации, то MakeCert сначала попытается использовать \_ спецификацию ключа подписи.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-203">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="5b0ea-204">В случае сбоя MakeCert попытается использовать по адресу \_ кэйексчанже.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-204">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="5b0ea-205">Так как большинство пользователей имеют либо \_ ключ подписи \_ , либо ключ кэйексчанже, в большинстве случаев этот параметр не требуется использовать.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-205">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="5b0ea-206">Следующие параметры предназначены только для файлов [*сертификата издателя программного обеспечения*](../secgloss/s-gly.md) (SPC) и технологии закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-206">The following options are only for [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) files and private key technology.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b0ea-207">Параметр SPC и закрытый ключ</span><span class="sxs-lookup"><span data-stu-id="5b0ea-207">SPC and private key option</span></span></th>
<th><span data-ttu-id="5b0ea-208">Описание</span><span class="sxs-lookup"><span data-stu-id="5b0ea-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b0ea-209"><strong>-IC</strong> <strong></strong> <em>Иссуерцертфиле</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span></span></td>
<td><span data-ttu-id="5b0ea-210">Расположение сертификата издателя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-210">Location of the issuer's certificate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-211"><strong>-ОК</strong> <strong></strong> <em>Оба поля оставлены</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span></span></td>
<td><span data-ttu-id="5b0ea-212">Расположение контейнера ключей издателя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-212">Location of the issuer's key container.</span></span> <span data-ttu-id="5b0ea-213">Значение по умолчанию — корневой ключ теста.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-213">The default is the test root key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-214"><strong>-ИКИ</strong> <strong></strong> <em>Иссуеркэйспек</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span></span></td>
<td><span data-ttu-id="5b0ea-215">Спецификация ключа издателя, которая должна быть одним из трех возможных значений:</span><span class="sxs-lookup"><span data-stu-id="5b0ea-215">Issuer's key specification, which must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="5b0ea-216"><strong>Signature</strong> (спецификация ключа AT_SIGNATURE)</span><span class="sxs-lookup"><span data-stu-id="5b0ea-216"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="5b0ea-217"><strong>Exchange</strong> (спецификация ключа AT_KEYEXCHANGE)</span><span class="sxs-lookup"><span data-stu-id="5b0ea-217"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="5b0ea-218">Целое число, например <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="5b0ea-218">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="5b0ea-219">Дополнительные сведения см. в заметке, следующей за таблицей.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-219">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-220"><strong>— IP-адрес</strong> <strong></strong> <em>Иссуерпровидернаме</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span></span></td>
<td><span data-ttu-id="5b0ea-221">Поставщик CryptoAPI для издателя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-221">CryptoAPI provider for issuer.</span></span> <span data-ttu-id="5b0ea-222">По умолчанию используется поставщик пользователя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-222">The default is the user's provider.</span></span> <span data-ttu-id="5b0ea-223">Дополнительные сведения о поставщиках CryptoAPI см. в документации по CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-223">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b0ea-224"><strong>-IV</strong> <strong></strong> <em>Иссуеркэйфиле</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span></span></td>
<td><span data-ttu-id="5b0ea-225">Файл закрытого ключа издателя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-225">Issuer's private key file.</span></span> <span data-ttu-id="5b0ea-226">Значение по умолчанию — корень теста.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-226">The default is the test root.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b0ea-227"><strong>-ий</strong> <strong></strong> <em>ниссуерпровидертипе</em></span><span class="sxs-lookup"><span data-stu-id="5b0ea-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span></span></td>
<td><span data-ttu-id="5b0ea-228">Тип поставщика CryptoAPI для издателя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-228">CryptoAPI provider type for issuer.</span></span> <span data-ttu-id="5b0ea-229">Значение по умолчанию — <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-229">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="5b0ea-230">Дополнительные сведения о типах поставщиков CryptoAPI см. в документации по CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-230">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="5b0ea-231">Если параметр спецификации **-ИКИ** Key используется в Internet Explorer 4,0 или более поздней версии, спецификация должна соответствовать спецификации ключа, указанной в файле [*закрытого ключа*](../secgloss/p-gly.md) или в [*контейнере*](../secgloss/k-gly.md)закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-231">If the **-iky** key specification option is used in Internet Explorer 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="5b0ea-232">Если параметр спецификации ключа не используется, будет использоваться ключевая спецификация, указанная в файле закрытого ключа или контейнере закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-232">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="5b0ea-233">Если в контейнере ключей содержится более одной ключевой спецификации, то MakeCert сначала попытается использовать \_ спецификацию ключа подписи.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-233">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="5b0ea-234">В случае сбоя MakeCert попытается использовать по адресу \_ кэйексчанже.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-234">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="5b0ea-235">Так как большинство пользователей имеют либо \_ ключ подписи \_ , либо ключ кэйексчанже, в большинстве случаев этот параметр не требуется использовать.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-235">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="5b0ea-236">Следующие параметры предназначены только для технологии [*хранилища сертификатов*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0ea-236">The following options are for [*certificate store*](../secgloss/c-gly.md) technology only.</span></span>



| <span data-ttu-id="5b0ea-237">Параметр хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="5b0ea-237">Certificate store option</span></span>          | <span data-ttu-id="5b0ea-238">Описание</span><span class="sxs-lookup"><span data-stu-id="5b0ea-238">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b0ea-239">**-IC** *иссуерцертфиле*</span><span class="sxs-lookup"><span data-stu-id="5b0ea-239">**-ic** *IssuerCertFile*</span></span>          | <span data-ttu-id="5b0ea-240">Файл, содержащий сертификат издателя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-240">File that contains the issuer's certificate.</span></span> <span data-ttu-id="5b0ea-241">MakeCert выполнит поиск сертификата в хранилище сертификатов с точным совпадением.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-241">MakeCert will search in the certificate store for a certificate with an exact match.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="5b0ea-242">**— в** *иссуернаместринг*</span><span class="sxs-lookup"><span data-stu-id="5b0ea-242">**-in** *IssuerNameString*</span></span>        | <span data-ttu-id="5b0ea-243">Общее имя сертификата издателя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-243">Common name of the issuer's certificate.</span></span> <span data-ttu-id="5b0ea-244">MakeCert выполнит поиск сертификата в хранилище сертификатов, общее имя которого включает *иссуернаместринг*.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-244">MakeCert will search in the certificate store for a certificate whose common name includes *IssuerNameString*.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="5b0ea-245">**-IR** *иссуерцертсторелокатион*</span><span class="sxs-lookup"><span data-stu-id="5b0ea-245">**-ir** *IssuerCertStoreLocation*</span></span> | <span data-ttu-id="5b0ea-246">Расположение в реестре хранилища сертификатов издателя.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-246">Registry location of the issuer's certificate store.</span></span> <span data-ttu-id="5b0ea-247">*Иссуерцертсторелокатион* должен иметь значение **LocalMachine** (локальный компьютер раздела реестра hKey \_ \_ ) или **CurrentUser** (раздел реестра hKey \_ текущий \_ пользователь).</span><span class="sxs-lookup"><span data-stu-id="5b0ea-247">*IssuerCertStoreLocation* must be either **LocalMachine** (registry key HKEY\_LOCAL\_MACHINE) or **CurrentUser** (registry key HKEY\_CURRENT\_USER).</span></span> <span data-ttu-id="5b0ea-248">Параметр **CurrentUser** используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-248">**CurrentUser** is the default.</span></span>                                                                                                |
| <span data-ttu-id="5b0ea-249">**—** *иссуерцертсторенаме*</span><span class="sxs-lookup"><span data-stu-id="5b0ea-249">**-is** *IssuerCertStoreName*</span></span>     | <span data-ttu-id="5b0ea-250">Хранилище сертификатов издателя, включающее сертификат издателя и связанные с ним сведения о закрытом ключе.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-250">Issuer's certificate store that includes the issuer's certificate and its associated private key information.</span></span> <span data-ttu-id="5b0ea-251">Если в хранилище больше одного сертификата, пользователь должен однозначно идентифицировать его с помощью параметра **-IC** или **-in** .</span><span class="sxs-lookup"><span data-stu-id="5b0ea-251">If there is more than one certificate in the store, the user must uniquely identify it by using the **-ic** or **-in** option.</span></span> <span data-ttu-id="5b0ea-252">Если сертификат в хранилище сертификатов не определен уникальным образом, MakeCert завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-252">If the certificate in the certificate store is not uniquely identified, MakeCert will fail.</span></span> |



 

 

 
