---
description: Действие функции InstallFinalize запускает скрипт, содержащий все операции в последовательности действий с момента запуска установки или выполнения действий Инсталлексекуте или Инсталлексекутеагаин.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Действие функции InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96296c2241f5769296b7192ce89ab9f44364bb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811290"
---
# <a name="installfinalize-action"></a><span data-ttu-id="7799d-103">Действие функции InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="7799d-103">InstallFinalize Action</span></span>

<span data-ttu-id="7799d-104">Действие функции InstallFinalize запускает скрипт, содержащий все операции в последовательности действий с момента запуска установки или выполнения действий [инсталлексекуте](installexecute-action.md) или [инсталлексекутеагаин](installexecuteagain-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7799d-104">The InstallFinalize action runs a script that contains all operations in the action sequence since either the start of the installation or the execution of the [InstallExecute](installexecute-action.md) or [InstallExecuteAgain](installexecuteagain-action.md) actions.</span></span> <span data-ttu-id="7799d-105">Это действие отмечает конец транзакции, который начинается с действия [инсталлинитиализе](installinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7799d-105">This action marks the end of a transaction that begins with the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7799d-106">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="7799d-106">Sequence Restrictions</span></span>

<span data-ttu-id="7799d-107">Действие [инсталлинитиализе](installinitialize-action.md) должно следовать перед действием функции InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="7799d-107">The [InstallInitialize](installinitialize-action.md) action must come before the InstallFinalize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7799d-108">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="7799d-108">ActionData Messages</span></span>

<span data-ttu-id="7799d-109">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="7799d-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="7799d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7799d-110">Remarks</span></span>

<span data-ttu-id="7799d-111">Если обнаруживается, что продукт помечен для полного удаления, операции автоматически добавляются в сценарий, чтобы удалить компонент **Установка и удаление программ** на **панели управления** для продукта, отменить регистрацию и отмену публикации продукта, а также удалить кэшированную локальную базу данных из% Windows%, если она существует.</span><span class="sxs-lookup"><span data-stu-id="7799d-111">If it is detected that the product is marked for complete removal, operations are automatically added to the script to remove the **Add/Remove Programs** in the **Control Panel** information for the product, to unregister and unpublish the product, and to remove the cached local database from %WINDOWS%, if it exists.</span></span>

<span data-ttu-id="7799d-112">Системные изменения, внесенные до выполнения действия, не могут быть восстановлены после завершения действия функции InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="7799d-112">System changes made before the action may not be restored after the InstallFinalize action is executed.</span></span> <span data-ttu-id="7799d-113">Действие функции InstallFinalize обновляет систему, используя все операции, определенные в этой точке, а затем завершает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="7799d-113">The InstallFinalize action updates the system with all operations determined to that point and then ends the transaction.</span></span>

 

 



