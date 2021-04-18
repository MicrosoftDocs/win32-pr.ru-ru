---
description: Тип семантики RTF является одним из типов текстовых форматов.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: Тип RTF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81c708183596d794f20e38bf89c073472e3affb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650851"
---
# <a name="rtf-type"></a><span data-ttu-id="7925a-103">Тип RTF</span><span class="sxs-lookup"><span data-stu-id="7925a-103">RTF Type</span></span>

<span data-ttu-id="7925a-104">Тип [семантики](semantic-types.md) RTF является одним из [типов текстовых форматов](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="7925a-104">The RTF Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="7925a-105">Этот тип состоит из произвольной текстовой строки в формате RTF для любой длины, предоставленной пользователем.</span><span class="sxs-lookup"><span data-stu-id="7925a-105">This type consists of an arbitrary text string in the Rich Text Format (RTF) of any length provided by the user.</span></span> <span data-ttu-id="7925a-106">Средство слияния заменяет эту строку на шаблоны, указанные в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7925a-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="7925a-107">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя текстовой строки в столбец "имя", ввести "0" в столбец "формат", ввести "RTF" в столбец "тип" и оставить пустой столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md). Строка может находиться на любом языке, совместимом с кодовой страницей базы данных.</span><span class="sxs-lookup"><span data-stu-id="7925a-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "RTF" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="7925a-108">См. раздел [Обработка кодовой страницы (установщик Windows)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="7925a-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="7925a-109">Значение null является допустимым для текстовой строки, если только Мсмконфигитемноннуллабле не включен в поле Attributes таблицы Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="7925a-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



