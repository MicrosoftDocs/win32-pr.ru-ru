---
description: Используйте стандартные элементы управления Windows, когда это возможно, так как они полностью совместимы с рекомендациями Microsoft Active Accessibility. К ним относятся элементы управления, предоставляемые Windows (User32.dll) и библиотека стандартных элементов управления Windows (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Использование стандартных элементов управления Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343285"
---
# <a name="using-standard-windows-controls"></a><span data-ttu-id="538e0-104">Использование стандартных элементов управления Windows</span><span class="sxs-lookup"><span data-stu-id="538e0-104">Using Standard Windows Controls</span></span>

<span data-ttu-id="538e0-105">Используйте стандартные элементы управления Windows, когда это возможно, так как они полностью совместимы с рекомендациями Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="538e0-105">Use standard Windows controls whenever possible, because they are fully compatible with Microsoft Active Accessibility guidelines.</span></span> <span data-ttu-id="538e0-106">К ним относятся элементы управления, предоставляемые Windows (User32.dll) и библиотека стандартных элементов управления Windows (Comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="538e0-106">This includes controls provided by Windows (User32.dll) and the Windows common controls library (Comctl32.dll).</span></span>

<span data-ttu-id="538e0-107">Каждый стандартный элемент управления Windows является отдельным окном определенного класса, поэтому специальные возможности уведомляются при перемещении фокуса на новый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="538e0-107">Each standard Windows control is a separate window of a specific class, so the accessibility aid is notified when the focus moves to a new control.</span></span> <span data-ttu-id="538e0-108">Вспомогательная помощь может определить класс окна Controls и все дополнительные сообщения, которые он может отправить для запроса или изменить состояние элементов управления.</span><span class="sxs-lookup"><span data-stu-id="538e0-108">The aid can determine the controls window class, and any additional messages it can send to query or alter the controls state.</span></span> <span data-ttu-id="538e0-109">Кроме того, вспомогательное средство может идентифицировать все дочерние элементы управления, содержащиеся в родительском окне, и идентифицировать родителя любого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="538e0-109">The aid can also identify all of the child controls contained within a parent window and identify the parent of any control.</span></span>

<span data-ttu-id="538e0-110">Некоторые стандартные элементы управления являются чрезвычайно гибкими и часто могут подставляться для менее доступных пользовательских элементов управления и элементов управления, рисуемых владельцем.</span><span class="sxs-lookup"><span data-stu-id="538e0-110">Some common controls are extremely flexible and can often substitute for less-accessible custom controls and owner-drawn controls.</span></span> <span data-ttu-id="538e0-111">Например, представление списка может заменить рисуемый владельцем список для отображения флажка рядом с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="538e0-111">For example, a list view can replace an owner-drawn list box to display a check box next to each item.</span></span> <span data-ttu-id="538e0-112">Другой пример: расширенный элемент управления "Кнопка" может отображать как изображения, так и текст.</span><span class="sxs-lookup"><span data-stu-id="538e0-112">As another example, the enhanced button control can display both images and text.</span></span> <span data-ttu-id="538e0-113">Ранее это требовало использования пользовательского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="538e0-113">Previously, this required the use of a custom control.</span></span>

 

 



