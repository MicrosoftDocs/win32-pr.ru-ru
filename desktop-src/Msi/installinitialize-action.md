---
description: Действие Инсталлинитиализе и функции InstallFinalize отмечают начало и конец последовательности действий, которые изменяют систему.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Действие Инсталлинитиализе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810301"
---
# <a name="installinitialize-action"></a><span data-ttu-id="10fce-103">Действие Инсталлинитиализе</span><span class="sxs-lookup"><span data-stu-id="10fce-103">InstallInitialize Action</span></span>

<span data-ttu-id="10fce-104">Действие Инсталлинитиализе и [функции InstallFinalize](installfinalize-action.md) отмечают начало и конец последовательности действий, которые изменяют систему.</span><span class="sxs-lookup"><span data-stu-id="10fce-104">The InstallInitialize action and [InstallFinalize](installfinalize-action.md) action mark the beginning and end of a sequence of actions that change the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="10fce-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="10fce-105">Sequence Restrictions</span></span>

<span data-ttu-id="10fce-106">Действие Инсталлинитиализе должно быть упорядочено до любых действий, изменяющих систему, таких как действие [инсталлфилес](installfiles-action.md) , действие [Вритерегистривалуес](writeregistryvalues-action.md) , действие [селфрегмодулес](selfregmodules-action.md) и действие [процесскомпонентс](processcomponents-action.md) .</span><span class="sxs-lookup"><span data-stu-id="10fce-106">The InstallInitialize action must be sequenced before any actions that change the system, such as the [InstallFiles](installfiles-action.md) action, the [WriteRegistryValues](writeregistryvalues-action.md) action, the [SelfRegModules](selfregmodules-action.md) action, and the [ProcessComponents](processcomponents-action.md) action.</span></span> <span data-ttu-id="10fce-107">Следовательно, действие Инсталлинитиализе должно быть упорядочено до действия [функции InstallFinalize](installfinalize-action.md) и действия [инсталлексекуте](installexecute-action.md) .</span><span class="sxs-lookup"><span data-stu-id="10fce-107">The InstallInitialize action must therefore be sequenced before the [InstallFinalize](installfinalize-action.md) action and the [InstallExecute](installexecute-action.md) action.</span></span>

<span data-ttu-id="10fce-108">[Настраиваемые действия](custom-actions.md) , изменяющие пакет установщик Windows, например добавление строк в таблицу, обрабатывающую устанавливаемые ресурсы, такие как таблица [реестра](registry-table.md) или таблица [дупликатефиле](duplicatefile-table.md) , должны быть упорядочены перед действием инсталлинитиализе.</span><span class="sxs-lookup"><span data-stu-id="10fce-108">[Custom actions](custom-actions.md) that modify the Windows Installer package, for example by adding rows to a table that handles installable resources, such as the [Registry](registry-table.md) table or [DuplicateFile](duplicatefile-table.md) table, must be sequenced before InstallInitialize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="10fce-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="10fce-109">ActionData Messages</span></span>

<span data-ttu-id="10fce-110">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="10fce-110">There are no ActionData messages.</span></span>

 

 



