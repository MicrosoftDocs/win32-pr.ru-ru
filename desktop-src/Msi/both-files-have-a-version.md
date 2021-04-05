---
description: Если оба файла имеют номер версии, установщик Windows использует логику, показанную на следующей схеме потока, чтобы определить, следует ли заменить все установленные файлы, принадлежащие компоненту.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Оба файла имеют версию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909047"
---
# <a name="both-files-have-a-version"></a><span data-ttu-id="ffff8-103">Оба файла имеют версию</span><span class="sxs-lookup"><span data-stu-id="ffff8-103">Both Files Have a Version</span></span>

<span data-ttu-id="ffff8-104">Если файл ключа устанавливаемого компонента (Copy-A) имеет то же имя, что и файл, уже установленный в целевом расположении (Copy-B), установщик сравнивает номер версии и язык двух файлов.</span><span class="sxs-lookup"><span data-stu-id="ffff8-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number and language of the two files.</span></span>

<span data-ttu-id="ffff8-105">Если оба файла имеют номер версии, установщик использует логику, показанную на следующей схеме потока, чтобы определить, следует ли заменить все установленные файлы, принадлежащие компоненту.</span><span class="sxs-lookup"><span data-stu-id="ffff8-105">If both files have a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="ffff8-106">Поскольку установщик устанавливает только компоненты целиком, при замене установленного файла ключей все файлы компонента заменяются.</span><span class="sxs-lookup"><span data-stu-id="ffff8-106">Because the installer only installs entire components, if the installed key file is replaced then all of the component's files are replaced.</span></span>

<span data-ttu-id="ffff8-107">Обратите внимание, что на этой диаграмме показаны [правила управления версиями файлов](file-versioning-rules.md)по умолчанию, которые можно переопределить, задав свойство [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="ffff8-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="ffff8-108">Значение свойства **REINSTALLMODE** по умолчанию — "omus".</span><span class="sxs-lookup"><span data-stu-id="ffff8-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![правила управления версиями файлов по умолчанию, если оба файла имеют одинаковое имя или номер версии](images/waiflow1.png)

<span data-ttu-id="ffff8-110">Предыдущую диаграмму также можно использовать с файлами без указания языка.</span><span class="sxs-lookup"><span data-stu-id="ffff8-110">The previous diagram can also be used with files with no language specified.</span></span> <span data-ttu-id="ffff8-111">Если для Copy-A указан язык, а для Copy-B не задан язык, то Copy-B заменяется на Copy-A.</span><span class="sxs-lookup"><span data-stu-id="ffff8-111">If copy-A has a specified language and copy-B has no specified language, copy-B is replaced with copy-A.</span></span> <span data-ttu-id="ffff8-112">Если для копий-A и Copy-B не задан язык, то Copy-B не заменяется.</span><span class="sxs-lookup"><span data-stu-id="ffff8-112">If copy-A and copy-B both have no language specified, then copy-B is not replaced.</span></span>

<span data-ttu-id="ffff8-113">См. Примеры управления версиями файлов по умолчанию при [замене существующих файлов](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="ffff8-113">See examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="ffff8-114">Ни один из файлов не имеет версии</span><span class="sxs-lookup"><span data-stu-id="ffff8-114">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="ffff8-115">Ни один из файлов не имеет версии с проверками хэша файла</span><span class="sxs-lookup"><span data-stu-id="ffff8-115">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="ffff8-116">Один файл имеет версию</span><span class="sxs-lookup"><span data-stu-id="ffff8-116">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



