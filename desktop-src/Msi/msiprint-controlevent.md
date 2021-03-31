---
description: Это событие публикуется элементом управления Скроллаблетекст, чтобы позволить пользователю распечатать содержимое этого элемента управления.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: Мсипринт таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913263"
---
# <a name="msiprint-controlevent"></a><span data-ttu-id="c7a77-103">Мсипринт таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="c7a77-103">MsiPrint ControlEvent</span></span>

<span data-ttu-id="c7a77-104">Это событие публикуется [элементом управления скроллаблетекст](scrollabletext-control.md) , чтобы позволить пользователю распечатать содержимое этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c7a77-104">This event is published by the [ScrollableText Control](scrollabletext-control.md) to enable the user to print the contents of that control.</span></span>

<span data-ttu-id="c7a77-105">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c7a77-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="c7a77-106">Этот таблице ControlEvent событие доступен начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="c7a77-106">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="c7a77-107">На это событие следует подписывать [элемент управления "кнопка](pushbutton-control.md) ", расположенный в том же диалоговом окне, что и [элемент управления скроллаблетекст](scrollabletext-control.md).</span><span class="sxs-lookup"><span data-stu-id="c7a77-107">This event should be subscribed to by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the [ScrollableText Control](scrollabletext-control.md).</span></span> <span data-ttu-id="c7a77-108">Семсипринт таблице ControlEvent событие должен быть создан в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="c7a77-108">TheMsiPrint ControlEvent should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="c7a77-109">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="c7a77-109">Published By</span></span>

[<span data-ttu-id="c7a77-110">скроллаблетекст</span><span class="sxs-lookup"><span data-stu-id="c7a77-110">ScrollableText</span></span>](scrollabletext-control.md)

## <a name="argument"></a><span data-ttu-id="c7a77-111">Аргумент</span><span class="sxs-lookup"><span data-stu-id="c7a77-111">Argument</span></span>

<span data-ttu-id="c7a77-112">В этом таблице ControlEvent событие не используется аргумент.</span><span class="sxs-lookup"><span data-stu-id="c7a77-112">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c7a77-113">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="c7a77-113">Action on Subscribers</span></span>

<span data-ttu-id="c7a77-114">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="c7a77-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c7a77-115">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="c7a77-115">Typical Use</span></span>

<span data-ttu-id="c7a77-116">Элемент управления " [кнопка](pushbutton-control.md) " в том же диалоговом окне, что и [элемент управления скроллаблетекст](scrollabletext-control.md) , может использоваться для отображения модального диалогового окна, позволяющего пользователю распечатать содержимое элемента управления скроллаблетекст.</span><span class="sxs-lookup"><span data-stu-id="c7a77-116">A [PushButton](pushbutton-control.md) control on the same dialog box as the [ScrollableText Control](scrollabletext-control.md) can be used to display a modal dialog box enabling the user to print the contents of the ScrollableText Control.</span></span>

 

 



