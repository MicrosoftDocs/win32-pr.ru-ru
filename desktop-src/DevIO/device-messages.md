---
description: Сообщения устройства являются системными сообщениями, которые уведомляют приложения и другие функции событий изменения устройства.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Сообщения устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655979"
---
# <a name="device-messages"></a><span data-ttu-id="f9d41-103">Сообщения устройства</span><span class="sxs-lookup"><span data-stu-id="f9d41-103">Device Messages</span></span>

<span data-ttu-id="f9d41-104">Сообщения устройства являются системными сообщениями, которые уведомляют приложения и другие функции событий изменения устройства.</span><span class="sxs-lookup"><span data-stu-id="f9d41-104">Device messages are system messages that notify applications and other features of device change events.</span></span> <span data-ttu-id="f9d41-105">Эти события возникают каждый раз, когда система обнаруживает изменение оборудования системы, например, когда пользователь закрепляет и открепляет портативный компьютер или вставляет или удаляет устройство, например адаптер PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="f9d41-105">These events occur whenever the system detects a change to the system hardware, such as when the user docks and undocks a laptop computer, or inserts or removes a device such as a PCMCIA card.</span></span> <span data-ttu-id="f9d41-106">События устройств могут возникать во время работы системы или при возобновлении работы системы после временной приостановки.</span><span class="sxs-lookup"><span data-stu-id="f9d41-106">Device events can occur while the system is running or when the system resumes operation after temporarily being suspended.</span></span>

<span data-ttu-id="f9d41-107">Чтобы гарантировать, что приложения не теряют данные, когда устройства становятся недоступными, система отслеживает конфигурацию оборудования и отправляет сообщения в приложения, чтобы уведомить их об изменениях и предоставить им возможность подготовиться к изменениям до их появления.</span><span class="sxs-lookup"><span data-stu-id="f9d41-107">To help ensure that applications do not lose data when devices become unavailable, the system monitors the hardware configuration and sends device messages to the applications to notify them of the changes and to give them the opportunity to prepare for the changes before they occur.</span></span>

<span data-ttu-id="f9d41-108">Для каждого события устройства система передает сообщение [**WM \_ девицечанже**](wm-devicechange.md) всем приложениям.</span><span class="sxs-lookup"><span data-stu-id="f9d41-108">For each device event, the system broadcasts a [**WM\_DEVICECHANGE**](wm-devicechange.md) message to all applications.</span></span> <span data-ttu-id="f9d41-109">В этом сообщении параметр *wParam* определяет [Тип события устройства](device-event-types.md) , а параметр *lParam* — указатель на данные, относящиеся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="f9d41-109">In this message, the *wParam* parameter identifies the [device event type](device-event-types.md) and the *lParam* parameter is a pointer to event-specific data.</span></span>

 

 



