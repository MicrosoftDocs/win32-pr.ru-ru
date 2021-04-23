---
description: Средство CryptoAPI, которое создает файл каталога.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: макекат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897610"
---
# <a name="makecat"></a><span data-ttu-id="6ffc3-103">макекат</span><span class="sxs-lookup"><span data-stu-id="6ffc3-103">MakeCat</span></span>

<span data-ttu-id="6ffc3-104">Средство Макекат — это средство CryptoAPI, которое создает файл каталога.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-104">The MakeCat tool is a CryptoAPI tool that creates a catalog file.</span></span> <span data-ttu-id="6ffc3-105">Макекат доступен в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK) для Windows 7 и платформа .NET Framework 4,0 и устанавливается по умолчанию в \\ папке bin пути установки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-105">MakeCat is available as part of the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 and is installed, by default, in the \\Bin folder of the SDK installation path.</span></span>

<span data-ttu-id="6ffc3-106">Средство Макекат использует следующий синтаксис команды:</span><span class="sxs-lookup"><span data-stu-id="6ffc3-106">The MakeCat tool uses the following command syntax:</span></span>

<span data-ttu-id="6ffc3-107">**Макекат** \[ **-n** \| **-r** \| **-v** \] *Имя файла*</span><span class="sxs-lookup"><span data-stu-id="6ffc3-107">**MakeCat** \[**-n**\|**-r**\|**-v**\] *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="6ffc3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ffc3-108">Parameters</span></span>



| <span data-ttu-id="6ffc3-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="6ffc3-109">Parameter</span></span>             | <span data-ttu-id="6ffc3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6ffc3-110">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffc3-111">**-n**</span><span class="sxs-lookup"><span data-stu-id="6ffc3-111">**-n**</span></span><br/>     | <span data-ttu-id="6ffc3-112">Не останавливайте восстановление при устранимой ошибке.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-112">Do not stop on a recoverable error.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="6ffc3-113">**-r**</span><span class="sxs-lookup"><span data-stu-id="6ffc3-113">**-r**</span></span><br/>     | <span data-ttu-id="6ffc3-114">Принудительное завершение Макекат при обнаружении устранимых ошибок.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-114">Forces MakeCat to end if it encounters recoverable errors.</span></span> <span data-ttu-id="6ffc3-115">В частности, она будет завершаться при обработке записей в разделе файлы каталога CDF-файла.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-115">Specifically, it will end when processing the entries in the catalog files section of a .cdf file.</span></span><br/> |
| <span data-ttu-id="6ffc3-116">**-v**</span><span class="sxs-lookup"><span data-stu-id="6ffc3-116">**-v**</span></span><br/>     | <span data-ttu-id="6ffc3-117">Verbose.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-117">Verbose.</span></span> <span data-ttu-id="6ffc3-118">Отображает все ход выполнения и сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-118">Displays all progress and error messages.</span></span><br/>                                                                                                            |
| <span data-ttu-id="6ffc3-119">*FileName*</span><span class="sxs-lookup"><span data-stu-id="6ffc3-119">*FileName*</span></span><br/> | <span data-ttu-id="6ffc3-120">Имя файла. CDF, который необходимо проанализировать.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-120">Name of the .cdf file to be parsed.</span></span> <span data-ttu-id="6ffc3-121">Сведения о требуемой структуре и содержимом см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-121">For required structure and contents, see Remarks.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="6ffc3-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ffc3-122">Remarks</span></span>

<span data-ttu-id="6ffc3-123">CDF – файл должен быть построен со следующими спецификациями.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-123">The .cdf file must be built with the following specifications.</span></span>

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> <span data-ttu-id="6ffc3-124">Последняя запись в файле. CDF должна всегда содержать явный символ новой строки в конце строки.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-124">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

<span data-ttu-id="6ffc3-125">\[Раздел каталогхеадер \] определяет сведения о файле всего каталога.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-125">The \[CatalogHeader\] section defines information about the entire catalog file.</span></span>



| <span data-ttu-id="6ffc3-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="6ffc3-126">Option</span></span>                    | <span data-ttu-id="6ffc3-127">Описание</span><span class="sxs-lookup"><span data-stu-id="6ffc3-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffc3-128">Имя</span><span class="sxs-lookup"><span data-stu-id="6ffc3-128">Name</span></span><br/>           | <span data-ttu-id="6ffc3-129">Имя файла каталога, включая его расширение.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-129">Name of the catalog file, including its extension.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6ffc3-130">ресултдир</span><span class="sxs-lookup"><span data-stu-id="6ffc3-130">ResultDir</span></span><br/>      | <span data-ttu-id="6ffc3-131">Каталог, в который будет помещен созданный файл. cat.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-131">Directory where the created .cat file will be placed.</span></span> <span data-ttu-id="6ffc3-132">Если этот параметр не указан, используется текущий каталог по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-132">If not indicated, the default current directory is used.</span></span> <span data-ttu-id="6ffc3-133">Если каталог не существует, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-133">If the directory does not exist, it is created.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6ffc3-134">публикверсион</span><span class="sxs-lookup"><span data-stu-id="6ffc3-134">PublicVersion</span></span><br/>  | <span data-ttu-id="6ffc3-135">Этот параметр не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-135">This option is not supported.</span></span> <br/> <span data-ttu-id="6ffc3-136">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP:** Версия каталога.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-136">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** Catalog version.</span></span> <span data-ttu-id="6ffc3-137">Если оставить это поле пустым, используется значение по умолчанию, равное 1.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-137">If left blank, the default value, 1, is used.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6ffc3-138">каталогверсион</span><span class="sxs-lookup"><span data-stu-id="6ffc3-138">CatalogVersion</span></span><br/> | <span data-ttu-id="6ffc3-139">Версия каталога.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-139">Catalog version.</span></span> <span data-ttu-id="6ffc3-140">Если версия отсутствует или имеет значение 1, то значение "0x100" передается параметру *двпубликверсион* функции [**крипткатопен**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) , а также создается файл каталога версии 1.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-140">If the version is not present or is set to 1, then "0x100" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 1 catalog file is created.</span></span> <span data-ttu-id="6ffc3-141">Параметр Хашалгорисмс должен быть пустым или содержать SHA1.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-141">The HashAlgorithms option must be empty or contain SHA1.</span></span><br/> <span data-ttu-id="6ffc3-142">Если для версии задано значение 2, то в параметре *двпубликверсион* функции [**крипткатопен**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) передается "0x200", а также создается файл каталога версии 2.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-142">If the version is set to 2, then "0x200" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 2 catalog file is created.</span></span> <span data-ttu-id="6ffc3-143">Параметр Хашалгорисмс должен содержать SHA256.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-143">The HashAlgorithms option must contain SHA256.</span></span><br/> <span data-ttu-id="6ffc3-144">Если этот параметр имеется, но содержит любое значение, отличное от 1 или 2, то средство Макекат выдаст ошибку.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-144">If this option is present but contains any value other than 1 or 2, the MakeCat tool will error out.</span></span><br/> <span data-ttu-id="6ffc3-145">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот параметр не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-145">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/> |
| <span data-ttu-id="6ffc3-146">хашалгорисмс</span><span class="sxs-lookup"><span data-stu-id="6ffc3-146">HashAlgorithms</span></span><br/> | <span data-ttu-id="6ffc3-147">Имя используемого алгоритма хэширования.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-147">Name of the hashing algorithm used.</span></span> <span data-ttu-id="6ffc3-148">Дополнительные сведения см. в описании параметра Каталогверсион.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-148">For more information, see the CatalogVersion option.</span></span><br/> <span data-ttu-id="6ffc3-149">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот параметр не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-149">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6ffc3-150">пажехашес</span><span class="sxs-lookup"><span data-stu-id="6ffc3-150">PageHashes</span></span><br/>     | <span data-ttu-id="6ffc3-151">Указывает, следует ли хэшировать файлы, перечисленные в <HASH> параметре, \[ в \] разделе каталогфилес</span><span class="sxs-lookup"><span data-stu-id="6ffc3-151">Specifies whether to hash the files listed in the <HASH> option in the \[CatalogFiles\] section</span></span><br/> <span data-ttu-id="6ffc3-152">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот параметр не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-152">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6ffc3-153">енкодингтипе</span><span class="sxs-lookup"><span data-stu-id="6ffc3-153">EncodingType</span></span><br/>   | <span data-ttu-id="6ffc3-154">Тип используемой кодировки сообщений.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-154">Type of message encoding used.</span></span> <span data-ttu-id="6ffc3-155">Если оставить это поле пустым, Енкодингтипе по умолчанию будет иметь номер PKCS \_ 7 ASN кодировка \_ \_ \| X509 \_ ASN \_ , 0x00010001.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-155">If left blank, the default EncodingType is PKCS\_7\_ASN\_ENCODING \| X509\_ASN\_ENCODING, 0x00010001.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="6ffc3-156">\[Раздел каталогфилес \] определяет каждый член файла каталога с файлами различных типов и атрибутов различных типов в отдельных группах.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-156">The \[CatalogFiles\] section defines each member of the catalog file with files of various types and attributes of various types in separate groups.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ffc3-157">Параметр</span><span class="sxs-lookup"><span data-stu-id="6ffc3-157">Option</span></span></th>
<th><span data-ttu-id="6ffc3-158">Описание</span><span class="sxs-lookup"><span data-stu-id="6ffc3-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ffc3-159">тег ссылки</span><span class="sxs-lookup"><span data-stu-id="6ffc3-159">reference tag</span></span><br/></td>
<td><span data-ttu-id="6ffc3-160">Текстовая ссылка на файл.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-160">Text reference to the file.</span></span> <span data-ttu-id="6ffc3-161">Это могут быть любые текстовые символы ASCII, кроме знака равенства (=).</span><span class="sxs-lookup"><span data-stu-id="6ffc3-161">This can include any ASCII text characters except the equal sign (=).</span></span> <span data-ttu-id="6ffc3-162">Система должна иметь возможность воспроизводить этот тег после установки.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-162">The system must be able to reproduce this tag after installation.</span></span> <br/> <span data-ttu-id="6ffc3-163">Используйте <HASH> в качестве префикса имени файла.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-163">Use <HASH> as a prefix of the file name.</span></span> <span data-ttu-id="6ffc3-164">В результате тег будет являться хэшем файла в форме строки ASCII.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-164">This results in the tag being the file's hash in ASCII string form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ffc3-165">путь и имя файла</span><span class="sxs-lookup"><span data-stu-id="6ffc3-165">file path and name</span></span><br/></td>
<td><span data-ttu-id="6ffc3-166">Имя файла, включая расширение для синтаксического анализа и относительный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-166">The file name, including the extension to be parsed and the relative path to the file.</span></span> <span data-ttu-id="6ffc3-167">В каталог можно добавить любой тип файла, который можно подписать с помощью средства SignTool.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-167">Any type of file that can be signed with SignTool can be added to a catalog.</span></span> <span data-ttu-id="6ffc3-168">Например, имена файлов со следующими расширениями, помимо прочих, можно добавить в каталог:. exe,. cab,. cat,. ocx,. dll и. STL.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-168">For example, file names with the following extensions, among others, can be added to a catalog: .exe, .cab, .cat, .ocx, .dll, and .stl.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ffc3-169">алтсипид</span><span class="sxs-lookup"><span data-stu-id="6ffc3-169">ALTSIPID</span></span><br/></td>
<td><span data-ttu-id="6ffc3-170">Идентификатор GUID SIP, который будет использоваться для хэширования вместо стандартного SIP, основанного на типе файлов.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-170">SIP GUID that is to be used for hashing instead of the standard SIP based on file type.</span></span> <span data-ttu-id="6ffc3-171">Эта запись не является обязательной.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-171">This entry is optional.</span></span> <span data-ttu-id="6ffc3-172">Если эта запись отсутствует, элемент будет хэширован с использованием SIP по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-172">If this entry is omitted, the member will be hashed using the default SIP.</span></span> <span data-ttu-id="6ffc3-173">Если установленный по умолчанию SIP не найден, будет использоваться плоский модуль SIP.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-173">If no default installed SIP is found, the Flat SIP will be used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ffc3-174">guid</span><span class="sxs-lookup"><span data-stu-id="6ffc3-174">guid</span></span><br/></td>
<td><span data-ttu-id="6ffc3-175">Текстовое представление идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-175">Text representation of a GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ffc3-176">аттркс</span><span class="sxs-lookup"><span data-stu-id="6ffc3-176">ATTRx</span></span><br/></td>
<td><span data-ttu-id="6ffc3-177">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-177">Optional.</span></span> <span data-ttu-id="6ffc3-178">Атрибут или оператор о файле или содержимом.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-178">Attribute or statement about the file or content.</span></span> <span data-ttu-id="6ffc3-179">Может существовать любое количество атрибутов, включая None.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-179">There can be any number of attributes, including none.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ffc3-180">тип</span><span class="sxs-lookup"><span data-stu-id="6ffc3-180">type</span></span><br/></td>
<td><span data-ttu-id="6ffc3-181">Определяет, какой тип атрибута добавляется в формате 0x00000000 (текст).</span><span class="sxs-lookup"><span data-stu-id="6ffc3-181">Defines what type of attribute is being added in the format 0x00000000 (text).</span></span> <span data-ttu-id="6ffc3-182">Этот параметр может быть сочетанием битового<strong>или</strong> нуля или более следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6ffc3-182">This option can be a bitwise-<strong>OR</strong> combination of zero or more of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="6ffc3-183">0x10000000 прошедший проверку атрибут (подписанный, включается в хэш).</span><span class="sxs-lookup"><span data-stu-id="6ffc3-183">0x10000000 Authenticated attribute (signed, included in the hash).</span></span></li>
<li><span data-ttu-id="6ffc3-184">0x20000000 непроверенный атрибут (без подписи, не включается в хэш, не поддающийся проверке).</span><span class="sxs-lookup"><span data-stu-id="6ffc3-184">0x20000000 Unauthenticated attribute (unsigned, not included in the hash, not verifiable).</span></span></li>
<li><span data-ttu-id="6ffc3-185">Атрибут 0x01000000 не будет реплицирован в записи SHA1 в каталоге Каталогверсион 2.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-185">0x01000000 Attribute will not be replicated to SHA1 entries in a CatalogVersion 2 catalog.</span></span></li>
<li><span data-ttu-id="6ffc3-186">Атрибут 0x00010000 представлен в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-186">0x00010000 Attribute is represented in plaintext.</span></span> <span data-ttu-id="6ffc3-187">Преобразование не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-187">No conversion will be done.</span></span></li>
<li><span data-ttu-id="6ffc3-188">Атрибут 0x00020000 представлен в кодировке Base-64.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-188">0x00020000 Attribute is represented in base-64 encoding.</span></span> <span data-ttu-id="6ffc3-189">Используется для представления двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-189">This is used to represent binary data.</span></span></li>
<li><span data-ttu-id="6ffc3-190">0x00000001 — это пара "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="6ffc3-190">0x00000001 Attribute is a name-value pair.</span></span> <span data-ttu-id="6ffc3-191">Используйте параметр OID для имени.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-191">Use the oid option for the name.</span></span> <span data-ttu-id="6ffc3-192">Этот атрибут работает слишком долго; Поэтому используйте этот параметр с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-192">This attribute is slow; therefore, use this option sparingly.</span></span></li>
<li><span data-ttu-id="6ffc3-193">на атрибут 0x00000002 ссылается <a href="/windows/desktop/SecGloss/o-gly"><em>идентификатор объекта</em></a> (OID).</span><span class="sxs-lookup"><span data-stu-id="6ffc3-193">0x00000002 Attribute is referenced by an <a href="/windows/desktop/SecGloss/o-gly"><em>object identifier</em></a> (OID).</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ffc3-194">oid</span><span class="sxs-lookup"><span data-stu-id="6ffc3-194">oid</span></span><br/></td>
<td><span data-ttu-id="6ffc3-195">Текстовое представление ключа ссылки атрибута.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-195">The text representation of the attribute's reference key.</span></span> <span data-ttu-id="6ffc3-196">Это OID в виде текстовой строки в точечно-десятичной нотации (например, a. b. c. d) или в текстовом имени.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-196">It is an OID in the form of a text string in dotted quad notation (for example, a.b.c.d) or a text Name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ffc3-197">значение</span><span class="sxs-lookup"><span data-stu-id="6ffc3-197">value</span></span><br/></td>
<td><span data-ttu-id="6ffc3-198">Текстовое представление значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-198">The text representation of the value of the attribute.</span></span> <span data-ttu-id="6ffc3-199">Тип используемого текстового представления зависит от значения параметра Type.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-199">The type of text representation used depends on the value of the type option.</span></span> <span data-ttu-id="6ffc3-200">КОНЦА строки символы определяют длину.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-200">The EOL characters determine the length.</span></span><br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td><span data-ttu-id="6ffc3-201">Хэширует указанный файл.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-201">Hashes the specified file.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6ffc3-202">Созданный файл каталога не подписан.</span><span class="sxs-lookup"><span data-stu-id="6ffc3-202">The generated catalog file is unsigned.</span></span> <span data-ttu-id="6ffc3-203">Если он должен быть подписан до передачи, он подписывается с помощью средства [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="6ffc3-203">If it is to be signed prior to transmittal, it is signed by using [SignTool](signtool.md).</span></span>

 

 
