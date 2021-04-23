---
description: Текущее оборудование не обязательно реализует все функции, которые обеспечивает интерфейс Direct3D. Приложение должно проверять оборудование пользователя и соответствующим образом настраивать его стратегии отрисовки.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Рекомендации по оборудованию для текстурирования (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894021"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a><span data-ttu-id="e832d-104">Рекомендации по оборудованию для текстурирования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e832d-104">Hardware Considerations for Texturing (Direct3D 9)</span></span>

<span data-ttu-id="e832d-105">Текущее оборудование не обязательно реализует все функции, которые обеспечивает интерфейс Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e832d-105">Current hardware does not necessarily implement all the functionality that the Direct3D interface enables.</span></span> <span data-ttu-id="e832d-106">Приложение должно проверять оборудование пользователя и соответствующим образом настраивать его стратегии отрисовки.</span><span class="sxs-lookup"><span data-stu-id="e832d-106">Your application must test user hardware and adjust its rendering strategies accordingly.</span></span>

<span data-ttu-id="e832d-107">Многие трехмерные карты ускорителя не поддерживают рассеянные значения в качестве аргументов для элементов наложения.</span><span class="sxs-lookup"><span data-stu-id="e832d-107">Many 3D accelerator cards do not support diffuse iterated values as arguments to blending units.</span></span> <span data-ttu-id="e832d-108">Однако приложение может ввести итеративные данные о цвете при выполнении смешения текстур.</span><span class="sxs-lookup"><span data-stu-id="e832d-108">However, your application can introduce iterated color data when it performs texture blending.</span></span>

<span data-ttu-id="e832d-109">На некоторых трехмерных устройствах может не быть этапа смешения, связанного с первой текстурой.</span><span class="sxs-lookup"><span data-stu-id="e832d-109">Some 3D hardware may not have a blending stage associated with the first texture.</span></span> <span data-ttu-id="e832d-110">На этих адаптерах приложение должно выполнять смешивание во второй и третьей стадиях текстуры в наборе текущих текстур.</span><span class="sxs-lookup"><span data-stu-id="e832d-110">On these adapters, your application must perform blending in the second and third texture stages in the set of current textures.</span></span>

<span data-ttu-id="e832d-111">Из-за ограничений в большинстве современных аппаратных средств некоторые видеоадаптеры могут выполнять интерполяцию трилинейной mipmap через интерфейс смешивания текстур, предлагаемый [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="e832d-111">Because of limitations in much of today's hardware, few display adapters can perform trilinear mipmap interpolation through the multiple texture blending interface offered by [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span> <span data-ttu-id="e832d-112">Приложение может использовать смешение многопроходных текстур для достижения одних и тех же эффектов или переходить к \_ режиму фильтра D3DTEXF Point mipmap, который широко поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e832d-112">Your application can use multipass texture blending to achieve the same effects, or degrade to the D3DTEXF\_POINT mipmap filter mode, which is widely supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e832d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e832d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e832d-114">Текстуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="e832d-114">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
