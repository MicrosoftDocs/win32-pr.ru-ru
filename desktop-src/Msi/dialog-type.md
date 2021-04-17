---
description: Тип диалогового окна семантического типа является одним из типов формата ключа. Этот тип состоит из внешнего ключа в диалоговую таблицу, предоставленную пользователем.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Тип диалога
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663706"
---
# <a name="dialog-type"></a><span data-ttu-id="7aabf-104">Тип диалога</span><span class="sxs-lookup"><span data-stu-id="7aabf-104">Dialog Type</span></span>

<span data-ttu-id="7aabf-105">Тип диалогового окна [семантического типа](semantic-types.md) является одним из [типов формата ключа](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="7aabf-105">The Dialog Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="7aabf-106">Этот тип состоит из внешнего ключа в [диалоговую таблицу](dialog-table.md) , предоставленную пользователем.</span><span class="sxs-lookup"><span data-stu-id="7aabf-106">This type consists of a foreign key into the [Dialog table](dialog-table.md) provided by the user.</span></span>

<span data-ttu-id="7aabf-107">Средство слияния должно заменить допустимый [идентификатор](identifier.md) установщик Windows для элементов этого типа.</span><span class="sxs-lookup"><span data-stu-id="7aabf-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="7aabf-108">Mergemod.dll не применяет это ограничение и является средством слияния, чтобы убедиться, что пользователь предоставляет допустимый ключ в таблице диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="7aabf-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Dialog table.</span></span>

<span data-ttu-id="7aabf-109">Значение null является допустимым для этого типа, если только Мсмконфигитемноннуллабле не включен в поле Attributes [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="7aabf-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="7aabf-110">Тип диалогового окна можно использовать со следующими видами Контекстдата.</span><span class="sxs-lookup"><span data-stu-id="7aabf-110">The Dialog type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="7aabf-111">**Диалогнекст Контекстдата**</span><span class="sxs-lookup"><span data-stu-id="7aabf-111">**DialogNext ContextData**</span></span>

<span data-ttu-id="7aabf-112">Настраиваемый модуль слияния может использовать этот тип, чтобы позволить пользователю предоставить внешний ключ в таблице диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="7aabf-112">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="7aabf-113">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя настраиваемого элемента в столбец "имя", ввести "1" в столбец "формат", ввести "Dialog" в столбец Type и ввести "Диалогнекст" в столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="7aabf-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogNext" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="7aabf-114">**Диалогпрев Контекстдата**</span><span class="sxs-lookup"><span data-stu-id="7aabf-114">**DialogPrev ContextData**</span></span>

<span data-ttu-id="7aabf-115">Настраиваемый модуль слияния может использовать этот тип, чтобы позволить пользователю предоставить внешний ключ в таблице диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="7aabf-115">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="7aabf-116">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя настраиваемого элемента в столбец "имя", ввести "1" в столбец "формат", ввести "Dialog" в столбец Type и ввести "Диалогпрев" в столбец Контекстдата таблицы Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="7aabf-116">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogPrev" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



