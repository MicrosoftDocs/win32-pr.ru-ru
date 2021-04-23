---
description: Приложения C++ могут использовать альфа-тестирование для управления зазаписью пикселей на поверхность визуализации.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Состояние тестирования Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710769"
---
# <a name="alpha-testing-state-direct3d-9"></a><span data-ttu-id="19260-103">Состояние тестирования Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="19260-103">Alpha Testing State (Direct3D 9)</span></span>

<span data-ttu-id="19260-104">Приложения C++ могут использовать альфа-тестирование для управления зазаписью пикселей на поверхность визуализации.</span><span class="sxs-lookup"><span data-stu-id="19260-104">C++ applications can use alpha testing to control when pixels are written to the render-target surface.</span></span> <span data-ttu-id="19260-105">Используя состояние рендеринга [**D3DRS \_ алфатестенабле**](./d3drenderstatetype.md) , приложение устанавливает текущее устройство Direct3D, чтобы оно проводило тестирование каждого пикселя в соответствии с тестовой функцией Alpha.</span><span class="sxs-lookup"><span data-stu-id="19260-105">By using the [**D3DRS\_ALPHATESTENABLE**](./d3drenderstatetype.md) render state, your application sets the current Direct3D device so that it tests each pixel according to an alpha test function.</span></span> <span data-ttu-id="19260-106">Если тест выполнен, точка записывается на поверхность.</span><span class="sxs-lookup"><span data-stu-id="19260-106">If the test succeeds, the pixel is written to the surface.</span></span> <span data-ttu-id="19260-107">В противном случае Direct3D игнорирует Пиксель.</span><span class="sxs-lookup"><span data-stu-id="19260-107">If it does not, Direct3D ignores the pixel.</span></span> <span data-ttu-id="19260-108">Выберите функцию тестирования Alpha с состоянием рендеринга **D3DRS \_ алфафунк** .</span><span class="sxs-lookup"><span data-stu-id="19260-108">Select the alpha test function with the **D3DRS\_ALPHAFUNC** render state.</span></span> <span data-ttu-id="19260-109">Приложение может установить ссылку на альфа-значение для всех пикселей для сравнения с помощью состояния визуализации **D3DRS \_ алфареф** .</span><span class="sxs-lookup"><span data-stu-id="19260-109">Your application can set a reference alpha value for all pixels to compare against by using the **D3DRS\_ALPHAREF** render state.</span></span>

<span data-ttu-id="19260-110">Наиболее распространенным применением альфа-тестирования является повышение производительности при растрировании объектов, которые почти прозрачны.</span><span class="sxs-lookup"><span data-stu-id="19260-110">The most common use for alpha testing is to improve performance when rasterizing objects that are nearly transparent.</span></span> <span data-ttu-id="19260-111">Если растрирование цветовых данных является более прозрачным, чем цвет в заданном пикселе (D3DPCMPCAPS \_ загруженность), то записывается пиксель.</span><span class="sxs-lookup"><span data-stu-id="19260-111">If the color data being rasterized is more opaque than the color at a given pixel (D3DPCMPCAPS\_GREATEREQUAL), then the pixel is written.</span></span> <span data-ttu-id="19260-112">В противном случае средство программной прорисовки полностью игнорирует пиксел, сохраняя обработку, необходимую для смешения двух цветов.</span><span class="sxs-lookup"><span data-stu-id="19260-112">Otherwise, the rasterizer ignores the pixel altogether, saving the processing required to blend the two colors.</span></span> <span data-ttu-id="19260-113">В следующем примере кода проверяется, поддерживается ли данная функция сравнения, и, если это так, задаются параметры функции сравнения, необходимые для повышения производительности во время отрисовки.</span><span class="sxs-lookup"><span data-stu-id="19260-113">The following code example checks if a given comparison function is supported and, if so, it sets the comparison function parameters required to improve performance during rendering.</span></span>


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



<span data-ttu-id="19260-114">Не все оборудование поддерживает все функции для тестирования альфа-версии.</span><span class="sxs-lookup"><span data-stu-id="19260-114">Not all hardware supports all alpha-testing features.</span></span> <span data-ttu-id="19260-115">Можно проверить возможности устройства, вызвав метод [**IDirect3D9:: жетдевицекапс**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="19260-115">You can check the device capabilities by calling the [**IDirect3D9::GetDeviceCaps**](/windows/desktop/api) method.</span></span> <span data-ttu-id="19260-116">После получения возможностей устройства проверьте элемент Алфакмпкапс связанной структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для нужной функции сравнения.</span><span class="sxs-lookup"><span data-stu-id="19260-116">After retrieving the device capabilities, check the associated [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's AlphaCmpCaps member for the desired comparison function.</span></span> <span data-ttu-id="19260-117">Если член Алфакмпкапс содержит только \_ функцию D3DPCMPCAPS Always или только D3DPCMPCAPS \_ , драйвер не поддерживает альфа-тесты.</span><span class="sxs-lookup"><span data-stu-id="19260-117">If the AlphaCmpCaps member contains only the D3DPCMPCAPS\_ALWAYS capability or only the D3DPCMPCAPS\_NEVER capability, the driver does not support alpha tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19260-118">См. также</span><span class="sxs-lookup"><span data-stu-id="19260-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19260-119">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="19260-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
