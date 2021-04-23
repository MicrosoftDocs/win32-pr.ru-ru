---
title: Окно символов
description: Окно символов
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414228"
---
# <a name="the-character-window"></a><span data-ttu-id="ab8da-103">Окно символов</span><span class="sxs-lookup"><span data-stu-id="ab8da-103">The Character Window</span></span>

<span data-ttu-id="ab8da-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ab8da-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="ab8da-105">Microsoft Agent отображает анимированные символы в собственных окнах, которые всегда отображаются в верхней части z-порядка (то есть всегда поверх остальных окон).</span><span class="sxs-lookup"><span data-stu-id="ab8da-105">Microsoft Agent displays animated characters in their own windows that always appear at the top of the window z-order (that is, always on top).</span></span> <span data-ttu-id="ab8da-106">Пользователь может переместить окно символа, перетащив его с помощью левой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="ab8da-106">A user can move a character's window by dragging the character with the left mouse button.</span></span> <span data-ttu-id="ab8da-107">Изображение символа перемещается с указателем.</span><span class="sxs-lookup"><span data-stu-id="ab8da-107">The character image moves with the pointer.</span></span> <span data-ttu-id="ab8da-108">Кроме того, приложение может перемещать символ с помощью метода [**MoveTo**](moveto-method.md) .</span><span class="sxs-lookup"><span data-stu-id="ab8da-108">In addition, an application can move a character using the [**MoveTo**](moveto-method.md) method.</span></span>

<span data-ttu-id="ab8da-109">Когда пользователь щелкает правой кнопкой мыши символ, появляется всплывающее меню, в котором отображаются следующие команды:</span><span class="sxs-lookup"><span data-stu-id="ab8da-109">When the user right-clicks a character, a pop-up menu appears that displays the following commands:</span></span>

<span data-ttu-id="ab8da-110">Открыть \| окно "Close <span class="underline">V</span>лосовой Commands"</span><span class="sxs-lookup"><span data-stu-id="ab8da-110">Open \| Close <span class="underline">V</span>oice Commands Window</span></span>

<span data-ttu-id="ab8da-111"><span class="underline">H</span>IDE</span><span class="sxs-lookup"><span data-stu-id="ab8da-111"><span class="underline">H</span>ide</span></span>

<span data-ttu-id="ab8da-112">----------------------------…</span><span class="sxs-lookup"><span data-stu-id="ab8da-112">----------------------------…</span></span>

<span data-ttu-id="ab8da-113">Get-Help\*</span><span class="sxs-lookup"><span data-stu-id="ab8da-113">Command\*</span></span>


<span data-ttu-id="ab8da-114">*осерхостингаппликатионкаптион\*\**</span><span class="sxs-lookup"><span data-stu-id="ab8da-114">*OtherHostingApplicationCaption\*\**</span></span>

<span data-ttu-id="ab8da-115">\*Перечисленные команды основаны на клиенте input-Active.</span><span class="sxs-lookup"><span data-stu-id="ab8da-115">\*Commands listed are based on the input-active client.</span></span> <span data-ttu-id="ab8da-116">Дополнительные сведения об определении команд, отображаемых во всплывающем меню, см. в разделе Общие сведения о интерфейсе программирования агента Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ab8da-116">For more information on defining commands that appear in the pop-up menu, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="ab8da-117">\*\*Перечисленные записи — это все остальные приложения, в которых в настоящее время размещается символ.</span><span class="sxs-lookup"><span data-stu-id="ab8da-117">\*\*Entries listed are all other applications currently hosting the character.</span></span> <span data-ttu-id="ab8da-118">Дополнительные сведения об определении этой записи см. в статье Обзор программного интерфейса агента Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ab8da-118">For more information on defining this entry, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="ab8da-119">Команда открыть \| окно закрытия речи управляет отображением окна команд текущего активного символа.</span><span class="sxs-lookup"><span data-stu-id="ab8da-119">The Open \| Close Voice Commands Window command controls the display of the Commands Window of the current active character.</span></span> <span data-ttu-id="ab8da-120">Если службы распознавания речи отключены, эта команда отключена.</span><span class="sxs-lookup"><span data-stu-id="ab8da-120">If speech recognition services are disabled, this command is disabled.</span></span> <span data-ttu-id="ab8da-121">Если службы распознавания речи не установлены, эта команда не отображается.</span><span class="sxs-lookup"><span data-stu-id="ab8da-121">If speech recognition services are not installed, this command does not appear.</span></span>

<span data-ttu-id="ab8da-122">Команда Hide скрывает символ.</span><span class="sxs-lookup"><span data-stu-id="ab8da-122">The Hide command hides the character.</span></span> <span data-ttu-id="ab8da-123">Анимация, назначенная **скрытому** состоянию символа, воспроизводит и скрывает символ.</span><span class="sxs-lookup"><span data-stu-id="ab8da-123">The animation assigned to the character's **Hiding** state plays and hides the character.</span></span> <span data-ttu-id="ab8da-124">Буква "H" в разделе "скрыть" — это клавиша доступа команды (назначенная).</span><span class="sxs-lookup"><span data-stu-id="ab8da-124">The letter "H" in hide is the command's access key (mnemonic).</span></span>

<span data-ttu-id="ab8da-125">Команды для приложений, на которых в данный момент размещается символ, следуют за командой Hide, перед которой стоит разделитель.</span><span class="sxs-lookup"><span data-stu-id="ab8da-125">The commands for the application(s) currently hosting the character follow the Hide command, preceded by a separator.</span></span> <span data-ttu-id="ab8da-126">Имена других приложений, использующих этот символ, также предшествуют разделителю.</span><span class="sxs-lookup"><span data-stu-id="ab8da-126">Then the names of other applications using the character appear, also preceded by a separator.</span></span>

 

 




