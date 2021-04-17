---
description: Если модуль поддерживает несколько языков, его можно объединить в одну базу данных установщик Windows несколько раз, но убедитесь, что в каждом слиянии используется другой язык.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Несколько раз объединить многоязыковый модуль в один пакет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674121"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a><span data-ttu-id="8d0e2-103">Несколько раз объединить многоязыковый модуль в один пакет</span><span class="sxs-lookup"><span data-stu-id="8d0e2-103">Merging a Multiple Language Module into the Same Package Multiple Times</span></span>

<span data-ttu-id="8d0e2-104">Если модуль поддерживает несколько языков, его можно объединить в одну базу данных установщик Windows несколько раз, но убедитесь, что в каждом слиянии используется другой язык.</span><span class="sxs-lookup"><span data-stu-id="8d0e2-104">When a module supports multiple languages, you can merge it into the same Windows Installer database multiple times, but make sure that each merge uses a different language.</span></span> <span data-ttu-id="8d0e2-105">Перед каждым слиянием запросите другой язык из модуля.</span><span class="sxs-lookup"><span data-stu-id="8d0e2-105">Before each merge, request a different language from the module.</span></span> <span data-ttu-id="8d0e2-106">Результирующая база данных. msi затем содержит запись в [таблице ModuleSignature](modulesignature-table.md) для каждого объединения модуля.</span><span class="sxs-lookup"><span data-stu-id="8d0e2-106">The resulting .msi database then has a record in the [ModuleSignature Table](modulesignature-table.md) for each merge of the module.</span></span> <span data-ttu-id="8d0e2-107">Компоненты, которые являются общими для разных языков, существуют только один раз в [таблице Component](component-table.md), но связаны с каждым языком в [таблице модулекомпонентс](modulecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="8d0e2-107">Components that are shared between languages exist only one time in the [Component Table](component-table.md), but are associated with each language in the [ModuleComponents Table](modulecomponents-table.md).</span></span>

<span data-ttu-id="8d0e2-108">При объединении нескольких языков модуля в один пакет каждое слияние должно соответствовать тем же ограничениям кодовых страниц, что и модули с одним языком.</span><span class="sxs-lookup"><span data-stu-id="8d0e2-108">When merging multiple languages of a module into the same package, each merge must satisfy the same restrictions on code pages as single-language modules.</span></span> <span data-ttu-id="8d0e2-109">Модули не могут содержать строки в разных кодовых страницах.</span><span class="sxs-lookup"><span data-stu-id="8d0e2-109">The modules cannot contain strings in different code pages.</span></span>

<span data-ttu-id="8d0e2-110">При многократном объединении модуля в один MSI-файл может потребоваться изменить порядок файлов в [таблице File](file-table.md) для использования существующего CAB-файла из модуля непосредственно в установке.</span><span class="sxs-lookup"><span data-stu-id="8d0e2-110">When merging a module multiple times into a single .msi file, you may need to modify the order of the files in the [File Table](file-table.md) to use the existing .cab from the module directly in your installation.</span></span> <span data-ttu-id="8d0e2-111">Порядок файлов в таблице File должен соответствовать порядку файлов в CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="8d0e2-111">The order of files in the File Table must match the order of files in the .cab.</span></span> <span data-ttu-id="8d0e2-112">При многократном объединении модуля в базу данных установки последовательность может быть изменена, поскольку файлы, общие для разных языков, уже существуют в модуле из предыдущей операции слияния и имеют другой относительный порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="8d0e2-112">When merging a module multiple times into an installation database the sequence may be modified, because files shared between the languages may already exist in the module from a prior merge, and they have a different relative sequence number.</span></span>

 

 



