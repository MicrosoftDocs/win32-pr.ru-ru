---
description: Удаление или отключение сеанса прекращает связь. Приложение может отправлять сведения о пользователе во время отключения, если поставщик услуг его поддерживает.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Drop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991003"
---
# <a name="drop"></a><span data-ttu-id="037fe-104">Drop</span><span class="sxs-lookup"><span data-stu-id="037fe-104">Drop</span></span>

<span data-ttu-id="037fe-105">Удаление или отключение сеанса прекращает связь.</span><span class="sxs-lookup"><span data-stu-id="037fe-105">Dropping or disconnecting a session terminates communication.</span></span> <span data-ttu-id="037fe-106">Приложение может отправлять сведения о пользователе во время отключения, если поставщик услуг его поддерживает.</span><span class="sxs-lookup"><span data-stu-id="037fe-106">The application has the option of sending user-user information at the time of the disconnect, if the service provider supports it.</span></span>

<span data-ttu-id="037fe-107">Обычными причинами для удаления сеанса является то, что пользователь запросил отключение или отбросил другой конец сеанса.</span><span class="sxs-lookup"><span data-stu-id="037fe-107">The usual reasons for dropping a session is a user has requested a disconnect or the other end of the session has dropped.</span></span> <span data-ttu-id="037fe-108">Операция DROP также может вызываться, когда TAPI предлагает сеанс приложения.</span><span class="sxs-lookup"><span data-stu-id="037fe-108">A drop operation may also be called when TAPI offers a session to the application.</span></span> <span data-ttu-id="037fe-109">Если поставщик услуг поддерживает это, то в результате приложение отклоняет вызов.</span><span class="sxs-lookup"><span data-stu-id="037fe-109">If the service provider supports this, the effect is that the application rejects the call.</span></span>

<span data-ttu-id="037fe-110">При вызове операции удаления связанные сеансы иногда также могут быть затронуты.</span><span class="sxs-lookup"><span data-stu-id="037fe-110">When invoking a drop operation, related sessions can sometimes be affected as well.</span></span> <span data-ttu-id="037fe-111">Например, удаление вызова конференции может удалить всех отдельных участников.</span><span class="sxs-lookup"><span data-stu-id="037fe-111">For example, dropping a conference call can drop all individual participants.</span></span> <span data-ttu-id="037fe-112">Сообщения об изменении состояния отправляются в приложение для всех вызовов, состояние которых затронуто.</span><span class="sxs-lookup"><span data-stu-id="037fe-112">State change messages are sent to the application for all calls whose state is affected.</span></span>

<span data-ttu-id="037fe-113">В различных конфигурациях с мостом или с поддержкой моста, когда в вызове несколько Сторон, операция Drop может не очистить вызов.</span><span class="sxs-lookup"><span data-stu-id="037fe-113">In various bridged or party-line configurations when multiple parties are on the call, a drop operation may not actually clear the call.</span></span> <span data-ttu-id="037fe-114">Например, в ситуации с мостом вызов не может быть удален, так как состояние других станций в вызове может управляться.</span><span class="sxs-lookup"><span data-stu-id="037fe-114">For example, in a bridged situation, the call may not be dropped because the status of other stations on the call may govern.</span></span> <span data-ttu-id="037fe-115">Вместо этого вызов можно просто изменить на неактивное состояние, когда оно останется подключенным к другим станциям.</span><span class="sxs-lookup"><span data-stu-id="037fe-115">Instead, the call may simply be changed to the inactive state while remaining connected at other stations.</span></span>

<span data-ttu-id="037fe-116">После операции DROP идентификатор сеанса и большинство ресурсов, связанных с сеансом, будут использоваться для большинства операций запроса.</span><span class="sxs-lookup"><span data-stu-id="037fe-116">Following a drop operation, the session identifier and most resources associated with the session will remain usable for most query operations.</span></span> <span data-ttu-id="037fe-117">Если приложению больше не требуются эти ресурсы, оно должно [завершить сеанс](terminate-a-session-ovr.md) , чтобы избежать утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="037fe-117">When an application no longer requires these resources, it must [terminate the session](terminate-a-session-ovr.md) in order to avoid memory leaks.</span></span>

<span data-ttu-id="037fe-118">**Интерфейс TAPI 2. x:** См. [**линедроп**](/windows/win32/api/tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="037fe-118">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span></span>

<span data-ttu-id="037fe-119">**Интерфейс TAPI 3. x:** См. раздел [**итбасиккаллконтрол::D соединения**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="037fe-119">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
