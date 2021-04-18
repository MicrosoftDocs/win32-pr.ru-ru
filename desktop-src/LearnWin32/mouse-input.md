---
title: Ввод с помощью мыши (начало работы с Win32 и C++)
description: Ввод с помощью мыши
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105672437"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a><span data-ttu-id="afaff-103">Ввод с помощью мыши (начало работы с Win32 и C++)</span><span class="sxs-lookup"><span data-stu-id="afaff-103">Mouse Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="afaff-104">Windows поддерживает мыши до пяти кнопок: Left, Ближний и Right, а также две дополнительные кнопки с именами XBUTTON1 и XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="afaff-104">Windows supports mice with up to five buttons: left, middle, and right, plus two additional buttons called XBUTTON1 and XBUTTON2.</span></span>

![Иллюстрация, показывающая левую (1), правую (2), середину (3) и XBUTTON1 (4) кнопки.](images/mouse.png)

<span data-ttu-id="afaff-106">Большинство мышей для Windows имеют по крайней мере левую и правую кнопки.</span><span class="sxs-lookup"><span data-stu-id="afaff-106">Most mice for Windows have at least the left and right buttons.</span></span> <span data-ttu-id="afaff-107">Левая кнопка мыши используется для указания, выбора, перетаскивания и т. д.</span><span class="sxs-lookup"><span data-stu-id="afaff-107">The left mouse button is used for pointing, selecting, dragging, and so forth.</span></span> <span data-ttu-id="afaff-108">При нажатии правой кнопки мыши обычно отображается контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="afaff-108">The right mouse button typically displays a context menu.</span></span> <span data-ttu-id="afaff-109">Некоторые мыши имеют колесо прокрутки, расположенное между левой и правой кнопками.</span><span class="sxs-lookup"><span data-stu-id="afaff-109">Some mice have a scroll wheel located between the left and right buttons.</span></span> <span data-ttu-id="afaff-110">В зависимости от мыши колесо прокрутки можно также щелкнуть, сделав его средней кнопкой.</span><span class="sxs-lookup"><span data-stu-id="afaff-110">Depending on the mouse, the scroll wheel might also be clickable, making it the middle button.</span></span>

<span data-ttu-id="afaff-111">Кнопки XBUTTON1 и XBUTTON2 часто находятся на сторонах мыши, рядом с базой.</span><span class="sxs-lookup"><span data-stu-id="afaff-111">The XBUTTON1 and XBUTTON2 buttons are often located on the sides of the mouse, near the base.</span></span> <span data-ttu-id="afaff-112">Эти дополнительные кнопки отсутствуют на всех мышей.</span><span class="sxs-lookup"><span data-stu-id="afaff-112">These extra buttons are not present on all mice.</span></span> <span data-ttu-id="afaff-113">При наличии кнопок XBUTTON1 и XBUTTON2 часто сопоставляются с функциями приложения, такими как прямая и обратная Навигация в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="afaff-113">If present, the XBUTTON1 and XBUTTON2 buttons are often mapped to an application function, such as forward and backward navigation in a Web browser.</span></span>

<span data-ttu-id="afaff-114">Пользователи, работающие в левой части, часто покажут, что вы сможете поменять местами функции левой и правой кнопок, используя правую кнопку в качестве указателя, и левую кнопку, чтобы отобразить контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="afaff-114">Left-handed users often find it more comfortable to swap the functions of the left and right buttons—using the right button as the pointer, and the left button to show the context menu.</span></span> <span data-ttu-id="afaff-115">По этой причине в справочной документации Windows используется *ключевая кнопка основные* условия и *дополнительная кнопка*, которая ссылается на логическую функцию, а не на физическое размещение.</span><span class="sxs-lookup"><span data-stu-id="afaff-115">For this reason, the Windows help documentation uses the terms *primary button* and *secondary button*, which refer to logical function rather than physical placement.</span></span> <span data-ttu-id="afaff-116">В параметре по умолчанию (справа) слева находится основная кнопка, а право — вторичная кнопка.</span><span class="sxs-lookup"><span data-stu-id="afaff-116">In the default (right-handed) setting, the left button is the primary button and the right is the secondary button.</span></span> <span data-ttu-id="afaff-117">Тем не менее, по щелчку *правой кнопкой мыши* и *влево щелкните* ссылку на логические действия.</span><span class="sxs-lookup"><span data-stu-id="afaff-117">However, the terms *right click* and *left click* refer to logical actions.</span></span> <span data-ttu-id="afaff-118">Щелчок *правой кнопкой мыши* означает нажатие основной кнопки, независимо от того, находится ли эта кнопка в правой или левой части мыши.</span><span class="sxs-lookup"><span data-stu-id="afaff-118">*Right clicking* means clicking the primary button, whether that button is physically on the right or left side of the mouse.</span></span>

<span data-ttu-id="afaff-119">Независимо от того, как пользователь настраивает мышь, Windows автоматически преобразует сообщения мыши, чтобы они были единообразными.</span><span class="sxs-lookup"><span data-stu-id="afaff-119">Regardless of how the user configures the mouse, Windows automatically translates mouse messages so they are consistent.</span></span> <span data-ttu-id="afaff-120">Пользователь может поменять местами основную и дополнительную кнопки в середине использования программы, и это не повлияет на работу программы.</span><span class="sxs-lookup"><span data-stu-id="afaff-120">The user can swap the primary and secondary buttons in the middle of using your program, and it will not affect how your program behaves.</span></span>

<span data-ttu-id="afaff-121">В документации MSDN для обозначения *основной* и *дополнительной* кнопок используется *кнопка вправо* и *левая кнопка* .</span><span class="sxs-lookup"><span data-stu-id="afaff-121">MSDN documentation uses the terms *right button* and *left button* to mean *primary* and *secondary* button.</span></span> <span data-ttu-id="afaff-122">Эта терминология согласуется с именами оконных сообщений для ввода с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="afaff-122">This terminology is consistent with the names of the window messages for mouse input.</span></span> <span data-ttu-id="afaff-123">Просто помните, что физическая левая и правая кнопки могут быть заменены.</span><span class="sxs-lookup"><span data-stu-id="afaff-123">Just remember that the physical left and right buttons might be swapped.</span></span>

## <a name="next"></a><span data-ttu-id="afaff-124">Следующая</span><span class="sxs-lookup"><span data-stu-id="afaff-124">Next</span></span>

[<span data-ttu-id="afaff-125">Реагирование на щелчки мыши</span><span class="sxs-lookup"><span data-stu-id="afaff-125">Responding to Mouse Clicks</span></span>](mouse-clicks.md)

 

 




