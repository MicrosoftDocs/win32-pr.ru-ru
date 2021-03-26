---
description: Всякий раз, когда приложение создает контроллер домена и сразу же начинает вызывать функции рисования или вывода GDI, оно использует преимущества страничного пространства по умолчанию для пространства на устройстве, а также для преобразования устройств в клиентскую область.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Преобразования по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5f13c764a92c005fad36c9f2599b99a654284f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985004"
---
# <a name="default-transformations"></a><span data-ttu-id="fa644-103">Преобразования по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fa644-103">Default Transformations</span></span>

<span data-ttu-id="fa644-104">Всякий раз, когда приложение создает контроллер домена и сразу же начинает вызывать функции рисования или вывода GDI, оно использует преимущества страничного пространства по умолчанию для пространства на устройстве, а также для преобразования устройств в клиентскую область.</span><span class="sxs-lookup"><span data-stu-id="fa644-104">Whenever an application creates a DC and immediately begins calling GDI drawing or output functions, it takes advantage of the default page-space to device-space, and device-space to client-area transformations.</span></span> <span data-ttu-id="fa644-105">Преобразование "мир в Интернете" не может произойти до тех пор, пока приложение не вызовет функцию [**сетграфиксмоде**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) , чтобы задать для параметра mode значение GM \_ Advanced, а затем вызывает функцию [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .</span><span class="sxs-lookup"><span data-stu-id="fa644-105">A world-to-page space transformation cannot happen until the application first calls the [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) function to set the mode to GM\_ADVANCED and then calls the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function.</span></span>

<span data-ttu-id="fa644-106">Использование текста MM \_ (размер страницы по умолчанию в преобразовании «пространство на устройство») приводит к сопоставлению «один к одному», т. е. Указанная точка в пространстве страницы сопоставляется с той же точкой в пространстве устройства.</span><span class="sxs-lookup"><span data-stu-id="fa644-106">Use of MM\_TEXT (the default page-space to device-space transformation) results in a one-to-one mapping; that is, a given point in page space maps to the same point in device space.</span></span> <span data-ttu-id="fa644-107">Как упоминалось ранее, это преобразование не задается матрицей.</span><span class="sxs-lookup"><span data-stu-id="fa644-107">As previously mentioned, this transformation is not specified by a matrix.</span></span> <span data-ttu-id="fa644-108">Вместо этого она получается путем деления ширины окна просмотра на ширину и высоту области просмотра по высоте окна.</span><span class="sxs-lookup"><span data-stu-id="fa644-108">Instead, it is obtained by dividing the width of the viewport by the width of the window and the height of the viewport by the height of the window.</span></span> <span data-ttu-id="fa644-109">В случае по умолчанию размеры окна просмотра отображаются в 1 пиксель на 1 пиксель, а размеры окна — 1 единица с 1 страницей.</span><span class="sxs-lookup"><span data-stu-id="fa644-109">In the default case, the viewport dimensions are 1-pixel by 1-pixel and the window dimensions are 1-page unit by 1-page unit.</span></span>

<span data-ttu-id="fa644-110">Преобразование "место на устройстве" для физического устройства (клиентская область, Настольный компьютер или бумага в принтере) всегда приводит к сопоставлению "один к одному". то есть одна единица в пространстве устройства всегда эквивалентна одной единице в клиентской области, на рабочем столе или на странице.</span><span class="sxs-lookup"><span data-stu-id="fa644-110">The device-space to physical-device (client area, desktop, or printer paper) transformation always results in a one-to-one mapping; that is, one unit in device space is always equivalent to one unit in the client area, on the desktop, or on a page.</span></span> <span data-ttu-id="fa644-111">Единственное назначение этого преобразования — перевод; Он обеспечивает правильное отображение выходных данных в окне приложения независимо от того, где это окно перемещается на Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="fa644-111">The sole purpose of this transformation is translation; it ensures that output appears correctly in an application's window no matter where that window is moved on the desktop.</span></span>

<span data-ttu-id="fa644-112">Одним из уникальных аспектов текста MM \_ является ориентация оси y в пространстве страницы.</span><span class="sxs-lookup"><span data-stu-id="fa644-112">The one unique aspect of MM\_TEXT is the orientation of the y-axis in page space.</span></span> <span data-ttu-id="fa644-113">В \_ тексте mm положительная ось y расширяется вниз, а отрицательная ось y расширяется вверх.</span><span class="sxs-lookup"><span data-stu-id="fa644-113">In MM\_TEXT, the positive y-axis extends downward and the negative y-axis extends upward.</span></span>

 

 



