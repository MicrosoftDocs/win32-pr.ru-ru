---
description: Установщик Windows обрабатывает пользовательские действия в виде отдельного потока из основной установки.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Синхронные и асинхронные настраиваемые действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673434"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a><span data-ttu-id="f3bd0-103">Синхронные и асинхронные настраиваемые действия</span><span class="sxs-lookup"><span data-stu-id="f3bd0-103">Synchronous and Asynchronous Custom Actions</span></span>

<span data-ttu-id="f3bd0-104">Установщик Windows обрабатывает пользовательские действия в виде отдельного потока из основной установки.</span><span class="sxs-lookup"><span data-stu-id="f3bd0-104">The Windows Installer processes custom actions as a separate thread from the main installation.</span></span> <span data-ttu-id="f3bd0-105">Во время синхронного выполнения настраиваемого действия установщик ожидает завершения потока настраиваемого действия, прежде чем продолжить основную установку.</span><span class="sxs-lookup"><span data-stu-id="f3bd0-105">During synchronous execution of a custom action, the installer waits for the thread of the custom action to complete before continuing the main installation.</span></span> <span data-ttu-id="f3bd0-106">Во время асинхронного выполнения установщик выполняет настраиваемое действие одновременно с тем, как текущая установка продолжится.</span><span class="sxs-lookup"><span data-stu-id="f3bd0-106">During asynchronous execution, the installer runs the custom action simultaneously as the current installation continues.</span></span> <span data-ttu-id="f3bd0-107">Таким образом, авторы пользовательских действий должны знать о любых асинхронных потоках, которые могут вносить изменения в базу данных установки между вызовами функций.</span><span class="sxs-lookup"><span data-stu-id="f3bd0-107">Authors of custom actions must therefore be aware of any asynchronous threads that may be making changes to the installation database between function calls.</span></span>

<span data-ttu-id="f3bd0-108">В частности, в асинхронных настраиваемых действиях следует избегать вызовов [**мсижеттаржетпас**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) и [**мсисеттаржетпас**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) .</span><span class="sxs-lookup"><span data-stu-id="f3bd0-108">In particular, calls to [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) and [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) should be avoided in asynchronous custom actions.</span></span> <span data-ttu-id="f3bd0-109">Вместо этого используйте [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) для получения целевого пути.</span><span class="sxs-lookup"><span data-stu-id="f3bd0-109">Instead use [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) to obtain a target path.</span></span> <span data-ttu-id="f3bd0-110">Операции с массовыми базами данных, такие как операции импорта, экспорта и преобразования, следует избегать в любом типе настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="f3bd0-110">Bulk database operations such as import, export, and transform operations should be avoided in any type of custom action.</span></span>

<span data-ttu-id="f3bd0-111">Флаги параметров можно задать в поле Тип [таблицы CustomAction](customaction-table.md) , чтобы указать, что основные и пользовательские потоки действий выполняются синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f3bd0-111">Option flags can be set in the Type field of the [CustomAction table](customaction-table.md) to specify that the main and custom action threads run synchronously or asynchronously.</span></span> <span data-ttu-id="f3bd0-112">См. раздел [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="f3bd0-112">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="f3bd0-113">Установщик может выполнять только [пользовательские действия отката](rollback-custom-actions.md) и [параллельные действия установки](concurrent-installations.md) в качестве синхронных настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="f3bd0-113">The installer can only execute [Rollback Custom Actions](rollback-custom-actions.md) and [Concurrent Installation](concurrent-installations.md) actions as synchronous custom actions.</span></span>

 

 



