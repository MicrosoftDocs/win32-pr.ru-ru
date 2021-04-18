---
description: Метод Step перемещает DVD-Video поток на указанное число кадров.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Метод Step
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674168"
---
# <a name="step-method"></a><span data-ttu-id="510b1-103">Метод Step</span><span class="sxs-lookup"><span data-stu-id="510b1-103">Step Method</span></span>

> [!Note]  
> <span data-ttu-id="510b1-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="510b1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="510b1-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="510b1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="510b1-106">`Step`Метод перемещает DVD-Video поток на указанное число кадров.</span><span class="sxs-lookup"><span data-stu-id="510b1-106">The `Step` method advances the DVD-Video stream by the specified number of frames.</span></span>

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a><span data-ttu-id="510b1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="510b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="510b1-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*IFRAME*</span><span class="sxs-lookup"><span data-stu-id="510b1-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="510b1-109">Указывает количество кадров для шага в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="510b1-109">Specifies the number of frames to step as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="510b1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="510b1-110">Return Value</span></span>

<span data-ttu-id="510b1-111">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="510b1-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="510b1-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="510b1-112">Remarks</span></span>

<span data-ttu-id="510b1-113">Перед вызовом этого метода вызовите [**канстеп**](canstep-method.md) , чтобы определить, поддерживает ли декодер пошаговое выполнение.</span><span class="sxs-lookup"><span data-stu-id="510b1-113">Before calling this method, call [**CanStep**](canstep-method.md) to determine whether the decoder supports frame stepping.</span></span>

<span data-ttu-id="510b1-114">Если DVD-Video воспроизводится в обратном режиме при вызове этого метода, а декодер поддерживает обратный шаг за кадром, то пошаговое выполнение пакета выполняется в обратную.</span><span class="sxs-lookup"><span data-stu-id="510b1-114">If the DVD-Video is playing in reverse mode when this method is called, and the decoder supports reverse frame stepping, then the frame stepping is done in reverse.</span></span>

 

 



