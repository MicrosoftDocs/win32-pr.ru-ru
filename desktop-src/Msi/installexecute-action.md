---
description: Действие Инсталлексекуте запускает скрипт, содержащий все операции в последовательности действий с момента запуска установки или последнего действия Инсталлексекуте или Инсталлексекутеагаин.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Действие Инсталлексекуте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143846"
---
# <a name="installexecute-action"></a><span data-ttu-id="72c64-103">Действие Инсталлексекуте</span><span class="sxs-lookup"><span data-stu-id="72c64-103">InstallExecute Action</span></span>

<span data-ttu-id="72c64-104">Действие Инсталлексекуте запускает скрипт, содержащий все операции в последовательности действий с момента запуска установки или последнего действия Инсталлексекуте или [инсталлексекутеагаин](installexecuteagain-action.md).</span><span class="sxs-lookup"><span data-stu-id="72c64-104">The InstallExecute action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecute action or [InstallExecuteAgain action](installexecuteagain-action.md).</span></span> <span data-ttu-id="72c64-105">Действие Инсталлексекуте обновляет систему, не завершая транзакцию.</span><span class="sxs-lookup"><span data-stu-id="72c64-105">The InstallExecute action updates the system without ending the transaction.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="72c64-106">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="72c64-106">Sequence Restrictions</span></span>

<span data-ttu-id="72c64-107">Действие Инсталлексекуте происходит между [действием инсталлинитиализе](installinitialize-action.md) и [действием функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="72c64-107">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="72c64-108">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="72c64-108">ActionData Messages</span></span>

<span data-ttu-id="72c64-109">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="72c64-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="72c64-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72c64-110">Remarks</span></span>

<span data-ttu-id="72c64-111">[Действие инсталлексекутеагаин](installexecuteagain-action.md) делает то же самое, что и действие инсталлексекуте.</span><span class="sxs-lookup"><span data-stu-id="72c64-111">The [InstallExecuteAgain action](installexecuteagain-action.md) does the same thing as the InstallExecute action.</span></span> <span data-ttu-id="72c64-112">Так как таблицы последовательности имеют только один первичный ключ — столбец Action, одно и то же действие не может повторяться в определенной таблице последовательностей.</span><span class="sxs-lookup"><span data-stu-id="72c64-112">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="72c64-113">Существуют два действия, которые выполняют одно и то же действие, Инсталлексекуте и Инсталлексекутеагаин, в случаях, когда функциональность Инсталлексекуте требуется дважды в [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="72c64-113">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="72c64-114">Дополнительные сведения см. в разделе [Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="72c64-114">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



