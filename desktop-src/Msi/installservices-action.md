---
description: Действие Инсталлсервицес регистрирует службу для системы. Это действие запрашивает таблицу Сервицеинсталл.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Действие Инсталлсервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684355"
---
# <a name="installservices-action"></a><span data-ttu-id="d9bdb-104">Действие Инсталлсервицес</span><span class="sxs-lookup"><span data-stu-id="d9bdb-104">InstallServices Action</span></span>

<span data-ttu-id="d9bdb-105">Действие Инсталлсервицес регистрирует службу для системы.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-105">The InstallServices action registers a service for the system.</span></span> <span data-ttu-id="d9bdb-106">Это действие запрашивает [таблицу сервицеинсталл](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="d9bdb-106">This action queries the [ServiceInstall table](serviceinstall-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d9bdb-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="d9bdb-107">Sequence Restrictions</span></span>

<span data-ttu-id="d9bdb-108">Действие служб должно использоваться в следующей последовательности.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-108">The services action must be used in the following sequence.</span></span>

[<span data-ttu-id="d9bdb-109">стопсервицес</span><span class="sxs-lookup"><span data-stu-id="d9bdb-109">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="d9bdb-110">делетесервицес</span><span class="sxs-lookup"><span data-stu-id="d9bdb-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="d9bdb-111">Любое из следующих действий: [инсталлфилес](installfiles-action.md), [ремовефилес](removefiles-action.md), [дупликатефилес](duplicatefiles-action.md), [мовефилес](movefiles-action.md), [патчфилес](patchfiles-action.md)и [ремоведупликатефилес](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d9bdb-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

<span data-ttu-id="d9bdb-112">инсталлсервицес</span><span class="sxs-lookup"><span data-stu-id="d9bdb-112">InstallServices</span></span>

[<span data-ttu-id="d9bdb-113">стартсервицес</span><span class="sxs-lookup"><span data-stu-id="d9bdb-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="d9bdb-114">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="d9bdb-114">ActionData Messages</span></span>

<span data-ttu-id="d9bdb-115">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-115">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9bdb-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9bdb-116">Remarks</span></span>

<span data-ttu-id="d9bdb-117">Для выполнения этого действия пользователь должен быть администратором или обладать повышенными привилегиями с разрешением на установку служб или на то, что приложение является частью управляемой установки.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-117">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



