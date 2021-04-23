---
description: Хэширование файлов доступно в установщик Windows. Дополнительные сведения см. в разделе Мсижетфилехаш и таблица Мсифилехаш. Таблицу Мсифилехаш можно использовать только с файлами без версий.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Ни один из файлов не имеет версии с проверками хэша файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544255"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a><span data-ttu-id="64b3e-105">Ни один из файлов не имеет версии с проверками хэша файла</span><span class="sxs-lookup"><span data-stu-id="64b3e-105">Neither File Has a Version with File Hash Check</span></span>

<span data-ttu-id="64b3e-106">Хэширование файлов доступно в установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="64b3e-106">File hashing is available with Windows Installer.</span></span> <span data-ttu-id="64b3e-107">Дополнительные сведения см. в разделе [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) и [Таблица мсифилехаш](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="64b3e-107">For more information, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="64b3e-108">Таблицу Мсифилехаш можно использовать только с файлами без версий.</span><span class="sxs-lookup"><span data-stu-id="64b3e-108">The MsiFileHash table can only be used with unversioned files.</span></span>

<span data-ttu-id="64b3e-109">Если файл ключа устанавливаемого компонента (Copy-A) имеет то же имя, что и файл, уже установленный в целевом расположении (Copy-B), установщик сравнивает номер версии, дату и язык двух файлов.</span><span class="sxs-lookup"><span data-stu-id="64b3e-109">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="64b3e-110">Если ни один из файлов не имеет номера версии, установщик использует логику, показанную на следующей схеме потока, чтобы определить, следует ли заменить все установленные файлы, относящиеся к компоненту.</span><span class="sxs-lookup"><span data-stu-id="64b3e-110">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="64b3e-111">Поскольку установщик устанавливает только компоненты целиком, если установленный файл ключа заменяется, все файлы компонента заменяются.</span><span class="sxs-lookup"><span data-stu-id="64b3e-111">Because the installer only installs entire components, if the installed key file is replaced then, all of the component's files are replaced.</span></span>

<span data-ttu-id="64b3e-112">Обратите внимание, что на этой диаграмме показаны [правила управления версиями файлов](file-versioning-rules.md)по умолчанию, которые можно переопределить, задав свойство [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="64b3e-112">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="64b3e-113">Значение свойства **REINSTALLMODE** по умолчанию — "omus".</span><span class="sxs-lookup"><span data-stu-id="64b3e-113">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![правила управления версиями файлов по умолчанию при переопределении с помощью параметра свойства REINSTALLMODE](images/waiflow2b.png)

<span data-ttu-id="64b3e-115">См. Примеры управления версиями файлов по умолчанию при [замене существующих файлов](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="64b3e-115">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="64b3e-116">Оба файла имеют версию</span><span class="sxs-lookup"><span data-stu-id="64b3e-116">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="64b3e-117">Ни один из файлов не имеет версии</span><span class="sxs-lookup"><span data-stu-id="64b3e-117">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="64b3e-118">Один файл имеет версию</span><span class="sxs-lookup"><span data-stu-id="64b3e-118">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



