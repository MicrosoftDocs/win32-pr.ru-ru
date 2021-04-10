---
description: Если только один из файлов имеет номер версии, установщик Windows использует логику, показанную на следующей схеме потока, чтобы определить, следует ли заменить все установленные файлы, принадлежащие компоненту.
ms.assetid: 1eda5521-6e23-49b8-9870-f5370def487e
title: Один файл имеет версию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417060119f8b13b1545161faa80552c79e8ca9aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155130"
---
# <a name="one-file-has-a-version"></a><span data-ttu-id="84032-103">Один файл имеет версию</span><span class="sxs-lookup"><span data-stu-id="84032-103">One File Has a Version</span></span>

<span data-ttu-id="84032-104">Если файл ключа устанавливаемого компонента (Copy-A) имеет то же имя, что и файл, уже установленный в целевом расположении (Copy-B), установщик сравнивает номер версии, дату и язык двух файлов.</span><span class="sxs-lookup"><span data-stu-id="84032-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="84032-105">Если только один из файлов имеет номер версии, установщик использует логику, показанную на следующей схеме потока, чтобы определить, следует ли заменить все установленные файлы, принадлежащие компоненту.</span><span class="sxs-lookup"><span data-stu-id="84032-105">If only one of the files has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="84032-106">Поскольку установщик устанавливает только компоненты целиком, при замене установленного файла ключей все файлы компонента заменяются.</span><span class="sxs-lookup"><span data-stu-id="84032-106">Because the installer only installs entire components, if the installed key file is replaced, then all of the component's files are replaced.</span></span>

<span data-ttu-id="84032-107">Обратите внимание, что на этой диаграмме показаны [правила управления версиями файлов](file-versioning-rules.md)по умолчанию, которые можно переопределить, задав свойство [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="84032-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="84032-108">Значение свойства **REINSTALLMODE** по умолчанию — "omus".</span><span class="sxs-lookup"><span data-stu-id="84032-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![правила управления версиями файлов по умолчанию, если только один файл имеет номер версии](images/waiflow3.png)

<span data-ttu-id="84032-110">См. Примеры управления версиями файлов по умолчанию при [замене существующих файлов](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="84032-110">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="84032-111">Оба файла имеют версию</span><span class="sxs-lookup"><span data-stu-id="84032-111">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="84032-112">Ни один из файлов не имеет версии</span><span class="sxs-lookup"><span data-stu-id="84032-112">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="84032-113">Ни один из файлов не имеет версии с проверками хэша файла</span><span class="sxs-lookup"><span data-stu-id="84032-113">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)

 

 



