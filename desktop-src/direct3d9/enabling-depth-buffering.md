---
description: 'После создания буфера глубины, как описано в разделе Создание буфера глубины (Direct3D 9), можно включить буферизацию глубины, вызвав метод IDirect3DDevice9:: Сетрендерстате.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Включение буферизации глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341425"
---
# <a name="enabling-depth-buffering-direct3d-9"></a><span data-ttu-id="0f948-103">Включение буферизации глубины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0f948-103">Enabling Depth Buffering (Direct3D 9)</span></span>

<span data-ttu-id="0f948-104">После создания буфера глубины, как описано в разделе [Создание буфера глубины (Direct3D 9)](creating-a-depth-buffer.md), можно включить буферизацию глубины, вызвав метод [**IDirect3DDevice9:: сетрендерстате**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0f948-104">After you create a depth buffer, as described in [Creating a Depth Buffer (Direct3D 9)](creating-a-depth-buffer.md), you enable depth buffering by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="0f948-105">Установите \_ состояние отрисовки D3DRS зенабле, чтобы включить буферизацию глубины.</span><span class="sxs-lookup"><span data-stu-id="0f948-105">Set the D3DRS\_ZENABLE render state to enable depth-buffering.</span></span> <span data-ttu-id="0f948-106">Используйте член D3DZB \_ true перечисляемого типа [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) (или **true**), чтобы включить z-буферизацию, D3DZB \_ усев для включения w-Buffering или D3DZB \_ false (или **false**) для отключения буферизации глубины.</span><span class="sxs-lookup"><span data-stu-id="0f948-106">Use the D3DZB\_TRUE member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type (or **TRUE**) to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE (or **FALSE**) to disable depth buffering.</span></span>

> [!Note]  
> <span data-ttu-id="0f948-107">Чтобы использовать w-Buffering, приложение должно установить соответствующую матрицу проекции, даже если она не использует конвейер преобразования Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0f948-107">To use w-buffering, your application must set a compliant projection matrix even if it doesn't use the Direct3D transformation pipeline.</span></span> <span data-ttu-id="0f948-108">Сведения о предоставлении соответствующей матрицы проекции см. [в разделе матрица проекций, ориентированная на W](projection-transform.md)</span><span class="sxs-lookup"><span data-stu-id="0f948-108">For information about providing an appropriate projection matrix, see [A W-Friendly Projection Matrix](projection-transform.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0f948-109">См. также</span><span class="sxs-lookup"><span data-stu-id="0f948-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f948-110">Буферы глубины</span><span class="sxs-lookup"><span data-stu-id="0f948-110">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
