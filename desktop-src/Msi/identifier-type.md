---
description: Тип идентификатора семантического типа является одним из типов текстовых форматов.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Тип идентификатора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156327"
---
# <a name="identifier-type"></a><span data-ttu-id="1fa4f-103">Тип идентификатора</span><span class="sxs-lookup"><span data-stu-id="1fa4f-103">Identifier Type</span></span>

<span data-ttu-id="1fa4f-104">Тип идентификатора [семантического типа](semantic-types.md) является одним из [типов текстовых форматов](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="1fa4f-104">The Identifier Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="1fa4f-105">Этот тип состоит из текстовой строки, предоставленной пользователем в формате [идентификатора](identifier.md)установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="1fa4f-105">This type consists of an text string provided by the user in the format of a Windows Installer [Identifier](identifier.md).</span></span> <span data-ttu-id="1fa4f-106">Средство слияния заменяет эту строку на шаблоны, указанные в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="1fa4f-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="1fa4f-107">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя текстовой строки в столбец Name, ввести "0" в столбец Format, ввести "идентификатор" в столбец Type и оставить пустой столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md). Строка может находиться на любом языке, совместимом с кодовой страницей базы данных.</span><span class="sxs-lookup"><span data-stu-id="1fa4f-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Identifier" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="1fa4f-108">См. раздел [Обработка кодовой страницы (установщик Windows)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="1fa4f-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="1fa4f-109">Значение null является допустимым для текстовой строки, если только Мсмконфигитемноннуллабле не включен в поле Attributes таблицы Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="1fa4f-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



