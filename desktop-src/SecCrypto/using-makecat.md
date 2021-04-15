---
description: Создает неподписанный файл каталога, который содержит хэши набора файлов вместе со связанными атрибутами каждого файла в наборе. Файл каталога позволяет пользователю подписывать один файл (каталог) вместо подписывания множества отдельных файлов.
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: Использование Макекат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36c83531df38b95bde03edd719d98be325dbeac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682981"
---
# <a name="using-makecat"></a><span data-ttu-id="0386b-104">Использование Макекат</span><span class="sxs-lookup"><span data-stu-id="0386b-104">Using MakeCat</span></span>

<span data-ttu-id="0386b-105">Средство [макекат](makecat.md) создает неподписанный файл каталога, который содержит [*хэши*](../secgloss/h-gly.md) набора файлов вместе со связанными атрибутами каждого файла в наборе.</span><span class="sxs-lookup"><span data-stu-id="0386b-105">The [MakeCat](makecat.md) tool makes an unsigned catalog file, which contains the [*hashes*](../secgloss/h-gly.md) of a set of files along with associated attributes of each file in the set.</span></span> <span data-ttu-id="0386b-106">Файл каталога позволяет пользователю подписывать один файл (каталог) вместо подписывания множества отдельных файлов.</span><span class="sxs-lookup"><span data-stu-id="0386b-106">A catalog file allows the user to sign one file (the catalog) instead of signing numerous individual files.</span></span>

<span data-ttu-id="0386b-107">После подписания и передачи неподписанного файла каталога получатель может сравнить хэши исходных файлов с хэш-кодами, содержащимися в файле каталога, и убедиться, что эти файлы свободны от несанкционированного изменения.</span><span class="sxs-lookup"><span data-stu-id="0386b-107">After the unsigned catalog file is signed and transmitted, the receiver can compare the hashes of the original files to the hashes contained within the catalog file and verify that the files are free of tampering.</span></span>

<span data-ttu-id="0386b-108">Перед использованием средства [макекат](makecat.md) пользователь должен подготовить файл определения каталога (. CDF) с помощью любого текстового редактора.</span><span class="sxs-lookup"><span data-stu-id="0386b-108">Prior to using the [MakeCat](makecat.md) tool, the user must prepare a Catalog Definition File (.cdf), by using any text editor.</span></span> <span data-ttu-id="0386b-109">CDF-файл содержит список файлов и атрибуты файлов для каталогизации (спецификации перечислены ниже).</span><span class="sxs-lookup"><span data-stu-id="0386b-109">The .cdf file contains the list of files and the attributes of the files to be cataloged (the specifications are listed below).</span></span> <span data-ttu-id="0386b-110">Средство Макекат сканирует CDF-файл, проверяет список атрибутов каждого файла, добавляет указанные атрибуты в сам каталог, хэширует каждый из перечисленных файлов и сохраняет хэши каждого файла в файле каталога.</span><span class="sxs-lookup"><span data-stu-id="0386b-110">The MakeCat tool scans the .cdf file, verifies the list of attributes of each listed file, adds the listed attributes to the catalog itself, hashes each of the listed files, and stores the hashes of each file into the catalog file.</span></span> <span data-ttu-id="0386b-111">Каждый файл имеет свой хэш и атрибуты, хранящиеся отдельно в каталоге.</span><span class="sxs-lookup"><span data-stu-id="0386b-111">Each file has its hash and attributes stored separately within the catalog.</span></span> <span data-ttu-id="0386b-112">Этот файл каталога можно затем подписать и передать.</span><span class="sxs-lookup"><span data-stu-id="0386b-112">This catalog file can then be signed and transmitted.</span></span> <span data-ttu-id="0386b-113">Затем получатель может сравнить хэш каждого файла в каталоге с хэшом исходных файлов, чтобы доказать, что исходное содержимое не поддается иззаконному изменению.</span><span class="sxs-lookup"><span data-stu-id="0386b-113">The receiver can subsequently compare the hash of each file within the catalog with the hash of the original files to prove that the original content is free of tampering.</span></span> <span data-ttu-id="0386b-114">Макекат не изменяет файл. CDF.</span><span class="sxs-lookup"><span data-stu-id="0386b-114">MakeCat does not modify the .cdf file.</span></span>

<span data-ttu-id="0386b-115">В следующих примерах используются команды [макекат](makecat.md) .</span><span class="sxs-lookup"><span data-stu-id="0386b-115">The following examples use [MakeCat](makecat.md) commands.</span></span>

-   <span data-ttu-id="0386b-116">Создайте файл каталога из файла Good. CDF.</span><span class="sxs-lookup"><span data-stu-id="0386b-116">Generate a catalog file from the file Good.cdf.</span></span>

    <span data-ttu-id="0386b-117">**Макекат-v Good. CDF**</span><span class="sxs-lookup"><span data-stu-id="0386b-117">**MakeCat -v good.cdf**</span></span>

<span data-ttu-id="0386b-118">Файл Good. CDF создает файл каталога Good.cat, анализируя файлы UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, без знака. class и SignedPE.exe.</span><span class="sxs-lookup"><span data-stu-id="0386b-118">A file, Good.cdf, produces a catalog file, Good.cat, by parsing the files UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, Unsigned.Class, and SignedPE.exe.</span></span> <span data-ttu-id="0386b-119">Проанализированные файлы, а также хорошее. CDF и вновь созданные Good.cat, находятся в одном каталоге.</span><span class="sxs-lookup"><span data-stu-id="0386b-119">The parsed files, along with Good.cdf and the newly generated Good.cat, are all in the same directory.</span></span>

``` syntax
[CatalogHeader]
Name=Good.cat
ResultDir=.\
PublicVersion=0x00000001
EncodingType=
CATATTR1=0x10010001:Movie1:FirstMovie
CATATTR2=0x10010001:Movie2:SecondMovie
CATATTR3=0x10010001:Movie3:ThirdMovie

[CatalogFiles]
UnsignedPE=.\UnsignedPE.EXE
UnsignedDOS=.\UnsignedDOS.EXE
<HASH>UnsignedCAB=.\Unsigned.CAB
UnsignedClass=.\Unsigned.Class
SignedPE=.\SignedPE.EXE
```

> [!Note]  
> <span data-ttu-id="0386b-120">Последняя запись в файле. CDF должна всегда содержать явный символ новой строки в конце строки.</span><span class="sxs-lookup"><span data-stu-id="0386b-120">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

 

 
