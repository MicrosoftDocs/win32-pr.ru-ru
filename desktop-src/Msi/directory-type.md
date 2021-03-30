---
description: Тип семантического типа является одним из типов формата ключа, который состоит из внешнего ключа в таблицу каталога, предоставленную пользователем.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Тип каталога
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910955"
---
# <a name="directory-type"></a><span data-ttu-id="7d348-103">Тип каталога</span><span class="sxs-lookup"><span data-stu-id="7d348-103">Directory Type</span></span>

<span data-ttu-id="7d348-104">Тип [семантического типа](semantic-types.md) является одним из [типов формата ключа](key-format-types.md), который состоит из внешнего ключа в [таблицу каталога](directory-table.md) , предоставленную пользователем.</span><span class="sxs-lookup"><span data-stu-id="7d348-104">The Directory Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md), which consists of a foreign key into the [Directory table](directory-table.md) provided by the user.</span></span>

<span data-ttu-id="7d348-105">Средство слияния должно заменить допустимый [идентификатор](identifier.md) установщик Windows для элементов этого типа.</span><span class="sxs-lookup"><span data-stu-id="7d348-105">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="7d348-106">Mergemod.dll не применяет это ограничение и является средством слияния, чтобы убедиться, что пользователь предоставляет допустимый ключ в таблице Directory.</span><span class="sxs-lookup"><span data-stu-id="7d348-106">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Directory table.</span></span>

<span data-ttu-id="7d348-107">Настраиваемый элемент типа каталога должен изменять только целевой каталог установки и не изменять исходный образ.</span><span class="sxs-lookup"><span data-stu-id="7d348-107">A configurable item of the Directory type should only modify the destination directory of the installation and not modify the source image.</span></span> <span data-ttu-id="7d348-108">Поэтому настраиваемый элемент этого типа должен изменять только внешние ключи в таблице каталога и не изменять таблицу каталога напрямую.</span><span class="sxs-lookup"><span data-stu-id="7d348-108">A configurable item of this type should therefore only modify foreign keys to the Directory table and not modify the Directory table directly.</span></span>

<span data-ttu-id="7d348-109">Поскольку столбец каталога \_ [таблицы Component](component-table.md) не допускает значения NULL, значение NULL недопустимо для настраиваемого элемента этого типа, даже если мсмконфигитемноннуллабле не задан в столбце Attributes.</span><span class="sxs-lookup"><span data-stu-id="7d348-109">Because the Directory\_ column of the [Component table](component-table.md) is non-nullable, null is an invalid value for a configurable item of this type even if the msmConfigItemNonNullable is not set in the Attributes column.</span></span>

<span data-ttu-id="7d348-110">Тип каталога можно использовать с двумя видами Контекстдата.</span><span class="sxs-lookup"><span data-stu-id="7d348-110">The Directory type may be used with two kinds of ContextData.</span></span>

<span data-ttu-id="7d348-111">**Исолатиондиректори Контекстдата**</span><span class="sxs-lookup"><span data-stu-id="7d348-111">**IsolationDirectory ContextData**</span></span>

<span data-ttu-id="7d348-112">Настраиваемый модуль слияния может использовать этот тип, чтобы позволить пользователю предоставить каталог назначения для файлов в модуле.</span><span class="sxs-lookup"><span data-stu-id="7d348-112">A configurable merge module may use this type to enable the user to provide a destination directory for files in the module.</span></span> <span data-ttu-id="7d348-113">Средство слияния заменяет идентификатор каталога на шаблоны в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7d348-113">The merge tool substitutes the directory's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="7d348-114">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя каталога в столбец "имя", ввести "1" в столбец "формат", ввести "Directory" в столбец Type и ввести "Исолатиондиректори" в столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="7d348-114">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "IsolationDirectory" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="7d348-115">**Шорткутлокатион Контекстдата**</span><span class="sxs-lookup"><span data-stu-id="7d348-115">**ShortcutLocation ContextData**</span></span>

<span data-ttu-id="7d348-116">Настраиваемый модуль слияния может использовать этот тип, чтобы позволить пользователю предоставить каталог назначения для ярлыков в модуле.</span><span class="sxs-lookup"><span data-stu-id="7d348-116">A configurable merge module may use this type to enable the user to provide a destination directory for shortcuts in the module.</span></span> <span data-ttu-id="7d348-117">Средство слияния заменяет идентификатор ярлыка на шаблоны в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7d348-117">The merge tool substitutes the shortcut's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="7d348-118">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя каталога в столбец "имя", ввести "1" в столбец "формат", ввести "Directory" в столбец Type и ввести "Шорткутлокатион" в столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="7d348-118">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "ShortcutLocation" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



