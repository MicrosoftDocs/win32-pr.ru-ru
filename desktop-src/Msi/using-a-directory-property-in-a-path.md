---
description: Каталоги в таблице Directory определяют структуру установки.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Использование свойства каталога в пути
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674366"
---
# <a name="using-a-directory-property-in-a-path"></a><span data-ttu-id="4e833-103">Использование свойства каталога в пути</span><span class="sxs-lookup"><span data-stu-id="4e833-103">Using a Directory Property in a Path</span></span>

<span data-ttu-id="4e833-104">Каталоги в [таблице Directory](directory-table.md) определяют структуру установки.</span><span class="sxs-lookup"><span data-stu-id="4e833-104">The directories in the [Directory table](directory-table.md) specify the layout of an installation.</span></span> <span data-ttu-id="4e833-105">Когда установщик Windows разрешает эти каталоги во время [действия костфинализе](costfinalize-action.md), ключи в таблице Directory становятся [свойствами](properties.md) , для которых заданы пути к каталогам.</span><span class="sxs-lookup"><span data-stu-id="4e833-105">When the Windows Installer resolves these directories during the [CostFinalize action](costfinalize-action.md), the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span> <span data-ttu-id="4e833-106">Кроме того, установщик всегда задает для системных папок несколько стандартных [свойств системной папки](property-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="4e833-106">The installer also always sets a number of standard [System Folder Properties](property-reference.md) to system folder paths.</span></span>

<span data-ttu-id="4e833-107">Значения [свойств системной папки](property-reference.md) гарантированно заканчиваются разделителем каталогов.</span><span class="sxs-lookup"><span data-stu-id="4e833-107">The values of the [System Folder Properties](property-reference.md) are guaranteed to end in a directory separator.</span></span> <span data-ttu-id="4e833-108">Значения всех остальных свойств, вводимых в [таблице Directory](directory-table.md) , гарантированно заканчиваются разделителем каталогов после того, как установщик запустит [действие костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="4e833-108">The values of all other properties entered in the [Directory table](directory-table.md) are only guaranteed to end in a directory separator after the installer has run the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="4e833-109">Перед завершением учета стоимости значения свойств, которые были указаны в таблице каталога, которые не являются [свойствами системной папки](property-reference.md) , могут не заканчиваться разделителем каталогов.</span><span class="sxs-lookup"><span data-stu-id="4e833-109">Before costing has completed, the values of properties entered in the Directory table which are not [System Folder Properties](property-reference.md) may not end in a directory separator.</span></span> <span data-ttu-id="4e833-110">Таким образом, если установка устанавливает свойства каталога с помощью [настраиваемых действий](custom-actions.md) в пакете, значения в ссылке могут не заканчиваться разделителем каталогов.</span><span class="sxs-lookup"><span data-stu-id="4e833-110">Therefore, if your installation sets directory properties using [custom actions](custom-actions.md) in the package, the values on reference might not end with a directory separator.</span></span>

<span data-ttu-id="4e833-111">Таким образом, свойства каталога, которые заканчиваются разделителем каталогов, можно использовать в строке пути без явного включения разделителя каталогов.</span><span class="sxs-lookup"><span data-stu-id="4e833-111">Directory properties ending with a directory separator can therefore be used in a path string without explicitly including the directory separator.</span></span> <span data-ttu-id="4e833-112">Например, если значение Директорипроперти заканчивается разделителем каталога, следующая строка правильно указывает путь к *файлу* в *подкаталоге*</span><span class="sxs-lookup"><span data-stu-id="4e833-112">For example, if the value of DirectoryProperty ends with a directory separator, the following string correctly specifies the path to *file* in *subdirectory*</span></span>

``` syntax
[DirectoryProperty]subdirectory\file
```

<span data-ttu-id="4e833-113">и следующая строка пути неверна.</span><span class="sxs-lookup"><span data-stu-id="4e833-113">and the following path string is incorrect.</span></span>

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



