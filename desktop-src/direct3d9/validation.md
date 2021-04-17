---
description: Проверка выполняется во время компиляции результата. Чтобы проверить текущий метод, укажите значение NULL в качестве обрабатываемого метода.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Проверка (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710603"
---
# <a name="validation-direct3d-9"></a><span data-ttu-id="6db13-104">Проверка (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6db13-104">Validation (Direct3D 9)</span></span>

<span data-ttu-id="6db13-105">Проверка выполняется во время компиляции результата.</span><span class="sxs-lookup"><span data-stu-id="6db13-105">Validation is performed during the effect compile.</span></span> <span data-ttu-id="6db13-106">Чтобы проверить текущий метод, укажите **значение NULL** в качестве обрабатываемого метода.</span><span class="sxs-lookup"><span data-stu-id="6db13-106">To validate the current technique, specify **NULL** as the technique handle to be validated.</span></span>

<span data-ttu-id="6db13-107">Проверка завершится ошибкой для следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="6db13-107">Validation will fail for any of the following:</span></span>

-   <span data-ttu-id="6db13-108">Значение, если указанный обработчик методики не существует.</span><span class="sxs-lookup"><span data-stu-id="6db13-108">If the specified technique handle does not exist.</span></span>
-   <span data-ttu-id="6db13-109">Значение, если приложение любого состояния на любом этапе выполнения метода завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6db13-109">If the application of any state in any pass of the technique fails.</span></span>
-   <span data-ttu-id="6db13-110">Если проверка устройства завершается сбоем после применения всех состояний на любом этапе приема.</span><span class="sxs-lookup"><span data-stu-id="6db13-110">If device validation fails after the application of all the states in any pass of the technique.</span></span>
-   <span data-ttu-id="6db13-111">Если в качестве состояния воздействия PIXELSHADER или ВЕРТЕКСШАДЕР назначены недопустимые шейдеры на любом этапе приема.</span><span class="sxs-lookup"><span data-stu-id="6db13-111">If the PIXELSHADER or VERTEXSHADER effect states are assigned invalid shaders in any pass of the technique.</span></span>
-   <span data-ttu-id="6db13-112">Если устройства с ограничениями не поддерживают сопоставление кубов, а для состояния эффекты текстуры назначается значение типа Текстурекубе при любом прохождении метода.</span><span class="sxs-lookup"><span data-stu-id="6db13-112">If the device caps do not support cube mapping, and a TEXTURE effect state is assigned a value of type textureCUBE in any pass of the technique.</span></span>
-   <span data-ttu-id="6db13-113">Если устройства с ограничениями не поддерживают сопоставление томов, а для состояния эффекты текстуры назначено значение типа texture3D при любом прохождении метода.</span><span class="sxs-lookup"><span data-stu-id="6db13-113">If the device caps do not support volume mapping and a TEXTURE effect state is assigned a value of type texture3D in any pass of the technique.</span></span>

<span data-ttu-id="6db13-114">Дополнительные сведения см. в разделе [состояния эффектов (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="6db13-114">For more information, see [Effect States (Direct3D 9)](effect-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6db13-115">См. также</span><span class="sxs-lookup"><span data-stu-id="6db13-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6db13-116">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="6db13-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



