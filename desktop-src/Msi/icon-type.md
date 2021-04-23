---
description: Тип значка семантического типа является одним из типов формата ключа. Этот тип состоит из ключа в таблицу значков, предоставленную пользователем.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Тип значка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7c90de925ff34977e7ff192dffe0b8614e5734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650576"
---
# <a name="icon-type"></a><span data-ttu-id="14435-104">Тип значка</span><span class="sxs-lookup"><span data-stu-id="14435-104">Icon Type</span></span>

<span data-ttu-id="14435-105">Тип значка [семантического типа](semantic-types.md) является одним из [типов формата ключа](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="14435-105">The Icon Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="14435-106">Этот тип состоит из ключа в [таблицу значков](icon-table.md) , предоставленную пользователем.</span><span class="sxs-lookup"><span data-stu-id="14435-106">This type consists of a key into the [Icon table](icon-table.md) provided by the user.</span></span>

<span data-ttu-id="14435-107">Средство слияния должно заменить допустимый [идентификатор](identifier.md) установщик Windows для элементов этого типа.</span><span class="sxs-lookup"><span data-stu-id="14435-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="14435-108">Mergemod.dll не применяет это ограничение и является средством слияния, чтобы убедиться, что пользователь предоставляет допустимый ключ в таблице значков.</span><span class="sxs-lookup"><span data-stu-id="14435-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Icon table.</span></span>

<span data-ttu-id="14435-109">Значение null является допустимым для этого типа, если только Мсмконфигитемноннуллабле не включен в поле Attributes [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="14435-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="14435-110">Двоичный тип можно использовать со следующими видами Контекстдата.</span><span class="sxs-lookup"><span data-stu-id="14435-110">The Binary type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="14435-111">**Шорткутикон Контекстдата**</span><span class="sxs-lookup"><span data-stu-id="14435-111">**ShortcutIcon ContextData**</span></span>

<span data-ttu-id="14435-112">Настраиваемый модуль слияния может использовать этот тип, чтобы позволить пользователю предоставить внешний ключ для строки в [таблице значков](icon-table.md) , которая содержит изображение, подходящее для использования в качестве значка ярлыка.</span><span class="sxs-lookup"><span data-stu-id="14435-112">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the [Icon Table](icon-table.md) that contains an image suitable for use as a shortcut icon.</span></span> <span data-ttu-id="14435-113">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя настраиваемого элемента в столбец "имя", ввести "1" в столбец "формат", ввести "Icon" в столбец типа и ввести "Шоркутикон" в столбец Контекстдата таблицы Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="14435-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Icon" into the Type column, and enter "ShorcutIcon" into the ContextData column of the ModuleConfiguration table.</span></span> <span data-ttu-id="14435-114">Этот тип не подходит для использования в таблице пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14435-114">This type is not appropriate for use in a user interface table.</span></span> <span data-ttu-id="14435-115">Чтобы изменить ключ для таблицы значков в этих таблицах, см. значок Контекстдата в разделе [binary Type](binary-type.md).</span><span class="sxs-lookup"><span data-stu-id="14435-115">To modify a key to the Icon table in these tables see Icon ContextData under [Binary Type](binary-type.md).</span></span>

 

 



