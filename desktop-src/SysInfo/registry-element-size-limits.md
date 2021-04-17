---
description: В следующей таблице приведены ограничения по размеру для различных элементов реестра.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Ограничения размера элементов реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 262609a64e60536dcfc41f29e5d94ea499158861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663500"
---
# <a name="registry-element-size-limits"></a><span data-ttu-id="8b47c-103">Ограничения размера элементов реестра</span><span class="sxs-lookup"><span data-stu-id="8b47c-103">Registry Element Size Limits</span></span>

<span data-ttu-id="8b47c-104">В следующей таблице приведены ограничения по размеру для различных элементов реестра.</span><span class="sxs-lookup"><span data-stu-id="8b47c-104">The following table identifies the size limits for the various registry elements.</span></span>



| <span data-ttu-id="8b47c-105">Элемент реестра</span><span class="sxs-lookup"><span data-stu-id="8b47c-105">Registry Element</span></span> | <span data-ttu-id="8b47c-106">Максимальный размер</span><span class="sxs-lookup"><span data-stu-id="8b47c-106">Size Limit</span></span>                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b47c-107">Имя раздела</span><span class="sxs-lookup"><span data-stu-id="8b47c-107">Key name</span></span>         | <span data-ttu-id="8b47c-108">255 символов.</span><span class="sxs-lookup"><span data-stu-id="8b47c-108">255 characters.</span></span> <span data-ttu-id="8b47c-109">Имя ключа включает абсолютный путь к разделу в реестре, который всегда начинается с базового ключа, например HKEY \_ локальный \_ компьютер.</span><span class="sxs-lookup"><span data-stu-id="8b47c-109">The key name includes the absolute path of the key in the registry, always starting at a base key, for example, HKEY\_LOCAL\_MACHINE.</span></span> |
| <span data-ttu-id="8b47c-110">Имя значения</span><span class="sxs-lookup"><span data-stu-id="8b47c-110">Value name</span></span>       | <span data-ttu-id="8b47c-111">16 383 символов **Windows 2000:** 260 ANSI символов или 16 383 символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="8b47c-111">16,383 characters **Windows 2000:** 260 ANSI characters or 16,383 Unicode characters.</span></span><br/>                                                       |
| <span data-ttu-id="8b47c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8b47c-112">Value</span></span>            | <span data-ttu-id="8b47c-113">Доступная память (последний формат) 1 МБ (стандартный формат)</span><span class="sxs-lookup"><span data-stu-id="8b47c-113">Available memory (latest format)1 MB (standard format)</span></span><br/>                                                                                     |
| <span data-ttu-id="8b47c-114">Дерево</span><span class="sxs-lookup"><span data-stu-id="8b47c-114">Tree</span></span>             | <span data-ttu-id="8b47c-115">Дерево реестра может иметь глубину 512 уровней.</span><span class="sxs-lookup"><span data-stu-id="8b47c-115">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="8b47c-116">С помощью одного вызова API реестра можно создать до 32 уровней за раз.</span><span class="sxs-lookup"><span data-stu-id="8b47c-116">You can create up to 32 levels at a time through a single registry API call.</span></span>                                  |



 

<span data-ttu-id="8b47c-117">Длинные значения (более 2 048 байт) должны храниться в файле, а расположение файла должно храниться в реестре.</span><span class="sxs-lookup"><span data-stu-id="8b47c-117">Long values (more than 2,048 bytes) should be stored in a file, and the location of the file should be stored in the registry.</span></span> <span data-ttu-id="8b47c-118">Это помогает реестру работать эффективно.</span><span class="sxs-lookup"><span data-stu-id="8b47c-118">This helps the registry perform efficiently.</span></span>

<span data-ttu-id="8b47c-119">Расположением файла может быть имя значения или данные значения.</span><span class="sxs-lookup"><span data-stu-id="8b47c-119">The file location can be the name of a value or the data of a value.</span></span> <span data-ttu-id="8b47c-120">Каждой обратной косой черте в строке расположения должна предшествовать другая обратная косая черта в виде escape-символа.</span><span class="sxs-lookup"><span data-stu-id="8b47c-120">Each backslash in the location string must be preceded by another backslash as an escape character.</span></span> <span data-ttu-id="8b47c-121">Например, укажите "C: \\ \\ MyDir \\ \\ MyFile", чтобы сохранить строку "c: \\ MyDir \\ MyFile".</span><span class="sxs-lookup"><span data-stu-id="8b47c-121">For example, specify "C:\\\\mydir\\\\myfile" to store the string "C:\\mydir\\myfile".</span></span> <span data-ttu-id="8b47c-122">Расположение файла также может быть именем ключа, если оно находится в пределах 255 символов в именах ключей и не содержит обратных косых черт, которые не допускаются в именах ключей.</span><span class="sxs-lookup"><span data-stu-id="8b47c-122">A file location can also be the name of a key if it is within the 255-character limit for key names and does not contain backslashes, which are not allowed in key names.</span></span>

 

 




