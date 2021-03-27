---
title: Динамическая компоновка
description: Разработчики графики иногда создают крупные шейдеры общего назначения, которые могут использоваться множеством элементов сцены.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776397"
---
# <a name="dynamic-linking"></a><span data-ttu-id="d4364-103">Динамическая компоновка</span><span class="sxs-lookup"><span data-stu-id="d4364-103">Dynamic Linking</span></span>

<span data-ttu-id="d4364-104">Разработчики графики иногда создают крупные шейдеры общего назначения, которые могут использоваться множеством элементов сцены.</span><span class="sxs-lookup"><span data-stu-id="d4364-104">Graphics developers sometimes create large, general-purpose shaders that can be used by a wide variety of scene items.</span></span> <span data-ttu-id="d4364-105">Во время выполнения шейдер условно выполняет код, соответствующий данной ситуации.</span><span class="sxs-lookup"><span data-stu-id="d4364-105">At runtime, the shader conditionally runs code appropriate for the given situation.</span></span> <span data-ttu-id="d4364-106">К сожалению, эти крупные шейдеры общего назначения используют регистры общего назначения (GPRs) неэффективно и могут быть намного медленнее, чем небольшие, более целевые шейдеры.</span><span class="sxs-lookup"><span data-stu-id="d4364-106">Unfortunately, these large, general-purpose shaders use general-purpose registers (GPRs) inefficiently, and can be much slower than smaller, more targeted shaders.</span></span>

<span data-ttu-id="d4364-107">Модель шейдеров 5 решает эту проблему с производительностью, представляя динамическое связывание шейдера.</span><span class="sxs-lookup"><span data-stu-id="d4364-107">Shader model 5 addresses this performance problem by introducing dynamic shader linking.</span></span> <span data-ttu-id="d4364-108">Динамическая компоновка разделяет фрагменты кода шейдера с помощью интерфейсов и виртуальных функций и позволяет приложению выбрать фрагмент для использования во время рисования.</span><span class="sxs-lookup"><span data-stu-id="d4364-108">Dynamic linking separates shader code fragments by using interfaces and virtual functions and allows the application to select the fragment to use at draw time.</span></span> <span data-ttu-id="d4364-109">Это повышает производительность, привязывая только необходимый код шейдера, а не весь крупный шейдер общего назначения.</span><span class="sxs-lookup"><span data-stu-id="d4364-109">This improves performance by binding only the shader code needed and not the entire large, general-purpose shader.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4364-110">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="d4364-110">In This Section</span></span>



| <span data-ttu-id="d4364-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="d4364-111">Item</span></span>                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="d4364-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d4364-112">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4364-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Хранение переменных и типов для использования шейдерами](storing-variables-and-types-for-shaders-to-share.md)</span><span class="sxs-lookup"><span data-stu-id="d4364-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Storing Variables and Types for Shaders to Share](storing-variables-and-types-for-shaders-to-share.md)</span></span><br/> | <span data-ttu-id="d4364-114">Описывает объект компоновки класса для хранения переменных и типов, которые могут совместно использоваться несколькими шейдерами.</span><span class="sxs-lookup"><span data-stu-id="d4364-114">Describes the class linkage object for storing variables and types that multiple shaders can share.</span></span><br/> |
| <span data-ttu-id="d4364-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Интерфейсы и классы](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span><span class="sxs-lookup"><span data-stu-id="d4364-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces and Classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span></span><br/>                                                                                                         | <span data-ttu-id="d4364-116">Описывает использование интерфейсов и классов HLSL для реализации динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="d4364-116">Describes using HLSL interfaces and classes to implement dynamic linking.</span></span><br/>                           |
| <span data-ttu-id="d4364-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Ограничения использования интерфейса](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span><span class="sxs-lookup"><span data-stu-id="d4364-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Interface Usage Restrictions](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span></span><br/>                                                                            | <span data-ttu-id="d4364-118">Описывает ограничения на использование интерфейсов в коде шейдера.</span><span class="sxs-lookup"><span data-stu-id="d4364-118">Describes restrictions on the use of interfaces in shader code.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="d4364-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d4364-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4364-120">HLSL</span><span class="sxs-lookup"><span data-stu-id="d4364-120">HLSL</span></span>](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





