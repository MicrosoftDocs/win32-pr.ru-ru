---
description: DoAction таблице ControlEvent событие уведомляет установщик о необходимости выполнения настраиваемого действия. Это событие может быть опубликовано элементом управления "Кнопка", элементом управления CheckBox или элементом управления Селектионтри. Это событие должно быть создано в таблице таблице ControlEvent событие.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: DoAction таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143858"
---
# <a name="doaction-controlevent"></a><span data-ttu-id="5c5b3-105">DoAction таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="5c5b3-105">DoAction ControlEvent</span></span>

<span data-ttu-id="5c5b3-106">DoAction таблице ControlEvent событие уведомляет установщик о необходимости выполнения настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="5c5b3-106">The DoAction ControlEvent notifies the installer to execute a custom action.</span></span> <span data-ttu-id="5c5b3-107">Это событие может быть опубликовано элементом управления " [кнопка](pushbutton-control.md) ", элементом управления [CheckBox](checkbox-control.md) или элементом управления [селектионтри](selectiontree-control.md) .</span><span class="sxs-lookup"><span data-stu-id="5c5b3-107">This event can be published by a [PushButton](pushbutton-control.md) control, [CheckBox](checkbox-control.md) control, or a [SelectionTree](selectiontree-control.md) control.</span></span> <span data-ttu-id="5c5b3-108">Это событие должно быть создано в таблице [таблице ControlEvent событие](controlevent-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5c5b3-108">This event should be authored into the [ControlEvent](controlevent-table.md) table.</span></span>

<span data-ttu-id="5c5b3-109">Обратите внимание, что настраиваемые действия, запускаемые DoAction таблице ControlEvent событие, могут отправить сообщение с помощью [**метода Message**](session-message.md), но не могут отправить сообщение с помощью [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span><span class="sxs-lookup"><span data-stu-id="5c5b3-109">Note that custom actions launched by a DoAction ControlEvent can send a message with the [**Message Method**](session-message.md), but cannot send a message with [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="5c5b3-110">В системах до Windows Server 2003 настраиваемые действия, запускаемые DoAction таблице ControlEvent событие, не могут отправить сообщения с помощью метода **мсипроцессмессаже** или **Message**.</span><span class="sxs-lookup"><span data-stu-id="5c5b3-110">On systems prior to Windows Server 2003, custom actions launched by a DoAction ControlEvent cannot send messages with **MsiProcessMessage** or **Message Method**.</span></span> <span data-ttu-id="5c5b3-111">Дополнительные сведения см. [в разделе Отправка сообщений в установщик Windows с помощью мсипроцессмессаже](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="5c5b3-111">For more information, see [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="5c5b3-112">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5c5b3-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="5c5b3-113">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c5b3-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="5c5b3-114">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="5c5b3-114">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="5c5b3-115">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="5c5b3-115">Published By</span></span>

<span data-ttu-id="5c5b3-116">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="5c5b3-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="5c5b3-117">Аргумент</span><span class="sxs-lookup"><span data-stu-id="5c5b3-117">Argument</span></span>

<span data-ttu-id="5c5b3-118">Строка, имя настраиваемого действия, которое необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="5c5b3-118">A string, the name of the custom action to be executed.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="5c5b3-119">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="5c5b3-119">Action on Subscribers</span></span>

<span data-ttu-id="5c5b3-120">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="5c5b3-120">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="5c5b3-121">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="5c5b3-121">Typical Use</span></span>

<span data-ttu-id="5c5b3-122">Элемент управления " [кнопка](pushbutton-control.md) " в диалоговом окне связан с этим событием в таблице [таблице ControlEvent событие](controlevent-table.md) для вызова настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="5c5b3-122">A [PushButton](pushbutton-control.md) control on a dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to invoke a custom action.</span></span>

 

 



