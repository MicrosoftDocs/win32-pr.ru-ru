---
title: Автоматическая обрезка
description: Автоматическая обрезка
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331272"
---
# <a name="automatic-clipping"></a><span data-ttu-id="74f38-103">Автоматическая обрезка</span><span class="sxs-lookup"><span data-stu-id="74f38-103">Automatic Clipping</span></span>

<span data-ttu-id="74f38-104">Настоятельно рекомендуется, чтобы контейнер элементов управления ActiveX поддерживал автоматическую обрезку своих элементов управления.</span><span class="sxs-lookup"><span data-stu-id="74f38-104">It is strongly recommended that an ActiveX control container supports automatic clipping of its controls.</span></span> <span data-ttu-id="74f38-105">Это приведет к более эффективной работе для большинства элементов управления.</span><span class="sxs-lookup"><span data-stu-id="74f38-105">This will result in more efficient operation for most controls.</span></span> <span data-ttu-id="74f38-106">Если автоматическая обрезка поддерживается, свойство окружения автоклипа должно поддерживаться и иметь значение **true**.</span><span class="sxs-lookup"><span data-stu-id="74f38-106">If automatic clipping is supported, the AutoClip ambient property must be supported and have a value of **TRUE**.</span></span>

<span data-ttu-id="74f38-107">Автоматическая обрезка — это возможность контейнера, гарантирующая, что рисуемый выход элемента управления поступает только в текущую область отсечения контейнера.</span><span class="sxs-lookup"><span data-stu-id="74f38-107">Automatic clipping is the ability of a container to ensure that a control's drawn output goes only to the container's current clipping region.</span></span> <span data-ttu-id="74f38-108">В контейнере, поддерживающем автоматическую обрезку, элемент управления может рисовать без учета его области отсечения, поскольку контейнер автоматически обрезает все прорисовки, которые происходят за пределами области элемента управления.</span><span class="sxs-lookup"><span data-stu-id="74f38-108">In a container that supports automatic clipping, a control can paint without regard to its clipping region, because the container will automatically clip any painting that occurs outside the control's area.</span></span> <span data-ttu-id="74f38-109">Если контейнер не поддерживает автоматическую обрезку, элементы управления, созданные с помощью пакета CDK, будут создавать дополнительное родительское окно, если передается непустая область обрезки.</span><span class="sxs-lookup"><span data-stu-id="74f38-109">If a container does not support automatic clipping, then CDK-generated controls will create an extra parent window if a non-null clipping region is passed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74f38-110">См. также</span><span class="sxs-lookup"><span data-stu-id="74f38-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74f38-111">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="74f38-111">Containers</span></span>](containers.md)
</dt> </dl>

 

 




