---
title: Флаг уведомления
description: Флаг уведомления
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- Флаг MCI_NOTIFY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412921"
---
# <a name="the-notify-flag"></a><span data-ttu-id="2d568-104">Флаг уведомления</span><span class="sxs-lookup"><span data-stu-id="2d568-104">The Notify Flag</span></span>

<span data-ttu-id="2d568-105">Флаг уведомления (MCI \_ Notify) направляет устройство на помещение сообщения [**мЦинотифи mm**](mm-mcinotify.md) , когда устройство завершает действие.</span><span class="sxs-lookup"><span data-stu-id="2d568-105">The "notify" (MCI\_NOTIFY) flag directs the device to post an [**MM MCINOTIFY**](mm-mcinotify.md) message when the device completes an action.</span></span> <span data-ttu-id="2d568-106">Приложение должно иметь процедуру окна для обработки сообщения мЦинотифи MM, \_ чтобы уведомление имело какое-либо воздействие.</span><span class="sxs-lookup"><span data-stu-id="2d568-106">Your application must have a window procedure to process the MM\_MCINOTIFY message for notification to have any effect.</span></span> <span data-ttu-id="2d568-107">\_Сообщение МЦИНОТИФИ mm указывает на то, что обработка команды завершена, но не указывает, была ли команда выполнена успешно, завершилась ошибкой или была заменена или отменена.</span><span class="sxs-lookup"><span data-stu-id="2d568-107">An MM\_MCINOTIFY message indicates that the processing of a command has completed, but it does not indicate whether the command was completed successfully, failed, or was superseded or aborted.</span></span>

<span data-ttu-id="2d568-108">Приложение задает маркер для окна назначения для сообщения, когда оно выдает команду.</span><span class="sxs-lookup"><span data-stu-id="2d568-108">The application specifies the handle to the destination window for the message when it issues a command.</span></span> <span data-ttu-id="2d568-109">В интерфейсе командной строки этот обработчик является последним параметром функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2d568-109">In the command-string interface, this handle is the last parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="2d568-110">В интерфейсе командного сообщения этот маркер указывается в младшем слове элемента **двкаллбакк** структуры, отправленном с помощью командного сообщения.</span><span class="sxs-lookup"><span data-stu-id="2d568-110">In the command-message interface, the handle is specified in the low-order word of the **dwCallBack** member of the structure sent with the command message.</span></span> <span data-ttu-id="2d568-111">(Каждая структура, связанная с командным сообщением, содержит этот элемент.)</span><span class="sxs-lookup"><span data-stu-id="2d568-111">(Every structure associated with a command message contains this member.)</span></span>

 

 