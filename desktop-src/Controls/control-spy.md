---
title: Управление Spy v 2.0
description: Управление Spy — это средство, помогающее разработчикам понять общие элементы управления, как применять к ним стили и как они реагируют на сообщения и уведомления.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104070788"
---
# <a name="control-spy-v20"></a><span data-ttu-id="7bc63-103">Управление Spy v 2.0</span><span class="sxs-lookup"><span data-stu-id="7bc63-103">Control Spy v2.0</span></span>

<span data-ttu-id="7bc63-104">Управление Spy — это средство, помогающее разработчикам понять общие элементы управления: как применять стили к ним и как они реагируют на сообщения и уведомления.</span><span class="sxs-lookup"><span data-stu-id="7bc63-104">Control Spy is a tool that helps developers understand common controls: how to apply styles to them, and how they respond to messages and notifications.</span></span> <span data-ttu-id="7bc63-105">С помощью элемента управления Spy можно сразу же увидеть, как различные стили влияют на поведение и внешний вид каждого элемента управления, а также как можно изменить состояние каждого элемента управления, отправив сообщения.</span><span class="sxs-lookup"><span data-stu-id="7bc63-105">Using Control Spy, you can immediately see how different styles affect the behavior and appearance of each control, and also how you can change the state of each control by sending messages.</span></span>

<span data-ttu-id="7bc63-106">Доступны две версии элемента управления Spy, одна для [Comctl32.dll версии 5. x](common-control-versions.md) , а другая для Comctl32.dll версии 6,0 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="7bc63-106">Two versions of Control Spy are available, one for [Comctl32.dll version 5.x](common-control-versions.md) and one for Comctl32.dll version 6.0 and later.</span></span> <span data-ttu-id="7bc63-107">ControlSpyV6.exe имеет встроенный манифест приложения, который использует более новые тематические элементы управления.</span><span class="sxs-lookup"><span data-stu-id="7bc63-107">ControlSpyV6.exe has a built-in application manifest so that it uses the newer, themed controls.</span></span> <span data-ttu-id="7bc63-108">ControlSpyV5.exe не имеет этого манифеста, поэтому по умолчанию используется старая версия.</span><span class="sxs-lookup"><span data-stu-id="7bc63-108">ControlSpyV5.exe does not have this manifest and so defaults to the older version.</span></span>

<span data-ttu-id="7bc63-109">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="7bc63-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7bc63-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="7bc63-110">Overview</span></span>](#overview)
-   [<span data-ttu-id="7bc63-111">Стили</span><span class="sxs-lookup"><span data-stu-id="7bc63-111">Styles</span></span>](#styles)
-   [<span data-ttu-id="7bc63-112">Сообщения</span><span class="sxs-lookup"><span data-stu-id="7bc63-112">Messages</span></span>](#messages)
-   [<span data-ttu-id="7bc63-113">Размер и цвет</span><span class="sxs-lookup"><span data-stu-id="7bc63-113">Size/Color</span></span>](#sizecolor)
-   [<span data-ttu-id="7bc63-114">Где получить управление Spy</span><span class="sxs-lookup"><span data-stu-id="7bc63-114">Where to Get Control Spy</span></span>](#where-to-get-control-spy)
-   [<span data-ttu-id="7bc63-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7bc63-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="7bc63-116">Обзор</span><span class="sxs-lookup"><span data-stu-id="7bc63-116">Overview</span></span>

<span data-ttu-id="7bc63-117">Управление Spy размещает выбранный общий элемент управления в центре окна приложения.</span><span class="sxs-lookup"><span data-stu-id="7bc63-117">Control Spy hosts a selected common control in the center of its application window.</span></span> <span data-ttu-id="7bc63-118">Чтобы изменить отображаемый элемент управления, выберите другие элементы управления в списке в левой части окна.</span><span class="sxs-lookup"><span data-stu-id="7bc63-118">You can change which control is shown by selecting different controls from the list box at the left side of the window.</span></span> <span data-ttu-id="7bc63-119">Сообщения или уведомления, полученные элементом управления, будут перечислены в правой части окна по мере их прибытия.</span><span class="sxs-lookup"><span data-stu-id="7bc63-119">Messages or notifications received by the control will be listed at the right side of the window as they arrive.</span></span> <span data-ttu-id="7bc63-120">Вы можете включить или отключить эту функцию, используя флажки **полученные сообщения** и **уведомления** .</span><span class="sxs-lookup"><span data-stu-id="7bc63-120">You can enable or disable this functionality by using the **Messages Received** and **Notifications Received** check boxes.</span></span>

<span data-ttu-id="7bc63-121">На следующем рисунке показано приложение Spy Control.</span><span class="sxs-lookup"><span data-stu-id="7bc63-121">The following image shows the Control Spy application.</span></span>

![Управление окном Spy](images/controlspy-main.png)

<span data-ttu-id="7bc63-123">В нижней части окна есть несколько вкладок, которые предоставляют больше функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="7bc63-123">At the bottom of the window, there are several tabs that present more functionality.</span></span>

## <a name="styles"></a><span data-ttu-id="7bc63-124">Стили</span><span class="sxs-lookup"><span data-stu-id="7bc63-124">Styles</span></span>

<span data-ttu-id="7bc63-125">Вкладка **стили** позволяет изменить текущий стиль окна элемента управления.</span><span class="sxs-lookup"><span data-stu-id="7bc63-125">The **Styles** tab enables you to change the current window style of the control.</span></span> <span data-ttu-id="7bc63-126">Выберите или отмените выбор любого из перечисленных стилей, а затем нажмите кнопку **Применить** , чтобы изменить стиль отображаемого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="7bc63-126">Select or deselect any of the listed styles, then click the **Apply** button to change the style of the displayed control.</span></span> <span data-ttu-id="7bc63-127">Кроме того, можно использовать кнопку **Повторное создание** , чтобы создать новый элемент управления с выбранными стилями.</span><span class="sxs-lookup"><span data-stu-id="7bc63-127">Alternately, you can use the **Recreate** button to create a new control with the selected styles.</span></span> <span data-ttu-id="7bc63-128">Кнопка « **Сброс** » вернет элемент управления к стилям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bc63-128">The **Reset** button will return the control to the default styles.</span></span>

<span data-ttu-id="7bc63-129">Кнопки **Копировать стиль** и **Копировать операторе EXSTYLE** , расположенные под вкладкой, будут копировать выбранные константы стиля в буфер обмена в виде побитового \| списка с разделителями или ().</span><span class="sxs-lookup"><span data-stu-id="7bc63-129">The **Copy Style** and **Copy ExStyle** buttons below the tab will copy the selected style constants to the Clipboard as a bitwise OR (\|) delimited list.</span></span> <span data-ttu-id="7bc63-130">Этот список можно вставить непосредственно в вызов [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , чтобы предоставить элемент управления в своем приложении с тем же стилем.</span><span class="sxs-lookup"><span data-stu-id="7bc63-130">You can paste this list directly into your call to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to provide a control in your own application with the same style.</span></span>

<span data-ttu-id="7bc63-131">На следующем рисунке показана вкладка **стили** для элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="7bc63-131">The following image shows the **Styles** tab for a button control.</span></span>

![управление вкладкой "стили Spy"](images/controlspy-styles.png)

## <a name="messages"></a><span data-ttu-id="7bc63-133">Сообщения</span><span class="sxs-lookup"><span data-stu-id="7bc63-133">Messages</span></span>

<span data-ttu-id="7bc63-134">Вкладка **сообщения** позволяет отправить почти любое сообщение в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="7bc63-134">The **Messages** tab enables you to send almost any message to a control.</span></span> <span data-ttu-id="7bc63-135">После выбора сообщения из списка можно ввести данные, которые отправляются в качестве параметров *wParam* и *lParam* для вызова [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="7bc63-135">After selecting a message from the list box, you can enter data which is sent as the *wParam* and *lParam* parameters of the call to [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="7bc63-136">После нажатия кнопки **Отправить** сообщение отправляется в элемент управления, и все результаты отображаются в текстовом поле в нижней части вкладки.</span><span class="sxs-lookup"><span data-stu-id="7bc63-136">After you click **Send**, the message is sent to the control and any result is displayed in the text box at the bottom of the tab.</span></span>

<span data-ttu-id="7bc63-137">На следующем рисунке показана вкладка сообщения при выборе определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="7bc63-137">The following image shows the messages tab when a particular message is selected.</span></span>

![управление вкладкой сообщений Spy](images/controlspy-messages.png)

## <a name="sizecolor"></a><span data-ttu-id="7bc63-139">Размер и цвет</span><span class="sxs-lookup"><span data-stu-id="7bc63-139">Size/Color</span></span>

<span data-ttu-id="7bc63-140">Вкладка **размер/цвет** может использоваться для изменения размера элемента управления, а также цвета его фона.</span><span class="sxs-lookup"><span data-stu-id="7bc63-140">The **Size/Color** tab can be used to change the size of the control as well as the color of its background.</span></span>

## <a name="where-to-get-control-spy"></a><span data-ttu-id="7bc63-141">Где получить управление Spy</span><span class="sxs-lookup"><span data-stu-id="7bc63-141">Where to Get Control Spy</span></span>

<span data-ttu-id="7bc63-142">Вы можете загрузить [элемент управления Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) с сайта MSDN.</span><span class="sxs-lookup"><span data-stu-id="7bc63-142">You can download [Control Spy 2.0](https://www.microsoft.com/download/details.aspx?id=4635) from MSDN.</span></span> <span data-ttu-id="7bc63-143">Обе версии содержатся в скачивании.</span><span class="sxs-lookup"><span data-stu-id="7bc63-143">Both versions are contained in the download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bc63-144">См. также</span><span class="sxs-lookup"><span data-stu-id="7bc63-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7bc63-145">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7bc63-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7bc63-146">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="7bc63-146">Windows Controls</span></span>](window-controls.md)
</dt> <dt>

[<span data-ttu-id="7bc63-147">Включение стилей оформления</span><span class="sxs-lookup"><span data-stu-id="7bc63-147">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> </dl>

 

 