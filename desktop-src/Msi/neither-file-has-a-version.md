---
description: Если ни один из файлов не имеет номера версии, установщик Windows использует логику, показанную на следующей схеме потока, чтобы определить, следует ли заменить все установленные файлы, относящиеся к компоненту.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Ни один из файлов не имеет версии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5360bb7b6b4deda54156006073f353ab65ab2b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552311"
---
# <a name="neither-file-has-a-version"></a><span data-ttu-id="03fac-103">Ни один из файлов не имеет версии</span><span class="sxs-lookup"><span data-stu-id="03fac-103">Neither File Has a Version</span></span>

<span data-ttu-id="03fac-104">Если файл ключа устанавливаемого компонента (Copy-A) имеет то же имя, что и файл, уже установленный в целевом расположении (Copy-B), установщик сравнивает номер версии, дату и язык двух файлов.</span><span class="sxs-lookup"><span data-stu-id="03fac-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="03fac-105">Если ни один из файлов не имеет номера версии, установщик использует логику, показанную на следующей схеме потока, чтобы определить, следует ли заменить все установленные файлы, относящиеся к компоненту.</span><span class="sxs-lookup"><span data-stu-id="03fac-105">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="03fac-106">Поскольку установщик устанавливает только компоненты целиком, при замене установленного файла ключей все файлы компонента заменяются.</span><span class="sxs-lookup"><span data-stu-id="03fac-106">Because the installer only installs entire components, if the installed key file is replaced, then all of the component's files are replaced.</span></span>

<span data-ttu-id="03fac-107">Обратите внимание, что на этой диаграмме показаны [правила управления версиями файлов](file-versioning-rules.md)по умолчанию, которые можно переопределить, задав свойство [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="03fac-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="03fac-108">Значение свойства **REINSTALLMODE** по умолчанию — "omus".</span><span class="sxs-lookup"><span data-stu-id="03fac-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![правила управления версиями файлов по умолчанию, если ни один из файлов не имеет номера версии](images/waiflow2.png)

<span data-ttu-id="03fac-110">См. Примеры управления версиями файлов по умолчанию при [замене существующих файлов](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="03fac-110">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="03fac-111">Оба файла имеют версию</span><span class="sxs-lookup"><span data-stu-id="03fac-111">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="03fac-112">Ни один из файлов не имеет версии с проверками хэша файла</span><span class="sxs-lookup"><span data-stu-id="03fac-112">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="03fac-113">Один файл имеет версию</span><span class="sxs-lookup"><span data-stu-id="03fac-113">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



