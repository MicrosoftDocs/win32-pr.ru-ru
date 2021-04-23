---
description: Перо Tablet PC может иметь несколько конечных сторон, которые могут взаимодействовать с дигитайзером.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Несколько функциональных возможностей с одним пером
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349882"
---
# <a name="multiple-functionality-with-one-pen"></a><span data-ttu-id="36ebd-103">Несколько функциональных возможностей с одним пером</span><span class="sxs-lookup"><span data-stu-id="36ebd-103">Multiple Functionality with One Pen</span></span>

<span data-ttu-id="36ebd-104">Перо Tablet PC может иметь несколько конечных сторон, которые могут взаимодействовать с дигитайзером.</span><span class="sxs-lookup"><span data-stu-id="36ebd-104">A Tablet PC pen may have more than one end that can interact with the digitizer.</span></span> <span data-ttu-id="36ebd-105">Если оба конца пера могут создавать события, можно использовать один конец для размещения рукописного ввода, выбора и указания, а другой — для других функций, таких как удаление.</span><span class="sxs-lookup"><span data-stu-id="36ebd-105">If both ends of the pen can generate events, one end may be used to lay down ink, select, and point, and the other end may be used for other functions such as erasing.</span></span>

<span data-ttu-id="36ebd-106">Для реализации таких функций приложение должно иметь возможность определить, какой конец пера используется, и, соответственно, изменить внешний вид курсора.</span><span class="sxs-lookup"><span data-stu-id="36ebd-106">To implement such functionality, your application must be able to determine which end of the pen is being used and hence when to change the appearance of the cursor.</span></span> <span data-ttu-id="36ebd-107">Это можно сделать путем поиска состояния [**инвертированного**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) свойства в объекте [**курсора**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="36ebd-107">It can do this by looking for the state of the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

<span data-ttu-id="36ebd-108">Конкретные сведения об использовании задней части пера для стирания см. в разделе [стирание рукописного ввода с помощью пера](erasing-ink-with-the-pen.md).</span><span class="sxs-lookup"><span data-stu-id="36ebd-108">For specific details about using the back of the pen for erasing, see [Erasing Ink with the Pen](erasing-ink-with-the-pen.md).</span></span> <span data-ttu-id="36ebd-109">Кроме того, [Пример стирания рукописного ввода](ink-erasing-sample.md) демонстрирует, как использовать заднюю часть пера для стирания рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="36ebd-109">In addition, the [Ink Erasing Sample](ink-erasing-sample.md) demonstrates how to use the back of the pen to erase ink.</span></span>

 

 



