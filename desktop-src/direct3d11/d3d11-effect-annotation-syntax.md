---
title: Синтаксис аннотации (Direct3D 11)
description: Заметка — это определяемая пользователем часть данных, объявленная с синтаксисом, описанным в этом разделе.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9583dafd3e1fb314ae6ac9e53d609bebc74a030
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987538"
---
# <a name="annotation-syntax-direct3d-11"></a><span data-ttu-id="f7f09-103">Синтаксис аннотации (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="f7f09-103">Annotation Syntax (Direct3D 11)</span></span>

<span data-ttu-id="f7f09-104">Заметка — это определяемая пользователем часть данных, объявленная с синтаксисом, описанным в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="f7f09-104">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span>



| <span data-ttu-id="f7f09-105"><Значение имени *типа данных*   =  ; *...* ; ></span><span class="sxs-lookup"><span data-stu-id="f7f09-105"><*DataType* *Name* = *Value*; *...* ;></span></span> |
|----------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="f7f09-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7f09-106">Parameters</span></span>



| <span data-ttu-id="f7f09-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="f7f09-107">Item</span></span>                                                                                                   | <span data-ttu-id="f7f09-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f7f09-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f09-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Заданий*</span><span class="sxs-lookup"><span data-stu-id="f7f09-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="f7f09-110">\[в \] типе данных, который включает любой [скалярный тип HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) , а также [строковый тип](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span><span class="sxs-lookup"><span data-stu-id="f7f09-110">\[in\] The data type, which includes any [scalar HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) type as well as the [string type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span></span><br/> |
| <span data-ttu-id="f7f09-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*</span><span class="sxs-lookup"><span data-stu-id="f7f09-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="f7f09-112">\[в \] строке ASCII, представляющей имя заметки.</span><span class="sxs-lookup"><span data-stu-id="f7f09-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="f7f09-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Значений*</span><span class="sxs-lookup"><span data-stu-id="f7f09-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="f7f09-114">\[в \] начальном значении заметки.</span><span class="sxs-lookup"><span data-stu-id="f7f09-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="f7f09-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="f7f09-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="f7f09-116">\[в \] дополнительных аннотациях (пар "имя-значение").</span><span class="sxs-lookup"><span data-stu-id="f7f09-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="f7f09-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7f09-117">Remarks</span></span>

<span data-ttu-id="f7f09-118">В угловые скобки можно добавить несколько аннотаций, каждое из которых отделяется точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="f7f09-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="f7f09-119">Интерфейсы API платформы эффектов распознавать заметки в глобальных переменных. все остальные заметки игнорируются.</span><span class="sxs-lookup"><span data-stu-id="f7f09-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="f7f09-120">Например, .</span><span class="sxs-lookup"><span data-stu-id="f7f09-120">Example</span></span>

<span data-ttu-id="f7f09-121">Вот несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="f7f09-121">Here are some examples.</span></span>


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a><span data-ttu-id="f7f09-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f7f09-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7f09-123">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="f7f09-123">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="f7f09-124">Синтаксис переменной Effect</span><span class="sxs-lookup"><span data-stu-id="f7f09-124">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

