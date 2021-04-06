---
description: Действие Инсталлексекутеагаин запускает скрипт, содержащий все операции в последовательности действий с момента запуска установки или последнего действия Инсталлексекутеагаин или последнего действия Инсталлексекуте.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Действие Инсталлексекутеагаин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991039"
---
# <a name="installexecuteagain-action"></a><span data-ttu-id="fc8cc-103">Действие Инсталлексекутеагаин</span><span class="sxs-lookup"><span data-stu-id="fc8cc-103">InstallExecuteAgain Action</span></span>

<span data-ttu-id="fc8cc-104">Действие Инсталлексекутеагаин запускает скрипт, содержащий все операции в последовательности действий с момента запуска установки или последнего действия Инсталлексекутеагаин или последнего [действия инсталлексекуте](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="fc8cc-104">The InstallExecuteAgain action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecuteAgain action or the last [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="fc8cc-105">Действие Инсталлексекуте обновляет систему, не завершая транзакцию.</span><span class="sxs-lookup"><span data-stu-id="fc8cc-105">The InstallExecute action updates the system without ending the transaction.</span></span> <span data-ttu-id="fc8cc-106">Инсталлексекутеагаин выполняет ту же операцию, что и [действие инсталлексекуте](installexecute-action.md) , но ее следует использовать только после инсталлексекуте.</span><span class="sxs-lookup"><span data-stu-id="fc8cc-106">InstallExecuteAgain performs the same operation as the [InstallExecute action](installexecute-action.md) but should only be used after InstallExecute.</span></span>

<span data-ttu-id="fc8cc-107">Инсталлексекутеагаин всегда должен быть установлен, чтобы он не выполнялся во время удаления.</span><span class="sxs-lookup"><span data-stu-id="fc8cc-107">InstallExecuteAgain should always be set so that it does not run during removal.</span></span> <span data-ttu-id="fc8cc-108">Дополнительные сведения см. [в разделе Использование свойств в условных инструкциях](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="fc8cc-108">For information, see [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fc8cc-109">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="fc8cc-109">Sequence Restrictions</span></span>

<span data-ttu-id="fc8cc-110">Действие Инсталлексекуте происходит между [действием инсталлинитиализе](installinitialize-action.md) и [действием функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="fc8cc-110">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fc8cc-111">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="fc8cc-111">ActionData Messages</span></span>

<span data-ttu-id="fc8cc-112">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="fc8cc-112">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc8cc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc8cc-113">Remarks</span></span>

<span data-ttu-id="fc8cc-114">Действие Инсталлексекутеагаин делает то же самое, что и [действие инсталлексекуте](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="fc8cc-114">The InstallExecuteAgain action does the same thing as the [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="fc8cc-115">Так как таблицы последовательности имеют только один первичный ключ — столбец Action, одно и то же действие не может повторяться в определенной таблице последовательностей.</span><span class="sxs-lookup"><span data-stu-id="fc8cc-115">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="fc8cc-116">Существуют два действия, которые выполняют одно и то же действие, Инсталлексекуте и Инсталлексекутеагаин, в случаях, когда функциональность Инсталлексекуте требуется дважды в [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="fc8cc-116">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="fc8cc-117">Дополнительные сведения см. в разделе [Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="fc8cc-117">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



