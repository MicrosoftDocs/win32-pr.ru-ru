---
description: Средство настройки сертификатов служб Microsoft Windows HTTP (WinHTTP), &\# 0034; WinHttpCertCfg.exe&\# 0034;, позволяет администраторам устанавливать и настраивать сертификаты клиентов в любом хранилище сертификатов, доступ к которому может получить учетная запись диспетчера веб-приложений Internet Server Web (IWAM). Это средство также устраняет необходимость в специальных возможностях для учетных записей, таких как учетная запись IWAM, для получения доступа к сертификатам при использовании Active Server страниц (ASP).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, средство настройки сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4250cd717b9f611f4f23f17c93069760c283c97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145154"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a><span data-ttu-id="1e2cc-104">WinHttpCertCfg.exe, средство настройки сертификатов</span><span class="sxs-lookup"><span data-stu-id="1e2cc-104">WinHttpCertCfg.exe, a Certificate Configuration Tool</span></span>

<span data-ttu-id="1e2cc-105">Средство настройки сертификатов [служб Microsoft Windows HTTP (WinHTTP)](about-winhttp.md) , "WinHttpCertCfg.exe", позволяет администраторам устанавливать и настраивать сертификаты клиентов в любом [*хранилище сертификатов*](glossary.md) , доступ к которому может получить учетная запись диспетчера веб-приложений (IWAM) Internet Server.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-105">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) certificate configuration tool, "WinHttpCertCfg.exe", enables administrators to install and configure client certificates in any [*certificate store*](glossary.md) that can be accessed by the Internet Server Web Application Manager (IWAM) account.</span></span> <span data-ttu-id="1e2cc-106">Это средство также устраняет необходимость в специальных возможностях для учетных записей, таких как учетная запись IWAM, для получения доступа к сертификатам при использовании Active Server страниц (ASP).</span><span class="sxs-lookup"><span data-stu-id="1e2cc-106">The tool also eliminates the need to do anything special to accounts such as the IWAM account to gain access to certificates when using Active Server Pages (ASP).</span></span>

<span data-ttu-id="1e2cc-107">Консоль управления Microsoft (MMC) позволяет администраторам импортировать сертификаты клиентов на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-107">The Microsoft Management Console (MMC) enables administrators to import client certificates to a local computer.</span></span> <span data-ttu-id="1e2cc-108">Однако при импорте сертификата не предоставляется автоматически доступ к закрытому ключу для других учетных записей.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-108">However, importing a certificate does not automatically grant access to the private key for other accounts.</span></span> <span data-ttu-id="1e2cc-109">Этот закрытый ключ необходим для проверки подлинности сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-109">This private key is required for client certificate authentication.</span></span> <span data-ttu-id="1e2cc-110">При необходимости средство настройки сертификатов служб Microsoft Windows HTTP (WinHTTP) предоставляет возможность предоставления доступа к дополнительным учетным записям, таким как учетная запись IWAM.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-110">The Microsoft Windows HTTP Services (WinHTTP) certificate configuration tool provides the ability to grant access to additional accounts, such as the IWAM account, when required.</span></span>

-   [<span data-ttu-id="1e2cc-111">Использование средства настройки сертификатов</span><span class="sxs-lookup"><span data-stu-id="1e2cc-111">Using the Certificate Configuration Tool</span></span>](#using-the-certificate-configuration-tool)
-   [<span data-ttu-id="1e2cc-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="1e2cc-112">Examples</span></span>](#examples)

## <a name="using-the-certificate-configuration-tool"></a><span data-ttu-id="1e2cc-113">Использование средства настройки сертификатов</span><span class="sxs-lookup"><span data-stu-id="1e2cc-113">Using the Certificate Configuration Tool</span></span>

<span data-ttu-id="1e2cc-114">Средство настройки сертификатов WinHTTP, WinHttpCertCfg.exe, доступно для загрузки на веб-сайте [средств комплекта ресурсов Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) .</span><span class="sxs-lookup"><span data-stu-id="1e2cc-114">The WinHTTP certificate configuration tool, WinHttpCertCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="1e2cc-115">В следующем примере кода показаны допустимые параметры командной строки для использования с этим инструментом.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-115">The following example code shows the valid command line parameters to use with this tool.</span></span>

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

<span data-ttu-id="1e2cc-116">В следующей таблице перечислены параметры для средства настройки.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-116">The following table lists parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e2cc-117">Параметр</span><span class="sxs-lookup"><span data-stu-id="1e2cc-117">Parameter</span></span></th>
<th><span data-ttu-id="1e2cc-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1e2cc-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e2cc-119">-?</span><span class="sxs-lookup"><span data-stu-id="1e2cc-119">-?</span></span></td>
<td><span data-ttu-id="1e2cc-120">Отображает данные синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-120">Displays syntax data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e2cc-121">-i</span><span class="sxs-lookup"><span data-stu-id="1e2cc-121">-i</span></span></td>
<td><span data-ttu-id="1e2cc-122">Указывает, что сертификат должен быть импортирован из файла обмена личной информацией (PFX).</span><span class="sxs-lookup"><span data-stu-id="1e2cc-122">Specifies that the certificate is to be imported from a Personal Information Exchange (PFX) file.</span></span> <span data-ttu-id="1e2cc-123">После этого параметра должно следовать имя файла.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-123">This parameter must be followed by the name of the file.</span></span> <span data-ttu-id="1e2cc-124">Если этот параметр задан, &quot; &quot; &quot; &quot; также необходимо указать параметр-a и-c.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-124">When this parameter is specified, &quot;-a&quot; and &quot;-c&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e2cc-125">-g</span><span class="sxs-lookup"><span data-stu-id="1e2cc-125">-g</span></span></td>
<td><span data-ttu-id="1e2cc-126">Указывает, что доступ предоставляется закрытому ключу.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-126">Specifies that access is granted to a private key.</span></span> <span data-ttu-id="1e2cc-127">Если указан этот параметр, &quot; &quot; необходимо также указать параметры-a, &quot; -c &quot; и &quot; -s &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e2cc-127">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e2cc-128">-r</span><span class="sxs-lookup"><span data-stu-id="1e2cc-128">-r</span></span></td>
<td><span data-ttu-id="1e2cc-129">Указывает, что доступ к закрытому ключу удаляется.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-129">Specifies that access is removed for a private key.</span></span> <span data-ttu-id="1e2cc-130">Если указан этот параметр, &quot; &quot; необходимо также указать параметры-a, &quot; -c &quot; и &quot; -s &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e2cc-130">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e2cc-131">-l</span><span class="sxs-lookup"><span data-stu-id="1e2cc-131">-l</span></span></td>
<td><span data-ttu-id="1e2cc-132">Указывает, что указаны учетные записи с доступом к закрытому ключу.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-132">Specifies that accounts with access to a private key are listed.</span></span> <span data-ttu-id="1e2cc-133">Если указан этот параметр, &quot; &quot; &quot; &quot; необходимо также указать параметр-c и-s.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-133">When this parameter is specified, &quot;-c&quot; and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e2cc-134">-a</span><span class="sxs-lookup"><span data-stu-id="1e2cc-134">-a</span></span></td>
<td><span data-ttu-id="1e2cc-135">Указывает учетную запись пользователя на настраиваемой машине.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-135">Specifies the user account on the machine being configured.</span></span> <span data-ttu-id="1e2cc-136">Это может быть локальный компьютер или учетная запись домена, например &quot; IWAM_TESTMACHINE &quot; , &quot; TESTUSER &quot; или &quot; тестдомаин\домаинусер &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e2cc-136">This could be a local machine or domain account, such as &quot;IWAM_TESTMACHINE&quot;, &quot;TESTUSER&quot;, or &quot;TESTDOMAIN\DOMAINUSER&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e2cc-137">-c</span><span class="sxs-lookup"><span data-stu-id="1e2cc-137">-c</span></span></td>
<td><span data-ttu-id="1e2cc-138">Указывает расположение и имя <a href="glossary.md"><em>хранилища сертификатов</em></a>.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-138">Specifies the location and name of the <a href="glossary.md"><em>certificate store</em></a>.</span></span> <span data-ttu-id="1e2cc-139">Используйте &quot; LOCAL_MACHINE &quot; или &quot; CURRENT_USER &quot; , чтобы указать, какую ветвь реестра следует использовать для расположения.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-139">Use &quot;LOCAL_MACHINE&quot; or &quot;CURRENT_USER&quot; to designate which registry branch to use for the location.</span></span> <span data-ttu-id="1e2cc-140"><em>Хранилище сертификатов</em> может быть установлено на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-140">The <em>certificate store</em> can be any installed on the machine.</span></span> <span data-ttu-id="1e2cc-141">Типичными примерами имен являются &quot; My &quot; , &quot; root &quot; и &quot; TrustedPeople &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e2cc-141">Typical name examples are &quot;MY&quot;, &quot;Root&quot;, and &quot;TrustedPeople&quot;.</span></span> <span data-ttu-id="1e2cc-142">Расположение и имя <em>хранилища сертификатов</em> разделяются обратной косой чертой, например &quot; LOCAL_MACHINE \рут &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e2cc-142">The location and name of the <em>certificate store</em> are separated with a backward slash, for example, &quot;LOCAL_MACHINE\Root&quot;.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e2cc-143">Несмотря на &quot; то &quot; , что с этим параметром можно указать CURRENT_USERную ветвь реестра, расширение доступа к закрытым ключам в основном предназначено для сертификатов, установленных в <a href="glossary.md"><em>хранилище сертификатов</em></a> на локальном компьютере, к которому могут обращаться несколько пользователей.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-143">Although the &quot;CURRENT_USER&quot; branch of the registry can be specified with this parameter, extending access to private keys is primarily intended for certificates installed in a local computer <a href="glossary.md"><em>certificate store</em></a> that can be accessed by multiple users.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e2cc-144">-S</span><span class="sxs-lookup"><span data-stu-id="1e2cc-144">-s</span></span></td>
<td><span data-ttu-id="1e2cc-145">Указывает строку поиска, не учитывающую регистр, для поиска первого перечисленного сертификата с именем субъекта, содержащим эту подстроку.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-145">Specifies a case-insensitive search string for finding the first enumerated certificate with a subject name that contains this substring.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e2cc-146">-p</span><span class="sxs-lookup"><span data-stu-id="1e2cc-146">-p</span></span></td>
<td><span data-ttu-id="1e2cc-147">Указывает пароль, используемый для импорта сертификата и закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-147">Specifies a password that is used to import the certificate and the private key.</span></span> <span data-ttu-id="1e2cc-148">Используется только с параметром импорта.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-148">This is only used with the import option.</span></span></td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> <span data-ttu-id="1e2cc-149">Пользователь должен иметь достаточные привилегии для использования этого средства, что требует, чтобы пользователь был администратором и тем же пользователем, который установил сертификат клиента, если он установлен.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-149">The user must have sufficient privileges to use this tool, which requires the user to be an administrator and the same user who installed the client certificate, if installed.</span></span>
>
> <span data-ttu-id="1e2cc-150">Средство "WinHttpCertCfg.exe" нецелесообразно для настройки сертификатов, хранящихся в файловой системе, например FAT32, которая не поддерживает списки управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="1e2cc-150">The "WinHttpCertCfg.exe" tool is not useful to configure certificates stored in a file system such as FAT32, which does not support access control lists (ACL).</span></span>

## <a name="examples"></a><span data-ttu-id="1e2cc-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="1e2cc-151">Examples</span></span>

<span data-ttu-id="1e2cc-152">В следующих примерах показаны некоторые способы использования средства настройки.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-152">The following examples show some of the ways in which the configuration tool can be used.</span></span>

1.  <span data-ttu-id="1e2cc-153">Эта команда перечисляет учетные записи, которые имеют доступ к закрытому ключу для сертификата "Мойсертификат" в корневом [*хранилище сертификатов*](glossary.md) \_ ветви локального компьютера в реестре.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-153">This command lists accounts that have access to the private key for the "MyCertificate" certificate in the "Root" [*certificate store*](glossary.md) of the LOCAL\_MACHINE branch of the registry.</span></span>

    <span data-ttu-id="1e2cc-154">**Winhttpcertcfg-l-c \_ корневая машина \\ root-s мойсертификат**</span><span class="sxs-lookup"><span data-stu-id="1e2cc-154">**winhttpcertcfg -l -c LOCAL\_MACHINE\\Root -s MyCertificate**</span></span>

2.  <span data-ttu-id="1e2cc-155">Эта команда предоставляет доступ к закрытому ключу сертификата "Мойсертификат" в [*хранилище сертификатов*](glossary.md) "My" для учетной записи TESTUSER.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-155">This command grants access to the private key of the "MyCertificate" certificate in the "My" [*certificate store*](glossary.md) for the TESTUSER account.</span></span>

    <span data-ttu-id="1e2cc-156">**Winhttpcertcfg-g-c локальный \_ компьютер \\ Мой-s мойсертификат-a TESTUSER**</span><span class="sxs-lookup"><span data-stu-id="1e2cc-156">**winhttpcertcfg -g -c LOCAL\_MACHINE\\My -s MyCertificate -a TESTUSER**</span></span>

3.  <span data-ttu-id="1e2cc-157">Эта команда импортирует сертификат и закрытый ключ из PFX-файла и расширяет доступ к закрытому ключу для другой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-157">This command imports a certificate and private key from a PFX file and extends private key access to another account.</span></span>

    <span data-ttu-id="1e2cc-158">**Winhttpcertcfg-i Пфксфиле-c локальный \_ компьютер \\ Мой-a IWAM \_ Тестмачине-p пфкспассворд**</span><span class="sxs-lookup"><span data-stu-id="1e2cc-158">**winhttpcertcfg -i PFXFile -c LOCAL\_MACHINE\\My -a IWAM\_TESTMACHINE -p PFXPassword**</span></span>

4.  <span data-ttu-id="1e2cc-159">Эта команда запрещает доступ к закрытому ключу \_ учетной записи IWAM тестмачине с указанным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="1e2cc-159">This command denies access to the private key for the IWAM\_TESTMACHINE account with the specified certificate.</span></span>

    <span data-ttu-id="1e2cc-160">**Winhttpcertcfg-r-c локальный \_ компьютер \\ root-s мойсертификат — a IWAM \_ тестмачине**</span><span class="sxs-lookup"><span data-stu-id="1e2cc-160">**winhttpcertcfg -r -c LOCAL\_MACHINE\\Root -s MyCertificate -a IWAM\_TESTMACHINE**</span></span>

 

 




