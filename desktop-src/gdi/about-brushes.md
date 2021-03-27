---
description: 'Существует два типа кистей: логическое и физическое.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: О кистях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155211"
---
# <a name="about-brushes"></a><span data-ttu-id="680bf-103">О кистях</span><span class="sxs-lookup"><span data-stu-id="680bf-103">About Brushes</span></span>

<span data-ttu-id="680bf-104">Существует два типа кистей: логическое и физическое.</span><span class="sxs-lookup"><span data-stu-id="680bf-104">There are two types of brushes: logical and physical.</span></span> <span data-ttu-id="680bf-105">*Логическая кисть* — это описание идеального точечного рисунка, используемого приложением для рисования фигур.</span><span class="sxs-lookup"><span data-stu-id="680bf-105">A *logical brush* is a description of the ideal bitmap that an application uses to paint shapes.</span></span> <span data-ttu-id="680bf-106">*Физическая кисть* — это фактический точечный рисунок, который создается драйвером устройства на основе определения логической кисти приложения.</span><span class="sxs-lookup"><span data-stu-id="680bf-106">A *physical brush* is the actual bitmap that a device driver creates based on an application's logical-brush definition.</span></span> <span data-ttu-id="680bf-107">Дополнительные сведения о растровых изображениях см. в разделе [точечные рисунки](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="680bf-107">For more information about bitmaps, see [Bitmaps](bitmaps.md).</span></span>

<span data-ttu-id="680bf-108">Когда приложение вызывает одну из функций, которые создают кисть, он получает дескриптор, идентифицирующий логическую кисть.</span><span class="sxs-lookup"><span data-stu-id="680bf-108">When an application calls one of the functions that creates a brush, it retrieves a handle that identifies a logical brush.</span></span> <span data-ttu-id="680bf-109">Когда приложение передает этот дескриптор функции [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) , драйвер устройства для соответствующего дисплея или принтера создает физическую кисть.</span><span class="sxs-lookup"><span data-stu-id="680bf-109">When the application passes this handle to the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function, the device driver for the corresponding display or printer creates the physical brush.</span></span>

<span data-ttu-id="680bf-110">В следующих разделах описываются кисти:</span><span class="sxs-lookup"><span data-stu-id="680bf-110">The following topics describe brushes:</span></span>

-   [<span data-ttu-id="680bf-111">Источник кисти</span><span class="sxs-lookup"><span data-stu-id="680bf-111">Brush Origin</span></span>](brush-origin.md)
-   [<span data-ttu-id="680bf-112">Логические типы кистей</span><span class="sxs-lookup"><span data-stu-id="680bf-112">Logical Brush Types</span></span>](logical-brush-types.md)
-   [<span data-ttu-id="680bf-113">Перенос блока шаблона</span><span class="sxs-lookup"><span data-stu-id="680bf-113">Pattern Block Transfer</span></span>](pattern-block-transfer.md)
-   [<span data-ttu-id="680bf-114">Функции-кисти с поддержкой ICM</span><span class="sxs-lookup"><span data-stu-id="680bf-114">ICM-Enabled Brush Functions</span></span>](icm-enabled-brush-functions.md)

 

 



