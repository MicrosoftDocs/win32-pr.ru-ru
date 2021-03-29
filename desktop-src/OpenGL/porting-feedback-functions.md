---
title: Перенос функций обратной связи
description: При использовании IRI GL способ обработки отзывов зависит от компьютера, на котором выполняется IRI GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- Перенос GL по IRI, обратная связь
- Перенос из ДИАФРАГМы в ГК, обратная связь
- Перенос на OpenGL из IRI GL, обратная связь
- Перенос по стандарту OpenGL из IRI GL, обратная связь
- обратная связь
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258808"
---
# <a name="porting-feedback-functions"></a><span data-ttu-id="051bc-108">Перенос функций обратной связи</span><span class="sxs-lookup"><span data-stu-id="051bc-108">Porting Feedback Functions</span></span>

<span data-ttu-id="051bc-109">При использовании IRI GL способ обработки отзывов зависит от компьютера, на котором выполняется IRI GL.</span><span class="sxs-lookup"><span data-stu-id="051bc-109">With IRIS GL, the way that feedback is handled differs depending on the computer running IRIS GL.</span></span> <span data-ttu-id="051bc-110">OpenGL стандартизируют функции обратной связи, чтобы вы могли полагаться на согласованную обратную связь между различными аппаратными платформами.</span><span class="sxs-lookup"><span data-stu-id="051bc-110">OpenGL standardizes feedback functions so you can rely on consistent feedback among various hardware platforms.</span></span> <span data-ttu-id="051bc-111">В следующей таблице перечислены функции обратной связи для IRI и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="051bc-111">The following table lists the IRIS GL feedback functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="051bc-112">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="051bc-112">IRIS GL function</span></span> | <span data-ttu-id="051bc-113">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="051bc-113">OpenGL function</span></span>                                                                                            | <span data-ttu-id="051bc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="051bc-114">Meaning</span></span>                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="051bc-115">**оставлять**</span><span class="sxs-lookup"><span data-stu-id="051bc-115">**feedback**</span></span>     | <span data-ttu-id="051bc-116">[**глрендермоде**](glrendermode.md) ( \_ обратная связь в ГК)</span><span class="sxs-lookup"><span data-stu-id="051bc-116">[**glRenderMode**](glrendermode.md) ( GL\_FEEDBACK )</span></span>                                                      | <span data-ttu-id="051bc-117">Переключается в режим обратной связи.</span><span class="sxs-lookup"><span data-stu-id="051bc-117">Switches to feedback mode.</span></span>                    |
| <span data-ttu-id="051bc-118">**ендфидбакк**</span><span class="sxs-lookup"><span data-stu-id="051bc-118">**endfeedback**</span></span>  | <span data-ttu-id="051bc-119">[**глрендермоде**](glrendermode.md) ( \_ рендеринг GL)[**глфидбаккбуффер**](glfeedbackbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="051bc-119">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )[**glFeedbackBuffer**](glfeedbackbuffer.md)</span></span><br/> | <span data-ttu-id="051bc-120">Переключается в режим рендеринга.</span><span class="sxs-lookup"><span data-stu-id="051bc-120">Switches to rendering mode.</span></span>                   |
| <span data-ttu-id="051bc-121">**Сылка**</span><span class="sxs-lookup"><span data-stu-id="051bc-121">**passthrough**</span></span>  | [<span data-ttu-id="051bc-122">**глпасссраугх**</span><span class="sxs-lookup"><span data-stu-id="051bc-122">**glPassThrough**</span></span>](glpassthrough.md)                                                                     | <span data-ttu-id="051bc-123">Помещает маркер маркера в буфер обратной связи.</span><span class="sxs-lookup"><span data-stu-id="051bc-123">Places a token marker in the feedback buffer.</span></span> |



 

 

 





