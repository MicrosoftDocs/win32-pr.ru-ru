---
title: Как работают уведомления
description: Как работают уведомления
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413861"
---
# <a name="how-notifications-work"></a><span data-ttu-id="13e6b-103">Как работают уведомления</span><span class="sxs-lookup"><span data-stu-id="13e6b-103">How Notifications Work</span></span>

<span data-ttu-id="13e6b-104">Уведомления создаются в приложении Object и передаются в контейнер с помощью обработчика объектов.</span><span class="sxs-lookup"><span data-stu-id="13e6b-104">Notifications originate in the object application and flow to the container by way of the object handler.</span></span> <span data-ttu-id="13e6b-105">Если объект является связанным объектом, связанный объект перехватывает уведомления от обработчика объектов и уведомляет контейнер напрямую.</span><span class="sxs-lookup"><span data-stu-id="13e6b-105">If the object is a linked object, the linked object intercepts the notifications from the object handler and notifies the container directly.</span></span>

<span data-ttu-id="13e6b-106">Приложение объекта должно управлять запросами на регистрацию, следить за тем, куда отправлять уведомления и отправлять эти уведомления, когда это необходимо.</span><span class="sxs-lookup"><span data-stu-id="13e6b-106">An object application must manage registration requests, keeping track of where to send which notifications and sending those notifications when appropriate.</span></span> <span data-ttu-id="13e6b-107">OLE предоставляет два объекта компонентов для упрощения этой задачи: Олеадвисехолдер для уведомлений составного документа и Датаадвисехолдер для уведомлений об изменении данных.</span><span class="sxs-lookup"><span data-stu-id="13e6b-107">OLE provides two component objects to simplify this task: the OleAdviseHolder for compound document notifications and the DataAdviseHolder for data notifications.</span></span>

<span data-ttu-id="13e6b-108">Приложения объектов определяют условия, которые запрашивают отправку каждого конкретного уведомления, и частоту отправки каждого уведомления.</span><span class="sxs-lookup"><span data-stu-id="13e6b-108">Object applications determine the conditions that prompt the sending of each specific notification and the frequency with which each notification should be sent.</span></span> <span data-ttu-id="13e6b-109">Если нужно отправить несколько уведомлений, не имеет значения, какое уведомление отправляется первыми. их можно отправить в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="13e6b-109">When it is appropriate for multiple notifications to be sent, it does not matter which notification is sent first; they can be sent in any order.</span></span>

<span data-ttu-id="13e6b-110">Время уведомлений влияет на производительность и координацию между приложением объекта и его контейнерами.</span><span class="sxs-lookup"><span data-stu-id="13e6b-110">The timing of notifications affects the performance and coordination between an object application and its containers.</span></span> <span data-ttu-id="13e6b-111">В то время как уведомления отправляются слишком часто, это приводит к слишком редкому получению уведомлений из-за несинхронизированного контейнера.</span><span class="sxs-lookup"><span data-stu-id="13e6b-111">Whereas notifications sent too frequently slow processing, notifications sent too infrequently result in an out-of-sync container.</span></span> <span data-ttu-id="13e6b-112">Частоту уведомлений можно сравнивать с частотой, с которой приложение перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="13e6b-112">Notification frequency can be compared with the rate at which an application repaints.</span></span> <span data-ttu-id="13e6b-113">Поэтому разумно использовать аналогичную логику для синхронизации уведомлений (как используется для перерисовки).</span><span class="sxs-lookup"><span data-stu-id="13e6b-113">Therefore, using similar logic for the timing of notifications (as is used for repainting) is wise.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13e6b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="13e6b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13e6b-115">**креатедатаадвисехолдер**</span><span class="sxs-lookup"><span data-stu-id="13e6b-115">**CreateDataAdviseHolder**</span></span>](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[<span data-ttu-id="13e6b-116">**креатеолеадвисехолдер**</span><span class="sxs-lookup"><span data-stu-id="13e6b-116">**CreateOleAdviseHolder**</span></span>](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[<span data-ttu-id="13e6b-117">Уведомления</span><span class="sxs-lookup"><span data-stu-id="13e6b-117">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 