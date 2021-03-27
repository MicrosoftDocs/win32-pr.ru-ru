---
title: Как экземпляр шейдера Geometry
description: Создание экземпляров шейдера Geometry позволяет выполнять несколько выполнений одного шейдера Geometry для каждого примитива.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7858de7d8526a9468d3ebd0a07d57777983a66db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996787"
---
# <a name="how-to-instance-a-geometry-shader"></a><span data-ttu-id="75027-103">Как выполнить экземпляр шейдера Geometry</span><span class="sxs-lookup"><span data-stu-id="75027-103">How To: Instance a Geometry Shader</span></span>

<span data-ttu-id="75027-104">Создание экземпляров шейдера Geometry позволяет выполнять несколько выполнений одного шейдера Geometry для каждого примитива.</span><span class="sxs-lookup"><span data-stu-id="75027-104">Geometry shader instancing allows multiple executions of the same geometry shader to be executed per primitive.</span></span> <span data-ttu-id="75027-105">Чтобы создать экземпляр шейдера Geometry, добавьте атрибут экземпляра в основную функцию шейдера и задайте параметр индекса экземпляра в теле функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="75027-105">To instance a geometry shader, add an instance attribute to the main shader function and identify an instance index parameter in the shader function body.</span></span>

<span data-ttu-id="75027-106">Для экземпляра шейдера Geometry:</span><span class="sxs-lookup"><span data-stu-id="75027-106">To Instance a Geometry Shader:</span></span>

1.  <span data-ttu-id="75027-107">Добавьте [атрибут экземпляра](sm5-attributes-instance.md) в функцию main.</span><span class="sxs-lookup"><span data-stu-id="75027-107">Add the [instance attribute](sm5-attributes-instance.md) to the main function.</span></span>

    ```
    [instance(24)]
    ```

    

    <span data-ttu-id="75027-108">Определяет количество экземпляров (не более 32), которые будут выполняться для каждого примитива.</span><span class="sxs-lookup"><span data-stu-id="75027-108">This defines the number of instances (a maximum of 32) to be run for each primitive.</span></span>

2.  <span data-ttu-id="75027-109">Присоедините системное значение [SV \_ гсинстанцеид](sv-gsinstanceid.md) к переменной в списке параметров функции, которая может использоваться для контроля идентификатора выполняемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="75027-109">Attach the [SV\_GSInstanceID](sv-gsinstanceid.md) system value to a variable in the function parameter list that can be used to track the ID of the instance being executed.</span></span>
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  <span data-ttu-id="75027-110">Скомпилируйте и создайте шейдер так же, как любой другой шейдер геометрии.</span><span class="sxs-lookup"><span data-stu-id="75027-110">Compile and create the shader just as you would any other geometry shader.</span></span>

<span data-ttu-id="75027-111">Другие сведения включают:</span><span class="sxs-lookup"><span data-stu-id="75027-111">Other details include:</span></span>

-   <span data-ttu-id="75027-112">Максимальное число экземпляров — 32.</span><span class="sxs-lookup"><span data-stu-id="75027-112">The maximum instance count is 32.</span></span>
-   <span data-ttu-id="75027-113">Максимальное число вершин — это максимальное число вершин на экземпляр.</span><span class="sxs-lookup"><span data-stu-id="75027-113">The maximum vertex count is a per-instance maximum vertex count.</span></span>
-   <span data-ttu-id="75027-114">Вызов каждого экземпляра (как и любой вызов шейдера Geometry) увеличивает число вызовов и создает неявный Рестартстрип ().</span><span class="sxs-lookup"><span data-stu-id="75027-114">Each instance invocation (like any geometry shader invocation) increases the invocation count and generates an implicit RestartStrip().</span></span>

## <a name="related-topics"></a><span data-ttu-id="75027-115">См. также</span><span class="sxs-lookup"><span data-stu-id="75027-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75027-116">Функции шейдера Geometry</span><span class="sxs-lookup"><span data-stu-id="75027-116">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




