---
description: При объединении модуля в базу данных установки существует два важных языка.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Открытие модуля слияния Multiple-Language на определенном языке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080396"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a><span data-ttu-id="943ab-103">Открытие модуля слияния Multiple-Language на определенном языке</span><span class="sxs-lookup"><span data-stu-id="943ab-103">Opening a Multiple-Language Merge Module in a Specific Language</span></span>

<span data-ttu-id="943ab-104">При объединении модуля в базу данных установки существует два важных языка.</span><span class="sxs-lookup"><span data-stu-id="943ab-104">When merging a module into an installation database, there are two important languages.</span></span> <span data-ttu-id="943ab-105">Первый — это язык целевого пакета установки, заданный параметром [**продуктлангуаже**](productlanguage.md) в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="943ab-105">The first is the language of the target installation package specified by [**ProductLanguage**](productlanguage.md) in the [Property Table](property-table.md).</span></span> <span data-ttu-id="943ab-106">Второй — это язык модуля слияния, который отображается в столбце Language [таблицы ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="943ab-106">The second is the language of the merge module that appears in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="943ab-107">Язык пакета установки может быть передан в модуль средством слияния при открытии пакета для слияния.</span><span class="sxs-lookup"><span data-stu-id="943ab-107">The language of the installation package can be passed to the module by the merge tool when the package is opened for a merge.</span></span> <span data-ttu-id="943ab-108">Тем не менее иногда может потребоваться проигнорировать язык целевого объекта и запросить открытие модуля на другом языке, например на английском языке, устанавливающем ресурсы на английском и немецком языках из модуля.</span><span class="sxs-lookup"><span data-stu-id="943ab-108">However, sometimes it may be necessary to disregard the language of the target, and request that the module be opened in another language, for example, an English package installing both the English and German resources from the module.</span></span>

<span data-ttu-id="943ab-109">При открытии модуля с запросом языка средство слияния проверяет запрошенный язык по языкам, указанным в столбце Language [таблицы ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="943ab-109">When opening a module with a language request, the merge tool checks the requested language against the languages that are specified in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="943ab-110">Для определения используемого языка используется следующий процесс.</span><span class="sxs-lookup"><span data-stu-id="943ab-110">The following process is used to determine which language to use.</span></span>

<span data-ttu-id="943ab-111">**Определение языка для использования**</span><span class="sxs-lookup"><span data-stu-id="943ab-111">**To determine which language to use**</span></span>

1.  <span data-ttu-id="943ab-112">Если язык в [таблице ModuleSignature](modulesignature-table.md) больше или равен значению запрошенного языка, то открывается модуль.</span><span class="sxs-lookup"><span data-stu-id="943ab-112">If the language in the [ModuleSignature Table](modulesignature-table.md) is equal or more general than the requested language, the module opens.</span></span>
2.  <span data-ttu-id="943ab-113">Если модуль поддерживает точный запрошенный язык, используется этот язык.</span><span class="sxs-lookup"><span data-stu-id="943ab-113">If the module supports the exact language requested, that language is used.</span></span>
3.  <span data-ttu-id="943ab-114">Если модуль поддерживает языковую группу, в которой запрашивается языковая группа, например, проверка 9, если 1033 была запрошена, но не найдена на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="943ab-114">If the module supports the language group of the language requested that language group is used, for example, check 9 if 1033 was requested but not found in step 2.</span></span>
4.  <span data-ttu-id="943ab-115">Проверьте, есть ли преобразование языка, которое изменяет модуль на нейтральный.</span><span class="sxs-lookup"><span data-stu-id="943ab-115">Check if there is a language transform that changes the module to neutral.</span></span>
5.  <span data-ttu-id="943ab-116">Если ни один из предыдущих шагов не выполнен, модуль не поддерживает запрошенный язык и слияние завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="943ab-116">If none of the previous steps succeed, the module does not support the requested language and the merge fails.</span></span>

 

 



