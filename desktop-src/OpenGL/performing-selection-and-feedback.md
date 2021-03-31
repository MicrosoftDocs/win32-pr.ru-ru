---
title: Выполнив выбор и обратную связь
description: Выполнив выбор и обратную связь
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, выбор
- OpenGL, обратная связь
- OpenGL, подготовка к просмотру
- режим выбора OpenGL
- режим отзывов OpenGL
- режим рендеринга OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329995"
---
# <a name="performing-selection-and-feedback"></a><span data-ttu-id="8f904-109">Выполнив выбор и обратную связь</span><span class="sxs-lookup"><span data-stu-id="8f904-109">Performing Selection and Feedback</span></span>

<span data-ttu-id="8f904-110">Выбор, обратная связь и подготовка к просмотру являются взаимоисключающими режимами работы.</span><span class="sxs-lookup"><span data-stu-id="8f904-110">Selection, feedback, and rendering are mutually exclusive modes of operation.</span></span> <span data-ttu-id="8f904-111">Отрисовка является нормальным режимом по умолчанию, во время которого фрагменты создаются с помощью растрирования.</span><span class="sxs-lookup"><span data-stu-id="8f904-111">Rendering is the normal, default mode during which fragments are produced by rasterization.</span></span>

<span data-ttu-id="8f904-112">В режимах выбора и обратной связи никакие фрагменты не создаются. Поэтому изменение буфера кадров не происходит.</span><span class="sxs-lookup"><span data-stu-id="8f904-112">In selection and feedback modes, no fragments are produced; therefore, no framebuffer modification occurs.</span></span> <span data-ttu-id="8f904-113">В режиме выбора можно определить, какие примитивы будут отображаться в некоторой области окна. в режиме обратной связи сведения о примитивах, которые будут растрируются, поправляются обратно в приложение.</span><span class="sxs-lookup"><span data-stu-id="8f904-113">In selection mode, you can determine which primitives will be drawn into some region of a window; in feedback mode, information about primitives that will be rasterized is fed back to the application.</span></span>

<span data-ttu-id="8f904-114">Вы выбираете из этих трех режимов с помощью [**глрендермоде**](glrendermode.md).</span><span class="sxs-lookup"><span data-stu-id="8f904-114">You select among these three modes with [**glRenderMode**](glrendermode.md).</span></span>

-   [<span data-ttu-id="8f904-115">Выбор</span><span class="sxs-lookup"><span data-stu-id="8f904-115">Selection</span></span>](selection.md)
-   [<span data-ttu-id="8f904-116">Отзывы</span><span class="sxs-lookup"><span data-stu-id="8f904-116">Feedback</span></span>](feedback.md)
-   [<span data-ttu-id="8f904-117">Ссылка на выбор и обратную связь</span><span class="sxs-lookup"><span data-stu-id="8f904-117">Selection and Feedback Reference</span></span>](selection-and-feedback-reference.md)

 

 




