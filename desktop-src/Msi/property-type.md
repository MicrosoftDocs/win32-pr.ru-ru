---
description: Тип свойства семантического типа является одним из типов формата ключа. Этот тип состоит из внешнего ключа в таблицу свойств, предоставленную пользователем.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Тип свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36236c78160abbfe3ad64c6b801a3cdbdbb98b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080764"
---
# <a name="property-type"></a><span data-ttu-id="7ebec-104">Тип свойства</span><span class="sxs-lookup"><span data-stu-id="7ebec-104">Property Type</span></span>

<span data-ttu-id="7ebec-105">Тип свойства [семантического типа](semantic-types.md) является одним из [типов формата ключа](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="7ebec-105">The Property Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="7ebec-106">Этот тип состоит из внешнего ключа в [таблицу свойств](property-table.md) , предоставленную пользователем.</span><span class="sxs-lookup"><span data-stu-id="7ebec-106">This type consists of a foreign key into the [Property table](property-table.md) provided by the user.</span></span>

<span data-ttu-id="7ebec-107">Средство слияния должно заменить допустимый [идентификатор](identifier.md) установщик Windows для элементов этого типа.</span><span class="sxs-lookup"><span data-stu-id="7ebec-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="7ebec-108">Mergemod.dll не применяет это ограничение и является средством слияния, чтобы убедиться, что пользователь предоставляет допустимый ключ в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="7ebec-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Property table.</span></span> <span data-ttu-id="7ebec-109">Первичными ключами таблицы свойств являются имена свойств.</span><span class="sxs-lookup"><span data-stu-id="7ebec-109">The primary keys of the Property table are the property names.</span></span>

<span data-ttu-id="7ebec-110">Значение null является допустимым для этого типа, если только Мсмконфигитемноннуллабле не включен в поле Attributes [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="7ebec-110">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="7ebec-111">Тип свойства можно использовать со следующими видами Контекстдата.</span><span class="sxs-lookup"><span data-stu-id="7ebec-111">The Property type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="7ebec-112">**Контекстдата null**</span><span class="sxs-lookup"><span data-stu-id="7ebec-112">**Null ContextData**</span></span>

<span data-ttu-id="7ebec-113">Настраиваемый модуль слияния может использовать этот тип, чтобы предоставить пользователю возможность указать имя свойства для таблицы базы данных в модуле.</span><span class="sxs-lookup"><span data-stu-id="7ebec-113">A configurable merge module may use this type to enable the user to provide a property name to a database table in the module.</span></span> <span data-ttu-id="7ebec-114">Средство слияния заменяет идентификатор свойства на шаблоны в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7ebec-114">The merge tool substitutes the property's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="7ebec-115">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя настраиваемого элемента в столбец "имя", ввести "1" в столбец "формат", ввести "свойство" в столбец "тип" и оставить пустой столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="7ebec-115">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Property" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="7ebec-116">**Общедоступная Контекстдата**</span><span class="sxs-lookup"><span data-stu-id="7ebec-116">**Public ContextData**</span></span>

<span data-ttu-id="7ebec-117">Настраиваемый модуль слияния может использовать этот тип, чтобы предоставить пользователю имя [открытого свойства](public-properties.md) для таблицы базы данных в модуле.</span><span class="sxs-lookup"><span data-stu-id="7ebec-117">A configurable merge module may use this type to enable the user to provide the name of a [public property](public-properties.md) to a database table in the module.</span></span> <span data-ttu-id="7ebec-118">Средство слияния заменяет идентификатор свойства на шаблоны в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7ebec-118">The merge tool substitutes the property's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="7ebec-119">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя настраиваемого элемента в столбец "имя", ввести "1" в столбец "формат", ввести "свойство" в столбец типа и ввести "Public" в столбец Контекстдата таблицы Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="7ebec-119">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Property" into the Type column, and enter "Public" into the ContextData column of the ModuleConfiguration table.</span></span>

<span data-ttu-id="7ebec-120">**Частный Контекстдата**</span><span class="sxs-lookup"><span data-stu-id="7ebec-120">**Private ContextData**</span></span>

<span data-ttu-id="7ebec-121">Настраиваемый модуль слияния может использовать этот тип, чтобы предоставить пользователю возможность указать имя [закрытого свойства](private-properties.md) в таблице базы данных в модуле.</span><span class="sxs-lookup"><span data-stu-id="7ebec-121">A configurable merge module may use this type to enable the user to provide the name of a [private property](private-properties.md) to a database table in the module.</span></span> <span data-ttu-id="7ebec-122">Средство слияния заменяет идентификатор свойства на шаблоны в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7ebec-122">The merge tool substitutes the property's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="7ebec-123">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя настраиваемого элемента в столбец "имя", ввести "1" в столбец "формат", ввести "свойство" в столбец типа и ввести "Private" в столбец Контекстдата таблицы Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="7ebec-123">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Property" into the Type column, and enter "Private" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



