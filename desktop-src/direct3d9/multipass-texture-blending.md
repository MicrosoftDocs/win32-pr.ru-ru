---
description: Приложения Direct3D могут создавать различные специальные эффекты путем применения различных текстур к примитиву в процессе многопроходной отрисовки.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Многопроходное смешение текстур (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139967"
---
# <a name="multipass-texture-blending-direct3d-9"></a><span data-ttu-id="3ad5e-103">Многопроходное смешение текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3ad5e-103">Multipass Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="3ad5e-104">Приложения Direct3D могут создавать различные специальные эффекты путем применения различных текстур к примитиву в процессе многопроходной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-104">Direct3D applications can achieve numerous special effects by applying various textures to a primitive over the course of multiple rendering passes.</span></span> <span data-ttu-id="3ad5e-105">Общий термин для этого — многопроходное наложение текстуры.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-105">The common term for this is multipass texture blending.</span></span> <span data-ttu-id="3ad5e-106">Обычно многопроходное наложение текстуры используется для эмуляции эффектов сложных моделей освещения и затенения путем применения нескольких цветов из нескольких различных текстур.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-106">A typical use for multipass texture blending is to emulate the effects of complex lighting and shading models by applying multiple colors from several different textures.</span></span> <span data-ttu-id="3ad5e-107">Одно такое приложение называется Сопоставление освещения.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-107">One such application is called light mapping.</span></span> <span data-ttu-id="3ad5e-108">Дополнительные сведения см. в разделе [светлое сопоставление с текстурами (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="3ad5e-108">For more information, see [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

> [!Note]  
> <span data-ttu-id="3ad5e-109">Некоторые устройства способны применять несколько текстур к примитивам за один проход.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-109">Some devices are capable of applying multiple textures to primitives in a single pass.</span></span> <span data-ttu-id="3ad5e-110">Дополнительные сведения см. в разделе [смешение текстур (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="3ad5e-110">For details, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

 

<span data-ttu-id="3ad5e-111">Если оборудование пользователя не поддерживает множественное наложение текстур, приложение может использовать многопроходное наложение текстур для достижения тех же визуальных эффектов.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-111">If the user's hardware does not support multiple texture blending, your application can use multipass texture blending to achieve the same visual effects.</span></span> <span data-ttu-id="3ad5e-112">Тем не менее приложение не может поддерживать ту же частоту кадров, которая достижима при использовании множественного наложения текстур.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-112">However, the application cannot sustain the frame rates that are possible when using multiple texture blending.</span></span>

<span data-ttu-id="3ad5e-113">Для выполнения многопроходного смешения текстур в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-113">To perform multipass texture blending in a C/C++ application.</span></span>

1.  <span data-ttu-id="3ad5e-114">Задайте текстуру на этапе текстуры 0, вызвав метод [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="3ad5e-114">Set a texture in texture stage 0 by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span>
2.  <span data-ttu-id="3ad5e-115">Выберите требуемый цвет и альфа-смешение аргументов и операций с помощью метода [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="3ad5e-115">Select the desired color and alpha blending arguments and operations with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="3ad5e-116">Параметры по умолчанию хорошо подходят для многопроходного наложения текстур.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-116">The default settings are well-suited for multipass texture blending.</span></span>
3.  <span data-ttu-id="3ad5e-117">Отрисовка соответствующих объектов в сцене.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-117">Render the appropriate objects in the scene.</span></span>
4.  <span data-ttu-id="3ad5e-118">Установите следующую текстуру на этапе текстуры 0.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-118">Set the next texture in texture stage 0.</span></span>
5.  <span data-ttu-id="3ad5e-119">Задайте для параметров \_ рендеринга D3DRS сркбленд и D3DRS \_ дестбленд, чтобы при необходимости изменить исходные и целевые Коэффициенты смешения.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-119">Set the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states to adjust the source and destination blending factors as needed.</span></span> <span data-ttu-id="3ad5e-120">Система накладывает новые текстуры на существующие пиксели на целевой поверхности отрисовки в соответствии с этими параметрами.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-120">The system blends the new textures with the existing pixels in the render-target surface according to these parameters.</span></span>
6.  <span data-ttu-id="3ad5e-121">Повторите шаги 3, 4 и 5 для всех необходимых текстур.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-121">Repeat Steps 3, 4, and 5 with as many textures as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ad5e-122">См. также</span><span class="sxs-lookup"><span data-stu-id="3ad5e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ad5e-123">Смешение текстур</span><span class="sxs-lookup"><span data-stu-id="3ad5e-123">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
