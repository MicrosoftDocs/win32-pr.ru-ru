---
title: Сбой прорисовки D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Сбой вызова Draw объектом прорисовки
keywords:
- Сбой прорисовки D1109 Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793710"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="9baee-104">D1109: сбой прорисовки</span><span class="sxs-lookup"><span data-stu-id="9baee-104">D1109: Draw Failure</span></span>

<span data-ttu-id="9baee-105">Вызов Draw невыполненным \[ *ресурсом* целевого объекта прорисовки \] .</span><span class="sxs-lookup"><span data-stu-id="9baee-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="9baee-106">Теги \[ *TAG1*, *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="9baee-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="9baee-107">Заполнители</span><span class="sxs-lookup"><span data-stu-id="9baee-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="9baee-108"><span id="resource"></span><span id="RESOURCE"></span>*ресурсов*</span><span class="sxs-lookup"><span data-stu-id="9baee-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="9baee-109">Адрес целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="9baee-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="9baee-110"><span id="tag1"></span><span id="TAG1"></span>*TAG1*</span><span class="sxs-lookup"><span data-stu-id="9baee-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="9baee-111">Первое значение тега (Дополнительные сведения см. в [**сеттагс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).</span><span class="sxs-lookup"><span data-stu-id="9baee-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="9baee-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="9baee-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="9baee-113">Второе значение тега (Дополнительные сведения см. в [**сеттагс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).</span><span class="sxs-lookup"><span data-stu-id="9baee-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="9baee-114">Уровень ошибки</span><span class="sxs-lookup"><span data-stu-id="9baee-114">Error Level</span></span> | <span data-ttu-id="9baee-115">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="9baee-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="9baee-116">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="9baee-116">Possible Causes</span></span>

<span data-ttu-id="9baee-117">Вызов рисования может завершиться неудачей по многим причинам.</span><span class="sxs-lookup"><span data-stu-id="9baee-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="9baee-118">Дополнительные сведения см. в документации по пакету SDK для Direct2D для метода, который завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9baee-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 