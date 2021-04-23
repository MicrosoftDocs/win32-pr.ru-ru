---
description: Установщик Windows реализует ряд стандартных элементов управления, которые авторы пакетов могут размещать в диалоговых окнах. Однако не все стандартные элементы управления Microsoft Windows доступны, а пользовательские элементы управления не могут быть созданы для использования с пользовательским интерфейсом установщика.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Обзор элементов управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fbd8477416eb5a126eca56cb1050112309b0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664491"
---
# <a name="controls-overview"></a><span data-ttu-id="c8b8b-104">Обзор элементов управления</span><span class="sxs-lookup"><span data-stu-id="c8b8b-104">Controls Overview</span></span>

<span data-ttu-id="c8b8b-105">Установщик Windows реализует ряд стандартных элементов управления, которые авторы пакетов могут размещать в диалоговых окнах.</span><span class="sxs-lookup"><span data-stu-id="c8b8b-105">Windows Installer implements a number of standard controls that package authors can place onto dialog boxes.</span></span> <span data-ttu-id="c8b8b-106">Однако не все стандартные элементы управления Microsoft Windows доступны, а пользовательские элементы управления не могут быть созданы для использования с пользовательским интерфейсом установщика.</span><span class="sxs-lookup"><span data-stu-id="c8b8b-106">However, not all standard Microsoft Windows controls are available, and custom controls cannot be created for use with the installer UI.</span></span>

<span data-ttu-id="c8b8b-107">Элементы управления создаются в диалоговых окнах установщика аналогично созданию диалоговых окон программным способом с помощью API интерфейса пользователя Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c8b8b-107">Controls are created on dialog boxes in the installer in a manner similar to how dialog boxes are created programmatically using the Microsoft Windows user interface API.</span></span> <span data-ttu-id="c8b8b-108">Элемент управления создается на основе шаблона, записанного в таблице элементов управления.</span><span class="sxs-lookup"><span data-stu-id="c8b8b-108">A control is created from a template recorded in the Control table.</span></span> <span data-ttu-id="c8b8b-109">Этот шаблон немного отличается тем, что он содержит уникальное имя диалогового окна, в котором отображается элемент управления.</span><span class="sxs-lookup"><span data-stu-id="c8b8b-109">This template is slightly different in that it contains the unique name of the dialog box on which the control appears.</span></span>

<span data-ttu-id="c8b8b-110">В API пользовательского интерфейса Microsoft Windows взаимодействие с пользователем осуществляется путем создания функции обратного вызова для работы с сообщениями, размещенными элементом управления.</span><span class="sxs-lookup"><span data-stu-id="c8b8b-110">In the Microsoft Windows user interface API, user interaction is accomplished by creating a callback function to handle messages posted by the control.</span></span> <span data-ttu-id="c8b8b-111">Кроме того, большинство элементов управления Microsoft Windows получают сообщения, например, отправленные функцией [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="c8b8b-111">Also, most Microsoft Windows controls receive messages, such as those sent by the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="c8b8b-112">Взаимодействие между пользователем и элементами управления осуществляется в установщике с помощью [контролевентс](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c8b8b-112">Communication between the user and controls is accomplished in the installer through the use of [ControlEvents](controlevent-overview.md).</span></span> <span data-ttu-id="c8b8b-113">Однако существует ограниченный набор Контролевентс, характерный для каждого элемента управления в ограниченном наборе элементов управления в установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="c8b8b-113">However, there is a limited set of ControlEvents that are specific to each control in the limited set of controls in Windows Installer.</span></span> <span data-ttu-id="c8b8b-114">Элементы управления могут отправлять более одного таблице ControlEvent событие и могут получить несколько таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="c8b8b-114">Controls may post more than one ControlEvent and may receive more than one ControlEvent.</span></span>

<span data-ttu-id="c8b8b-115">Элементы управления могут публиковать определенные Контролевентс с помощью таблицы таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="c8b8b-115">Controls can publish specific ControlEvents through the use of the ControlEvent table.</span></span> <span data-ttu-id="c8b8b-116">Элементы управления могут получить Контролевентс с помощью [таблицы таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8b8b-116">Controls can receive ControlEvents through the use of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="c8b8b-117">Установщик Windows публикует Контролевентс во время выполнения некоторых действий, а элементы управления, подписанные на эти Контролевентс в таблице таблица eventmapping, получают их.</span><span class="sxs-lookup"><span data-stu-id="c8b8b-117">Windows Installer publishes ControlEvents during the execution of some actions as well, and controls subscribed to these ControlEvents in the EventMapping table receive them.</span></span>

 

 
