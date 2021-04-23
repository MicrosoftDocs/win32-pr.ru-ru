---
description: Настраиваемые действия Процессаккаунтс и Унинсталлаккаунтс создают отложенные настраиваемые действия для создания, удаления или отката учетных записей пользователей.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Создание таблицы Инсталлексекутесекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662933"
---
# <a name="authoring-the-installexecutesequence-table"></a><span data-ttu-id="46126-103">Создание таблицы Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="46126-103">Authoring the InstallExecuteSequence Table</span></span>

<span data-ttu-id="46126-104">Настраиваемые действия Процессаккаунтс и Унинсталлаккаунтс создают отложенные настраиваемые действия для создания, удаления или отката учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="46126-104">The custom actions ProcessAccounts and UninstallAccounts generate the deferred custom actions that create, remove, or rollback user accounts.</span></span> <span data-ttu-id="46126-105">Пользовательские действия Процессаккаунтс и Унинсталлаккаунтс должны быть указаны в [таблице инсталлексекутесекуенце](installexecutesequence-table.md) для выполнения.</span><span class="sxs-lookup"><span data-stu-id="46126-105">The custom actions ProcessAccounts and UninstallAccounts must be entered into the [InstallExecuteSequence table](installexecutesequence-table.md) to be executed.</span></span> <span data-ttu-id="46126-106">Добавьте следующие записи в [таблицу инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="46126-106">Add the following entries to the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="46126-107">Так как эти настраиваемые действия должны быть частью создания скрипта, оба настраиваемых действия должны быть упорядочены после [действия инсталлинитиализе](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="46126-107">Because these custom actions must be a part of the script generation, both custom actions must be sequenced after the [InstallInitialize action](installinitialize-action.md).</span></span>

<span data-ttu-id="46126-108">Условие в Процессаккаунтс гарантирует следующее.</span><span class="sxs-lookup"><span data-stu-id="46126-108">The condition on ProcessAccounts ensures the following.</span></span> <span data-ttu-id="46126-109">См. раздел [Синтаксис условных инструкций](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="46126-109">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

-   <span data-ttu-id="46126-110">Процессаккаунтс выполняется только в том случае, если компонент Тестаккаунт устанавливается локально на компьютере.</span><span class="sxs-lookup"><span data-stu-id="46126-110">ProcessAccounts runs only if the component TestAccount is being installed locally on the computer.</span></span>
-   <span data-ttu-id="46126-111">Тестовая учетная запись компонента в настоящее время не установлена или установлена для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="46126-111">The component Test Account is currently not installed or is installed to run from the source.</span></span>

<span data-ttu-id="46126-112">Условие в Унинсталлаккаунт гарантирует следующее:</span><span class="sxs-lookup"><span data-stu-id="46126-112">The condition on UninstallAccount ensures the following:</span></span>

-   <span data-ttu-id="46126-113">Унинсталлаккаунтс выполняется только в том случае, если компонент Тестаккаунт установлен локально на компьютере.</span><span class="sxs-lookup"><span data-stu-id="46126-113">UninstallAccounts runs only if the component TestAccount is installed locally on the computer.</span></span>
-   <span data-ttu-id="46126-114">Учетная запись тестирования компонента удаляется или устанавливается для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="46126-114">The component Test Account is being removed or being installed to run from the source.</span></span>

[<span data-ttu-id="46126-115">Таблица Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="46126-115">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="46126-116">Действие</span><span class="sxs-lookup"><span data-stu-id="46126-116">Action</span></span>            | <span data-ttu-id="46126-117">Условие</span><span class="sxs-lookup"><span data-stu-id="46126-117">Condition</span></span>                                                           | <span data-ttu-id="46126-118">Последовательность</span><span class="sxs-lookup"><span data-stu-id="46126-118">Sequence</span></span> |
|-------------------|---------------------------------------------------------------------|----------|
| <span data-ttu-id="46126-119">процессаккаунтс</span><span class="sxs-lookup"><span data-stu-id="46126-119">ProcessAccounts</span></span>   | <span data-ttu-id="46126-120">Версионнт и (? Тестаккаунт = 2 или? Тестаккаунт = 4) и $TestAccount = 3</span><span class="sxs-lookup"><span data-stu-id="46126-120">VersionNT AND (?TestAccount=2 OR ?TestAccount=4) AND $TestAccount=3</span></span> | <span data-ttu-id="46126-121">1550</span><span class="sxs-lookup"><span data-stu-id="46126-121">1550</span></span>     |
| <span data-ttu-id="46126-122">унинсталлаккаунтс</span><span class="sxs-lookup"><span data-stu-id="46126-122">UninstallAccounts</span></span> | <span data-ttu-id="46126-123">Версионнт и? Тестаккаунт = 3 и ($TestAccount = 4 или $TestAccount = 2)</span><span class="sxs-lookup"><span data-stu-id="46126-123">VersionNT AND ?TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2)</span></span> | <span data-ttu-id="46126-124">1560</span><span class="sxs-lookup"><span data-stu-id="46126-124">1560</span></span>     |



 

<span data-ttu-id="46126-125">Продолжайте [Создание пользовательского интерфейса для ввода пароля](authoring-the-user-interface-for-password-input.md).</span><span class="sxs-lookup"><span data-stu-id="46126-125">Continue to [Authoring the user interface for password input](authoring-the-user-interface-for-password-input.md).</span></span>

 

 



