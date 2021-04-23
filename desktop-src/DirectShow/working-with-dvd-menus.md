---
description: Работа с меню DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Работа с меню DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684710"
---
# <a name="working-with-dvd-menus"></a><span data-ttu-id="d21ab-103">Работа с меню DVD</span><span class="sxs-lookup"><span data-stu-id="d21ab-103">Working With DVD Menus</span></span>

<span data-ttu-id="d21ab-104">Навигатор DVD может показывать меню, когда пользователь активирует кнопку или когда навигатор входит в первый домен воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d21ab-104">The DVD Navigator might show a menu when the user activates a button, or when the Navigator enters the First Play domain.</span></span> <span data-ttu-id="d21ab-105">Чтобы отобразить меню программным способом, вызовите метод [**IDvdControl2:: шовмену**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) .</span><span class="sxs-lookup"><span data-stu-id="d21ab-105">To show a menu programmatically, call the [**IDvdControl2::ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) method.</span></span>

<span data-ttu-id="d21ab-106">Существует несколько способов выбора кнопок меню программным способом.</span><span class="sxs-lookup"><span data-stu-id="d21ab-106">There are several ways to select menu buttons programmatically:</span></span>

-   <span data-ttu-id="d21ab-107">Чтобы выбрать кнопку по номеру, вызовите [**IDvdControl2:: селектбуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span><span class="sxs-lookup"><span data-stu-id="d21ab-107">To select a button by number, call [**IDvdControl2::SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span></span> <span data-ttu-id="d21ab-108">Номера кнопок нумеруются от 1 до 36.</span><span class="sxs-lookup"><span data-stu-id="d21ab-108">Buttons are numbered 1 to 36.</span></span> <span data-ttu-id="d21ab-109">Метод [**IDvdInfo2:: жеткуррентбуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) возвращает количество доступных кнопок.</span><span class="sxs-lookup"><span data-stu-id="d21ab-109">The [**IDvdInfo2::GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) method returns the number of available buttons.</span></span>
-   <span data-ttu-id="d21ab-110">Чтобы выбрать кнопку относительно положения выбранной в данный момент кнопки, вызовите метод [**IDvdControl2:: селектрелативебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span><span class="sxs-lookup"><span data-stu-id="d21ab-110">To select a button relative to the position of the currently selected button, call [**IDvdControl2::SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span></span> <span data-ttu-id="d21ab-111">Можно выбрать кнопку в направлении вверх, вниз, влево или вправо.</span><span class="sxs-lookup"><span data-stu-id="d21ab-111">You can select a button in the up, down, left, or right direction.</span></span>
-   <span data-ttu-id="d21ab-112">Чтобы выбрать кнопку по ее координатам в окне, вызовите [**IDvdControl2:: селектатпоситион**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span><span class="sxs-lookup"><span data-stu-id="d21ab-112">To select a button by its coordinates within the window, call [**IDvdControl2::SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span></span> <span data-ttu-id="d21ab-113">Этот метод принимает координаты (x, y) относительно клиентской области окна видео.</span><span class="sxs-lookup"><span data-stu-id="d21ab-113">This method takes (x,y) coordinates relative to the client area of the video window.</span></span> <span data-ttu-id="d21ab-114">(Для режима без окон это окно приложения.) Если в этом месте нет кнопки, метод возвращает \_ кнопку VFW E \_ DVD \_ No (нет) \_ .</span><span class="sxs-lookup"><span data-stu-id="d21ab-114">(For windowless mode, this is the application window.) If there is no button at that location, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="d21ab-115">Кроме того, существует несколько способов активации кнопки:</span><span class="sxs-lookup"><span data-stu-id="d21ab-115">In addition, there are several ways to activate a button:</span></span>

-   <span data-ttu-id="d21ab-116">Чтобы активировать кнопку по номеру, вызовите [**IDvdControl2:: селектандактиватебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span><span class="sxs-lookup"><span data-stu-id="d21ab-116">To activate a button by number, call [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span></span>
-   <span data-ttu-id="d21ab-117">Чтобы активировать кнопку по ее координатам, вызовите [**IDvdControl2:: активатеатпоситион**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span><span class="sxs-lookup"><span data-stu-id="d21ab-117">To activate a button by its coordinates, call [**IDvdControl2::ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span></span>
-   <span data-ttu-id="d21ab-118">Чтобы активировать кнопку, которая в данный момент выбрана, вызовите метод [**IDvdControl2:: активатебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span><span class="sxs-lookup"><span data-stu-id="d21ab-118">To activate the button that is currently selected, call [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span></span> <span data-ttu-id="d21ab-119">Если кнопка не выбрана, метод возвращает кнопку VFW \_ E \_ DVD \_ No \_ (нет).</span><span class="sxs-lookup"><span data-stu-id="d21ab-119">If no button is selected, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="d21ab-120">Помните, что при выборе кнопки просто выделяются ее границы.</span><span class="sxs-lookup"><span data-stu-id="d21ab-120">Keep in mind that selecting a button merely highlights its borders.</span></span> <span data-ttu-id="d21ab-121">Чтобы запустить связанную команду, необходимо активировать кнопку.</span><span class="sxs-lookup"><span data-stu-id="d21ab-121">To cause the associated command to be fired, the button must be activated.</span></span> <span data-ttu-id="d21ab-122">Программная активация кнопки может выполняться различными способами, но перед активацией эту кнопку всегда нужно выбрать.</span><span class="sxs-lookup"><span data-stu-id="d21ab-122">Activating a button programmatically can be done in various ways, but the button must always be selected before it can be activated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d21ab-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d21ab-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d21ab-124">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="d21ab-124">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



