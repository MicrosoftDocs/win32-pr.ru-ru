---
description: Объект InkOverlay можно присоединить к элементу управления "окно" и использовать для реализации базовой возможности рукописного ввода.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Стирание с помощью объекта InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf85926f3566340cbde0d3202f3485e7c54cccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810085"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a><span data-ttu-id="d21fb-103">Стирание с помощью объекта InkOverlay</span><span class="sxs-lookup"><span data-stu-id="d21fb-103">Erasing by Using the InkOverlay Object</span></span>

<span data-ttu-id="d21fb-104">Объект [**InkOverlay**](inkoverlay-class.md) можно присоединить к элементу управления "окно" и использовать для реализации базовой возможности рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="d21fb-104">The [**InkOverlay**](inkoverlay-class.md) object can be attached to a window control and is used to enable basic ink capability.</span></span> <span data-ttu-id="d21fb-105">Объект **InkOverlay** можно использовать для стирания рукописного ввода, установив свойство [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) равным **Delete**.</span><span class="sxs-lookup"><span data-stu-id="d21fb-105">You can use the **InkOverlay** object to erase ink by setting the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) property equal to **Delete**.</span></span> <span data-ttu-id="d21fb-106">Затем можно присвоить свойству [**ерасермоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) либо элемент **Stroke** , либо элемент **Point** объекта [**инковерлайерасермоде**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode).</span><span class="sxs-lookup"><span data-stu-id="d21fb-106">You can then set the [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) property to either the **Stroke** or **Point** members of [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode).</span></span> <span data-ttu-id="d21fb-107">Установка для свойства **ерасермоде** значения **Stroke** стирает все штрихи.</span><span class="sxs-lookup"><span data-stu-id="d21fb-107">Setting the **EraserMode** property to **Stroke** erases entire strokes.</span></span> <span data-ttu-id="d21fb-108">Установка для свойства **ерасермоде** значения **Point** стирает перо, над которым проходит курсор.</span><span class="sxs-lookup"><span data-stu-id="d21fb-108">Setting the **EraserMode** property to **Point** erases the ink that the cursor passes over.</span></span>

 

 



