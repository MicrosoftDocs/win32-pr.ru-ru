---
description: Произвольный тип текста семантического типа является одним из типов текстовых форматов.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Произвольный тип текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662949"
---
# <a name="arbitrary-text-type"></a><span data-ttu-id="705f4-103">Произвольный тип текста</span><span class="sxs-lookup"><span data-stu-id="705f4-103">Arbitrary Text Type</span></span>

<span data-ttu-id="705f4-104">Произвольный тип текста [семантического типа](semantic-types.md) является одним из [типов текстовых форматов](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="705f4-104">The Arbitrary Text Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="705f4-105">Этот тип состоит из произвольной текстовой строки любой длины, предоставленной пользователем.</span><span class="sxs-lookup"><span data-stu-id="705f4-105">This type consists of an arbitrary text string of any length provided by the user.</span></span> <span data-ttu-id="705f4-106">Средство слияния заменяет эту произвольную строку на шаблоны, указанные в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="705f4-106">The merge tool substitutes this arbitrary string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="705f4-107">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя текстовой строки в столбец Name, ввести "0" в столбец Format и оставить пустыми столбцы Type и Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md). Произвольная текстовая строка может находиться на любом языке, совместимом с кодовой страницей базы данных.</span><span class="sxs-lookup"><span data-stu-id="705f4-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).The arbitrary text string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="705f4-108">Дополнительные сведения см. в разделе [Обработка кодовых страниц (установщик Windows)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="705f4-108">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="705f4-109">Значение null является допустимым для текстовой строки, если только Мсмконфигитемноннуллабле не включен в поле Attributes таблицы Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="705f4-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



