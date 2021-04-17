---
description: Действие Вритерегистривалуес устанавливает сведения о реестре приложения.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Действие Вритерегистривалуес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673925"
---
# <a name="writeregistryvalues-action"></a><span data-ttu-id="564fe-103">Действие Вритерегистривалуес</span><span class="sxs-lookup"><span data-stu-id="564fe-103">WriteRegistryValues Action</span></span>

<span data-ttu-id="564fe-104">Действие Вритерегистривалуес устанавливает сведения о реестре приложения.</span><span class="sxs-lookup"><span data-stu-id="564fe-104">The WriteRegistryValues action sets up an application's registry information.</span></span> <span data-ttu-id="564fe-105">Сведения о реестре наследуется [таблицей Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="564fe-105">The registry information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="564fe-106">Значение реестра записывается в реестр, если соответствующий компонент настроен для установки локально или в качестве запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="564fe-106">A registry value is written to the registry if the corresponding component has been set to be installed either locally or as run from source.</span></span> <span data-ttu-id="564fe-107">Дополнительные сведения см. в разделе [Таблица реестра](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="564fe-107">For more information, see [Registry table](registry-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="564fe-108">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="564fe-108">Sequence Restrictions</span></span>

<span data-ttu-id="564fe-109">[Действие инсталлвалидате](installvalidate-action.md) должно следовать перед действием вритерегистривалуес.</span><span class="sxs-lookup"><span data-stu-id="564fe-109">The [InstallValidate action](installvalidate-action.md) must come before the WriteRegistryValues action.</span></span> <span data-ttu-id="564fe-110">Если имеется [действие ремоверегистривалуес](removeregistryvalues-action.md), оно должно предшествовать действию вритерегистривалуес.</span><span class="sxs-lookup"><span data-stu-id="564fe-110">If there is a [RemoveRegistryValues action](removeregistryvalues-action.md), then it must come before the WriteRegistryValues action.</span></span>

<span data-ttu-id="564fe-111">Пользовательское действие можно использовать для добавления строк в [таблицу реестра](registry-table.md) во время установки, удаления или восстановления транзакции.</span><span class="sxs-lookup"><span data-stu-id="564fe-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="564fe-112">Эти строки не сохраняются в таблице реестра, и эти данные доступны только во время текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="564fe-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="564fe-113">Поэтому пользовательское действие должно выполняться при каждой установке, удалении или исправлении транзакций, для которых требуется информация в этих дополнительных строках.</span><span class="sxs-lookup"><span data-stu-id="564fe-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="564fe-114">Пользовательское действие должно предшествовать действиям [ремоверегистривалуес](removeregistryvalues-action.md) и вритерегистривалуес в последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="564fe-114">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and WriteRegistryValues actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="564fe-115">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="564fe-115">ActionData Messages</span></span>



| <span data-ttu-id="564fe-116">Поле</span><span class="sxs-lookup"><span data-stu-id="564fe-116">Field</span></span> | <span data-ttu-id="564fe-117">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="564fe-117">Description of action data</span></span>                               |
|-------|----------------------------------------------------------|
| <span data-ttu-id="564fe-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="564fe-118">\[1\]</span></span> | <span data-ttu-id="564fe-119">Путь к разделу реестра значения, записанного в реестр.</span><span class="sxs-lookup"><span data-stu-id="564fe-119">Path to registry key of value written to registry.</span></span>       |
| <span data-ttu-id="564fe-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="564fe-120">\[2\]</span></span> | <span data-ttu-id="564fe-121">Форматированная текстовая строка имя значения, записанное в реестр.</span><span class="sxs-lookup"><span data-stu-id="564fe-121">Formatted text string name of value written to registry.</span></span> |
| <span data-ttu-id="564fe-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="564fe-122">\[3\]</span></span> | <span data-ttu-id="564fe-123">Форматированная текстовая строка значения, записанная в реестр.</span><span class="sxs-lookup"><span data-stu-id="564fe-123">Formatted text string of value written to registry.</span></span>      |



 

 

 



