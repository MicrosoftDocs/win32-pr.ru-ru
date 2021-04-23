---
description: Заметка — это определяемая пользователем часть данных, объявленная с помощью следующего синтаксиса.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Синтаксис аннотации (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896534"
---
# <a name="annotation-syntax-direct3d-10"></a><span data-ttu-id="33a35-103">Синтаксис аннотации (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="33a35-103">Annotation Syntax (Direct3D 10)</span></span>

<span data-ttu-id="33a35-104">Заметка — это определяемая пользователем часть данных, объявленная с помощью следующего синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="33a35-104">An annotation is a user-defined piece of information, declared with the following syntax.</span></span>



| <span data-ttu-id="33a35-105"><*Имя типа данных*   =  ;...; ></span><span class="sxs-lookup"><span data-stu-id="33a35-105"><*DataType* *Name* = *Value*; ... ;></span></span> |
|--------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="33a35-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="33a35-106">Parameters</span></span>



| <span data-ttu-id="33a35-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="33a35-107">Item</span></span>                                                                                                   | <span data-ttu-id="33a35-108">Описание</span><span class="sxs-lookup"><span data-stu-id="33a35-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a35-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Заданий*</span><span class="sxs-lookup"><span data-stu-id="33a35-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="33a35-110">\[в \] типе данных, который включает любой [скалярный тип HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) , а также [строковый тип](../direct3dhlsl/dx-graphics-hlsl-scalar.md).</span><span class="sxs-lookup"><span data-stu-id="33a35-110">\[in\] The data type, which includes any [scalar HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) type as well as the [string type](../direct3dhlsl/dx-graphics-hlsl-scalar.md).</span></span><br/> |
| <span data-ttu-id="33a35-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*</span><span class="sxs-lookup"><span data-stu-id="33a35-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="33a35-112">\[в \] строке ASCII, представляющей имя заметки.</span><span class="sxs-lookup"><span data-stu-id="33a35-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="33a35-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Значений*</span><span class="sxs-lookup"><span data-stu-id="33a35-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="33a35-114">\[в \] начальном значении заметки.</span><span class="sxs-lookup"><span data-stu-id="33a35-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="33a35-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="33a35-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="33a35-116">\[в \] дополнительных аннотациях (пар "имя-значение").</span><span class="sxs-lookup"><span data-stu-id="33a35-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="33a35-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33a35-117">Remarks</span></span>

<span data-ttu-id="33a35-118">В угловые скобки можно добавить несколько аннотаций, каждое из которых отделяется точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="33a35-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="33a35-119">Интерфейсы API платформы эффектов распознавать заметки в глобальных переменных. все остальные заметки игнорируются.</span><span class="sxs-lookup"><span data-stu-id="33a35-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="33a35-120">Пример</span><span class="sxs-lookup"><span data-stu-id="33a35-120">Example</span></span>

<span data-ttu-id="33a35-121">Вот несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="33a35-121">Here are some examples.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="33a35-122">См. также</span><span class="sxs-lookup"><span data-stu-id="33a35-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33a35-123">Синтаксис переменной Effect</span><span class="sxs-lookup"><span data-stu-id="33a35-123">Effect Variable Syntax</span></span>](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
