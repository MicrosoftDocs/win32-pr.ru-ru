---
description: Смешение цветов позволяет приложению создавать новые цвета, комбинируя перо или цвет кисти с цветами в существующем изображении.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Смешение цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155659"
---
# <a name="color-mixing"></a><span data-ttu-id="ea688-103">Смешение цветов</span><span class="sxs-lookup"><span data-stu-id="ea688-103">Color Mixing</span></span>

<span data-ttu-id="ea688-104">Смешение цветов позволяет приложению создавать новые цвета, комбинируя перо или цвет кисти с цветами в существующем изображении.</span><span class="sxs-lookup"><span data-stu-id="ea688-104">Color mixing lets an application create new colors by combining the pen or brush color with colors in the existing image.</span></span> <span data-ttu-id="ea688-105">Приложение может выбрать, как нарисовать перо или цвет кисти (фактически обрисуя любой существующий образ) или смешивать цвет с уже присутствующими цветами.</span><span class="sxs-lookup"><span data-stu-id="ea688-105">The application can choose either to draw the pen or brush color as is (effectively drawing over any existing image) or to mix the color with the colors already present.</span></span>

<span data-ttu-id="ea688-106">Режим многоцветового набора, который иногда называют операцией двоичной растровой операции, определяет, как эти цвета смешиваются.</span><span class="sxs-lookup"><span data-stu-id="ea688-106">The foreground mix mode, sometimes called the binary raster operation, determines how these colors are mixed.</span></span> <span data-ttu-id="ea688-107">Приложение может объединять цвета, сохраняя все компоненты обоих цветов. цвета маски, удаление или контроль компонентов, которые не являются общими; или только цвета маски, удаление или контроль общих компонентов.</span><span class="sxs-lookup"><span data-stu-id="ea688-107">An application can merge colors, preserving all components of both colors; mask colors, removing or moderating components that are not common; or exclusively mask colors, removing or moderating components that are common.</span></span> <span data-ttu-id="ea688-108">В этих основных операциях смешения существует несколько вариантов.</span><span class="sxs-lookup"><span data-stu-id="ea688-108">There are several variations on these basic mixing operations.</span></span>

<span data-ttu-id="ea688-109">Смешение цветов регулируется приближением к цвету.</span><span class="sxs-lookup"><span data-stu-id="ea688-109">Color mixing is subject to color approximation.</span></span> <span data-ttu-id="ea688-110">Если результатом смешения цветов является цвет, который не может быть создан устройством, система приближена к результату, используя цвет, который он может создать.</span><span class="sxs-lookup"><span data-stu-id="ea688-110">If the result of color mixing is a color that the device cannot generate, the system approximates the result, using a color it can generate.</span></span> <span data-ttu-id="ea688-111">Если приложение смешивается с переносящимися цветами, отдельные цвета, используемые для создания такого цвета, будут смешиваться, а результаты будут подвергаться приближению к цветовой аппроксимации.</span><span class="sxs-lookup"><span data-stu-id="ea688-111">If an application mixes dithered colors, the individual colors used to create the dithered color are mixed, and the results are subject to color approximation.</span></span>

<span data-ttu-id="ea688-112">Приложение устанавливает режим фонового набора с помощью функции [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) и получает текущий режим с помощью функции [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) .</span><span class="sxs-lookup"><span data-stu-id="ea688-112">An application sets the foreground mix mode by using the [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) function and retrieves the current mode by using the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) function.</span></span>

<span data-ttu-id="ea688-113">Хотя существует режим фонового набора, этот режим не управляет смешением цветов.</span><span class="sxs-lookup"><span data-stu-id="ea688-113">Although there is a background mix mode, that mode does not control the mixing of colors.</span></span> <span data-ttu-id="ea688-114">Вместо этого он указывает, используется ли цвет фона при рисовании линий в стиле, штриховых кистей и текста.</span><span class="sxs-lookup"><span data-stu-id="ea688-114">Instead, it specifies whether a background color is used when drawing styled lines, hatched brushes, and text.</span></span>

 

 



