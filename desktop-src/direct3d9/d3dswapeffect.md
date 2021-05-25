---
description: Определяет эффекты переключения.
ms.assetid: 522a5f71-3ad9-4cfc-a899-e25b9b721b1b
title: Перечисление D3DSWAPEFFECT (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSWAPEFFECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 58354e35ca8456f6fde57d2f2567a6b6a202f6d7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343039"
---
# <a name="d3dswapeffect-enumeration"></a><span data-ttu-id="77e28-103">Перечисление D3DSWAPEFFECT</span><span class="sxs-lookup"><span data-stu-id="77e28-103">D3DSWAPEFFECT enumeration</span></span>

<span data-ttu-id="77e28-104">Определяет эффекты переключения.</span><span class="sxs-lookup"><span data-stu-id="77e28-104">Defines swap effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e28-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77e28-105">Syntax</span></span>

```cpp
typedef enum D3DSWAPEFFECT { 
  D3DSWAPEFFECT_DISCARD      = 1,
  D3DSWAPEFFECT_FLIP         = 2,
  D3DSWAPEFFECT_COPY         = 3,
  D3DSWAPEFFECT_OVERLAY      = 4,
  D3DSWAPEFFECT_FLIPEX       = 5,
  D3DSWAPEFFECT_FORCE_DWORD  = 0xFFFFFFFF
} D3DSWAPEFFECT, *LPD3DSWAPEFFECT;
```

## <a name="constants"></a><span data-ttu-id="77e28-106">Константы</span><span class="sxs-lookup"><span data-stu-id="77e28-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="77e28-107"><span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT \_ отбросить**</span><span class="sxs-lookup"><span data-stu-id="77e28-107"><span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT\_DISCARD**</span></span>
</dt> <dd>

<span data-ttu-id="77e28-108">При создании цепочки буферов с помощью D3DSWAPEFFECT \_ отражения или D3DSWAPEFFECT \_ Copy среда выполнения гарантирует, что операция повторной отправки [**IDirect3DDevice9::P**](/windows/desktop/api) не будет влиять на содержимое всех задних буферов.</span><span class="sxs-lookup"><span data-stu-id="77e28-108">When a swap chain is created with a swap effect of D3DSWAPEFFECT\_FLIP or D3DSWAPEFFECT\_COPY, the runtime will guarantee that an [**IDirect3DDevice9::Present**](/windows/desktop/api) operation will not affect the content of any of the back buffers.</span></span> <span data-ttu-id="77e28-109">К сожалению, такая гарантия может включать значительный объем видеопамяти или обработку заголовков, особенно при реализации семантики отражения для оконной цепочки буферов или семантики копирования для всей цепочки буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="77e28-109">Unfortunately, meeting this guarantee can involve substantial video memory or processing overheads, especially when implementing flip semantics for a windowed swap chain or copy semantics for a full-screen swap chain.</span></span> <span data-ttu-id="77e28-110">Приложение может использовать D3DSWAPEFFECT \_ Отмена переключения, чтобы избежать этих перестановок и включить драйвер экрана для выбора наиболее эффективной методики представления цепочки буферов.</span><span class="sxs-lookup"><span data-stu-id="77e28-110">An application may use the D3DSWAPEFFECT\_DISCARD swap effect to avoid these overheads and to enable the display driver to select the most efficient presentation technique for the swap chain.</span></span> <span data-ttu-id="77e28-111">Это также единственный результат переключения, который может использоваться при указании значения, отличного от D3DMULTISAMPLE \_ None, для элемента мултисамплетипе в [**\_ параметрах D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="77e28-111">This is also the only swap effect that may be used when specifying a value other than D3DMULTISAMPLE\_NONE for the MultiSampleType member of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="77e28-112">Как и цепочка подкачки, использующая \_ перелистывание D3DSWAPEFFECT, цепочка подкачки, использующая D3DSWAPEFFECT \_ Discard, может включать несколько задних буферов, к которым можно получить доступ с помощью [**IDirect3DDevice9:: жетбаккбуффер**](/windows/desktop/api) или [**IDirect3DSwapChain9:: жетбаккбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer).</span><span class="sxs-lookup"><span data-stu-id="77e28-112">Like a swap chain that uses D3DSWAPEFFECT\_FLIP, a swap chain that uses D3DSWAPEFFECT\_DISCARD might include more than one back buffer, any of which may be accessed using [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) or [**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer).</span></span> <span data-ttu-id="77e28-113">Цепочка буфера обмена лучше предусмотрено как очередь, в которой 0 всегда индексирует задний буфер, который будет отображаться в следующей операции, и из которого удаляются буферы, когда они отображаются.</span><span class="sxs-lookup"><span data-stu-id="77e28-113">The swap chain is best envisaged as a queue in which 0 always indexes the back buffer that will be displayed by the next Present operation and from which buffers are discarded when they have been displayed.</span></span>

<span data-ttu-id="77e28-114">Приложение, использующее этот результат переключения, не может делать никаких предположений о содержимом отклоненного заднего буфера и, следовательно, обновлять весь задний буфер перед вызовом текущей операции, которая будет отображать его.</span><span class="sxs-lookup"><span data-stu-id="77e28-114">An application that uses this swap effect cannot make any assumptions about the contents of a discarded back buffer and should therefore update an entire back buffer before invoking a Present operation that would display it.</span></span> <span data-ttu-id="77e28-115">Хотя это не применяется принудительно, отладочная версия среды выполнения перезаписывает содержимое удаленных буферов случайными данными, чтобы позволить разработчикам проверить, правильно ли обновляются все поверхности заднего буфера в своих приложениях.</span><span class="sxs-lookup"><span data-stu-id="77e28-115">Although this is not enforced, the debug version of the runtime will overwrite the contents of discarded back buffers with random data to enable developers to verify that their applications are updating the entire back buffer surfaces correctly.</span></span>

</dd> <dt>

<span data-ttu-id="77e28-116"><span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**Перевернуть D3DSWAPEFFECT \_**</span><span class="sxs-lookup"><span data-stu-id="77e28-116"><span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT\_FLIP**</span></span>
</dt> <dd>

<span data-ttu-id="77e28-117">Цепочка буфера обмена может включать несколько задних буферов и лучше предусмотрено в качестве циклической очереди, включающей передний буфер.</span><span class="sxs-lookup"><span data-stu-id="77e28-117">The swap chain might include multiple back buffers and is best envisaged as a circular queue that includes the front buffer.</span></span> <span data-ttu-id="77e28-118">В этой очереди задние буферы всегда нумеруются последовательно от 0 до (n-1), где n — число задних буферов, чтобы значение 0 обозначает самый наименее недавно представленный буфер.</span><span class="sxs-lookup"><span data-stu-id="77e28-118">Within this queue, the back buffers are always numbered sequentially from 0 to (n - 1), where n is the number of back buffers, so that 0 denotes the least recently presented buffer.</span></span> <span data-ttu-id="77e28-119">Если вызывается метод Present, очередь поворачивается таким образом, что передний буфер становится обратным буфером (n-1), а задний буфер 0 становится новым интерфейсным буфером.</span><span class="sxs-lookup"><span data-stu-id="77e28-119">When Present is invoked, the queue is "rotated" so that the front buffer becomes back buffer (n - 1), while the back buffer 0 becomes the new front buffer.</span></span>

</dd> <dt>

<span data-ttu-id="77e28-120"><span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**\_Копирование D3DSWAPEFFECT**</span><span class="sxs-lookup"><span data-stu-id="77e28-120"><span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**D3DSWAPEFFECT\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="77e28-121">Этот результат переключения может быть указан только для цепочки буферов, состоящей из одного заднего буфера.</span><span class="sxs-lookup"><span data-stu-id="77e28-121">This swap effect may be specified only for a swap chain comprising a single back buffer.</span></span> <span data-ttu-id="77e28-122">Независимо от того, является ли цепочка буферов оконной или полноэкранной, среда выполнения гарантирует семантику, подразумеваемую операцией на основе копирования, а именно то, что операция оставляет содержимое заднего буфера без изменений, вместо того чтобы заменять его содержимым переднего буфера в качестве операции, основанной на переворачивании.</span><span class="sxs-lookup"><span data-stu-id="77e28-122">Whether the swap chain is windowed or full-screen, the runtime will guarantee the semantics implied by a copy-based Present operation, namely that the operation leaves the content of the back buffer unchanged, instead of replacing it with the content of the front buffer as a flip-based Present operation would.</span></span>

<span data-ttu-id="77e28-123">Для цепочки полноэкранного переключения среда выполнения использует сочетание операций отражения и операций копирования, поддерживаемых, если это необходимо для скрытых задних буферов, для выполнения текущей операции.</span><span class="sxs-lookup"><span data-stu-id="77e28-123">For a full-screen swap chain, the runtime uses a combination of flip operations and copy operations, supported if necessary by hidden back buffers, to accomplish the Present operation.</span></span> <span data-ttu-id="77e28-124">Соответственно, презентация синхронизируется с вертикальной перетрассировкой видеоадаптера, и ее частота ограничена выбранным интервалом презентации.</span><span class="sxs-lookup"><span data-stu-id="77e28-124">Accordingly, the presentation is synchronized with the display adapter's vertical retrace and its rate is constrained by the chosen presentation interval.</span></span> <span data-ttu-id="77e28-125">Единственным исключением является цепочка подкачки, указанная с помощью \_ \_ флага интерпретации интервала D3DPRESENT.</span><span class="sxs-lookup"><span data-stu-id="77e28-125">A swap chain specified with the D3DPRESENT\_INTERVAL\_IMMEDIATE flag is the only exception.</span></span> <span data-ttu-id="77e28-126">(См. Описание элемента **пресентатионинтервалс** структуры [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md) .) В этом случае операция приведения копирует содержимое заднего буфера непосредственно в передний буфер, не дожидаясь вертикальной повторной трассировки.</span><span class="sxs-lookup"><span data-stu-id="77e28-126">(Refer to the description of the **PresentationIntervals** member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure.) In this case, a Present operation copies the back buffer content directly to the front buffer without waiting for the vertical retrace.</span></span>

</dd> <dt>

<span data-ttu-id="77e28-127"><span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**Наложение D3DSWAPEFFECT \_**</span><span class="sxs-lookup"><span data-stu-id="77e28-127"><span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**D3DSWAPEFFECT\_OVERLAY**</span></span>
</dt> <dd>

<span data-ttu-id="77e28-128">Используйте выделенную область видеопамяти, которая может быть наложена на основную поверхность.</span><span class="sxs-lookup"><span data-stu-id="77e28-128">Use a dedicated area of video memory that can be overlayed on the primary surface.</span></span> <span data-ttu-id="77e28-129">При отображении оверлея не выполняется ни одна копия.</span><span class="sxs-lookup"><span data-stu-id="77e28-129">No copy is performed when the overlay is displayed.</span></span> <span data-ttu-id="77e28-130">Операция наложения выполняется в оборудовании без изменения данных на основной поверхности.</span><span class="sxs-lookup"><span data-stu-id="77e28-130">The overlay operation is performed in hardware, without modifying the data in the primary surface.</span></span>

<span data-ttu-id="77e28-131">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="77e28-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="77e28-132">Наложение D3DSWAPEFFECT \_ доступно только в Direct3D9Ex, работающем в Windows 7 (или более текущей операционной системе).</span><span class="sxs-lookup"><span data-stu-id="77e28-132">D3DSWAPEFFECT\_OVERLAY is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span>

</dd> <dt>

<span data-ttu-id="77e28-133"><span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ флипекс**</span><span class="sxs-lookup"><span data-stu-id="77e28-133"><span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT\_FLIPEX**</span></span>
</dt> <dd>

<span data-ttu-id="77e28-134">Указывает, когда приложение использует режим перелистывания, в течение которого кадр приложения передается вместо копирования в диспетчер окон рабочего стола (DWM) для композиции, когда приложение представлено в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="77e28-134">Designates when an application is adopting flip mode, during which time an application's frame is passed instead of copied to the Desktop Window Manager(DWM) for composition when the application is presenting in windowed mode.</span></span> <span data-ttu-id="77e28-135">Режим отражения позволяет приложению более эффективно использовать пропускную способность памяти, а также позволяет приложению воспользоваться преимуществами полноценного отображения статистики.</span><span class="sxs-lookup"><span data-stu-id="77e28-135">Flip mode allows an application to more efficiently use memory bandwidth as well as enabling an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="77e28-136">Режим отражения не влияет на полноэкранное поведение.</span><span class="sxs-lookup"><span data-stu-id="77e28-136">Flip mode does not affect full-screen behavior.</span></span>

> [!Note]  
> <span data-ttu-id="77e28-137">При создании цепочки подкачки с помощью D3DSWAPEFFECT \_ флипекс нельзя переопределить элемент **хдевицевиндов** структуры [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md) при отображении нового кадра для отображения.</span><span class="sxs-lookup"><span data-stu-id="77e28-137">If you create a swap chain with D3DSWAPEFFECT\_FLIPEX, you can't override the **hDeviceWindow** member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure when you present a new frame for display.</span></span> <span data-ttu-id="77e28-138">То есть необходимо передать **значение NULL** параметру *хдествиндововерриде* объекта [**IDirect3DDevice9Ex::P ресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) , чтобы указать среде выполнения использовать член **хдевицевиндов** **\_ параметров D3DPRESENT** для презентации.</span><span class="sxs-lookup"><span data-stu-id="77e28-138">That is, you must pass **NULL** to the *hDestWindowOverride* parameter of [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) to instruct the runtime to use the **hDeviceWindow** member of **D3DPRESENT\_PARAMETERS** for the presentation.</span></span>

<span data-ttu-id="77e28-139">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="77e28-139">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="77e28-140">D3DSWAPEFFECT \_ флипекс доступен только в Direct3D9Ex, работающем в Windows 7 (или более текущей операционной системе).</span><span class="sxs-lookup"><span data-stu-id="77e28-140">D3DSWAPEFFECT\_FLIPEX is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span>

</dd> <dt>

<span data-ttu-id="77e28-141"><span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="77e28-141"><span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="77e28-142">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="77e28-142">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="77e28-143">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="77e28-143">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="77e28-144">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="77e28-144">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77e28-145">Remarks</span><span class="sxs-lookup"><span data-stu-id="77e28-145">Remarks</span></span>

<span data-ttu-id="77e28-146">Состояние заднего буфера после вызова метода Present четко определено каждым из этих эффектов переключения, а также от того, было ли устройство Direct3D создано с помощью цепочки полноэкранной замены или цепочки оконных буферов не влияет на это состояние.</span><span class="sxs-lookup"><span data-stu-id="77e28-146">The state of the back buffer after a call to Present is well-defined by each of these swap effects, and whether the Direct3D device was created with a full-screen swap chain or a windowed swap chain has no effect on this state.</span></span> <span data-ttu-id="77e28-147">В частности, \_ результат переключения D3DSWAPEFFECT отражения работает одинаково в оконном или полноэкранном режиме, а среда выполнения Direct3D гарантирует это путем создания дополнительных буферов.</span><span class="sxs-lookup"><span data-stu-id="77e28-147">In particular, the D3DSWAPEFFECT\_FLIP swap effect operates the same whether windowed or full-screen, and the Direct3D runtime guarantees this by creating extra buffers.</span></span> <span data-ttu-id="77e28-148">Поэтому рекомендуется, чтобы приложения по возможности использовали D3DSWAPEFFECT Discard, \_ чтобы избежать каких-либо потерь.</span><span class="sxs-lookup"><span data-stu-id="77e28-148">As a result, it is recommended that applications use D3DSWAPEFFECT\_DISCARD whenever possible to avoid any such penalties.</span></span> <span data-ttu-id="77e28-149">Это обусловлено тем, что этот результат переключения всегда будет наиболее эффективным в плане потребления памяти и производительности.</span><span class="sxs-lookup"><span data-stu-id="77e28-149">This is because this swap effect will always be the most efficient in terms of memory consumption and performance.</span></span>

<span data-ttu-id="77e28-150">Приложения, использующие D3DSWAPEFFECT \_ переворот или D3DSWAPEFFECT, \_ не должны ждать, пока не будет работать альфа-канал назначения в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="77e28-150">Applications that use D3DSWAPEFFECT\_FLIP or D3DSWAPEFFECT\_DISCARD should not expect full-screen destination alpha to work.</span></span> <span data-ttu-id="77e28-151">Это означает, что \_ состояние визуализации D3DRS дестбленд не будет работать должным образом, так как цепочки полноэкранного переключения с этими эффектами переключения не имеют явного формата пикселей от точки зрения драйвера.</span><span class="sxs-lookup"><span data-stu-id="77e28-151">This means that the D3DRS\_DESTBLEND render state will not work as expected because full-screen swap chains with these swap effects do not have an explicit pixel format from the driver's point of view.</span></span> <span data-ttu-id="77e28-152">Драйвер определяет, что они должны иметь формат вывода, у которого нет альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="77e28-152">The driver infers that they should take on the display format, which does not have an alpha channel.</span></span> <span data-ttu-id="77e28-153">Чтобы обойти это, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="77e28-153">To work around this, take the following steps:</span></span>

-   <span data-ttu-id="77e28-154">Используйте D3DSWAPEFFECT \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="77e28-154">Use D3DSWAPEFFECT\_COPY.</span></span>
-   <span data-ttu-id="77e28-155">Установите флаг D3DCAPS3 \_ Alpha \_ в полноэкранном режиме \_ \_ или \_ отклонить в элементе Caps3 структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="77e28-155">Check the D3DCAPS3\_ALPHA\_FULLSCREEN\_FLIP\_OR\_DISCARD flag in the Caps3 member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="77e28-156">Этот флаг указывает, может ли драйвер выполнять альфа-смешение при \_ использовании D3DSWAPEFFECT отражения или D3DSWAPEFFECT \_ Discard.</span><span class="sxs-lookup"><span data-stu-id="77e28-156">This flag indicates whether the driver can do alpha blending when D3DSWAPEFFECT\_FLIP or D3DSWAPEFFECT\_DISCARD is used.</span></span>
-   <span data-ttu-id="77e28-157">Приложения, использующие режим перелистывания (D3DSWAPEFFECT \_ флипекс), должны вызывать [**пресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) после изменения размера окна или региона, чтобы обеспечить обновление отображаемого содержимого.</span><span class="sxs-lookup"><span data-stu-id="77e28-157">Applications using flip mode swap effect (D3DSWAPEFFECT\_FLIPEX) should call [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) after a window resize or region change to ensure that the display content is updated.</span></span>

<span data-ttu-id="77e28-158">Невидимое окно не может принимать события пользовательского режима; Кроме того, невидимое полноэкранное окно повлияет на представление окна оконного режима окна другого приложения.</span><span class="sxs-lookup"><span data-stu-id="77e28-158">An invisible window cannot receive user-mode events; furthermore, an invisible-fullscreen window will interfere with the presentation of another applications' windowed-mode window.</span></span> <span data-ttu-id="77e28-159">Таким образом, каждое приложение должно обеспечить видимость окна устройства, когда имеющуюся цепочку буферов представлен в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="77e28-159">Therefore, each application needs to ensure that a device window is visible when a swapchain is presented in fullscreen mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="77e28-160">Требования</span><span class="sxs-lookup"><span data-stu-id="77e28-160">Requirements</span></span>

| <span data-ttu-id="77e28-161">Требование</span><span class="sxs-lookup"><span data-stu-id="77e28-161">Requirement</span></span> | <span data-ttu-id="77e28-162">Значение</span><span class="sxs-lookup"><span data-stu-id="77e28-162">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77e28-163">Заголовок</span><span class="sxs-lookup"><span data-stu-id="77e28-163">Header</span></span><br/> | <dl> <span data-ttu-id="77e28-164"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="77e28-164"><dt>D3D9Types.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="77e28-165">См. также</span><span class="sxs-lookup"><span data-stu-id="77e28-165">See also</span></span>

[<span data-ttu-id="77e28-166">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="77e28-166">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)

[<span data-ttu-id="77e28-167">**IDirect3DDevice9::Reset**</span><span class="sxs-lookup"><span data-stu-id="77e28-167">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
