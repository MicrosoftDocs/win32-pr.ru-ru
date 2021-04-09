---
description: Отформатированный тип семантического типа является одним из типов текстовых форматов.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Форматированный тип
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080474"
---
# <a name="formatted-type"></a><span data-ttu-id="daec7-103">Форматированный тип</span><span class="sxs-lookup"><span data-stu-id="daec7-103">Formatted Type</span></span>

<span data-ttu-id="daec7-104">Отформатированный тип [семантического типа](semantic-types.md) является одним из [типов текстовых форматов](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="daec7-104">The Formatted Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="daec7-105">Этот тип состоит из произвольной текстовой строки любой длины, предоставленной пользователем, а также в формате установщик Windows форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="daec7-105">This type consists of an arbitrary text string of any length provided by the user and in the Windows Installer formatted text format.</span></span> <span data-ttu-id="daec7-106">Дополнительные сведения см. в разделе [форматированный](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="daec7-106">For details, see [Formatted](formatted.md).</span></span> <span data-ttu-id="daec7-107">Средство слияния заменяет эту строку на шаблоны, указанные в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="daec7-107">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="daec7-108">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя текстовой строки в столбец "имя", ввести "0" в столбец "формат", ввести "форматированный" в столбец "тип" и оставить пустой столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md). Строка может находиться на любом языке, совместимом с кодовой страницей базы данных.</span><span class="sxs-lookup"><span data-stu-id="daec7-108">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Formatted" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="daec7-109">Дополнительные сведения см. в разделе [Обработка кодовых страниц (установщик Windows)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="daec7-109">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="daec7-110">Значение null является допустимым для текстовой строки, если только Мсмконфигитемноннуллабле не включен в поле Attributes таблицы Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="daec7-110">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



