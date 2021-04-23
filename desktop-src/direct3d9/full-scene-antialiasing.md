---
description: Сглаживание в полноэкранном режиме означает размытие краев каждого многоугольника в сцене по мере его растрирования в один проход; второй проход не требуется.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Сглаживание Full-Scene (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536836"
---
# <a name="full-scene-antialiasing-direct3d-9"></a><span data-ttu-id="4643e-103">Сглаживание Full-Scene (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4643e-103">Full-Scene Antialiasing (Direct3D 9)</span></span>

<span data-ttu-id="4643e-104">Сглаживание в полноэкранном режиме означает размытие краев каждого многоугольника в сцене по мере его растрирования в один проход; второй проход не требуется.</span><span class="sxs-lookup"><span data-stu-id="4643e-104">Full-scene antialiasing refers to blurring the edges of each polygon in the scene as it is rasterized in a single pass; no second pass is required.</span></span> <span data-ttu-id="4643e-105">Сглаживание с полным монтажом сцены влияет только на треугольники и группы треугольников.</span><span class="sxs-lookup"><span data-stu-id="4643e-105">Full-scene antialiasing, when supported, affects only triangles and groups of triangles.</span></span> <span data-ttu-id="4643e-106">Линии не могут быть сглажены с помощью служб Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4643e-106">Lines cannot be antialiased by using Direct3D services.</span></span> <span data-ttu-id="4643e-107">Сглаживание в полноэкранном режиме выполняется в Direct3D с использованием множественной выборки на каждом пикселе.</span><span class="sxs-lookup"><span data-stu-id="4643e-107">Full-scene antialiasing is done in Direct3D by using multisampling on each pixel.</span></span> <span data-ttu-id="4643e-108">Если включена многовыборочная выборка, все подмножества пикселов обновляются за один проход, но при использовании других эффектов, использующих несколько этапов отрисовки, приложение может указать, что только некоторые подвыборки будут затронуты данным проходом отрисовки.</span><span class="sxs-lookup"><span data-stu-id="4643e-108">When multisampling is enabled, all subsamples of a pixel are updated in one pass but when used for other effects that involve multiple rendering passes, the application can specify that only some subsamples are to be affected by a given rendering pass.</span></span> <span data-ttu-id="4643e-109">Этот второй подход позволяет имитировать размытие движения, эффекты фокуса в поле глубины, размытие отражения и т. д.</span><span class="sxs-lookup"><span data-stu-id="4643e-109">This latter approach enables simulation of motion blur, depth-of-field focus effects, reflection blur, and so on.</span></span>

<span data-ttu-id="4643e-110">В обоих случаях различные примеры, записанные для каждого пикселя, объединяются и выводятся на экран.</span><span class="sxs-lookup"><span data-stu-id="4643e-110">In both cases, the various samples recorded for each pixel are blended together and output to the screen.</span></span> <span data-ttu-id="4643e-111">Это позволяет улучшить качество сглаживания изображения или других эффектов.</span><span class="sxs-lookup"><span data-stu-id="4643e-111">This enables the improved image quality of antialiasing or other effects.</span></span>

<span data-ttu-id="4643e-112">Перед созданием устройства с помощью метода [**IDirect3D9:: креатедевице**](/windows/desktop/api) необходимо определить, поддерживается ли сглаживание в полном монтаже.</span><span class="sxs-lookup"><span data-stu-id="4643e-112">Before creating a device with the [**IDirect3D9::CreateDevice**](/windows/desktop/api) method, you need to determine if full-scene antialiasing is supported.</span></span> <span data-ttu-id="4643e-113">Для этого вызовите метод [**IDirect3D9:: чеккдевицемултисамплетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) , как показано в примере кода ниже.</span><span class="sxs-lookup"><span data-stu-id="4643e-113">Do this by calling the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method as shown in the code example below.</span></span>


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



<span data-ttu-id="4643e-114">Первый параметр, [**IDirect3D9:: чеккдевицемултисамплетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) , принимает порядковый номер, обозначающий отображаемый видеоадаптер.</span><span class="sxs-lookup"><span data-stu-id="4643e-114">The first parameter that [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accepts is an ordinal number that denotes the display adapter to query.</span></span> <span data-ttu-id="4643e-115">В этом образце используется D3DADAPTER \_ по умолчанию для указания основного видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="4643e-115">This sample uses D3DADAPTER\_DEFAULT to specify the primary display adapter.</span></span> <span data-ttu-id="4643e-116">Второй параметр — это значение из перечислимого типа [**D3DDEVTYPE**](./d3ddevtype.md) , которое указывает тип устройства.</span><span class="sxs-lookup"><span data-stu-id="4643e-116">The second parameter is a value from the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type, specifying the device type.</span></span> <span data-ttu-id="4643e-117">Третий параметр задает формат поверхности.</span><span class="sxs-lookup"><span data-stu-id="4643e-117">The third parameter specifies the format of the surface.</span></span> <span data-ttu-id="4643e-118">Четвертый параметр сообщает платформе Direct3D, следует ли выполнять запрос многовыборочной (**true**) или полной (**false**)-сцены.</span><span class="sxs-lookup"><span data-stu-id="4643e-118">The fourth parameter tells Direct3D whether to inquire about full-windowed multisampling (**TRUE**) or full-scene antialiasing (**FALSE**).</span></span> <span data-ttu-id="4643e-119">В этом примере используется **значение false** , чтобы сообщить Direct3D о том, что он выполняет запрос на полное сглаживание.</span><span class="sxs-lookup"><span data-stu-id="4643e-119">This sample uses **FALSE** to tell Direct3D that it is inquiring about full-scene antialiasing.</span></span> <span data-ttu-id="4643e-120">Последний параметр указывает метод многовыборки, который необходимо протестировать.</span><span class="sxs-lookup"><span data-stu-id="4643e-120">The last parameter specifies the multisampling technique that you want to test.</span></span> <span data-ttu-id="4643e-121">Используйте значение из перечисляемого [**типа \_ D3DMULTISAMPLE**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4643e-121">Use a value from the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="4643e-122">Этот пример проверяет, поддерживаются ли два уровня множественной выборки.</span><span class="sxs-lookup"><span data-stu-id="4643e-122">This sample tests to see if two levels of multisampling are supported.</span></span>

<span data-ttu-id="4643e-123">Если устройство поддерживает требуемый уровень многоуровневой выборки, необходимо задать параметры презентации, заполнив соответствующие члены структуры [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md) , чтобы создать многовыборочную область отрисовки.</span><span class="sxs-lookup"><span data-stu-id="4643e-123">If the device supports the level of multisampling that you want to use, the next step is to set the presentation parameters by filling in the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to create a multisample rendering surface.</span></span> <span data-ttu-id="4643e-124">После этого можно создать устройство.</span><span class="sxs-lookup"><span data-stu-id="4643e-124">After that, you can create the device.</span></span> <span data-ttu-id="4643e-125">В примере кода ниже показано, как настроить устройство с многовыборочной областью отрисовки.</span><span class="sxs-lookup"><span data-stu-id="4643e-125">The sample code below shows how to set up a device with a multisampling render surface.</span></span>


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



<span data-ttu-id="4643e-126">Чтобы использовать многовыборочную настройку, члену SwapEffect \_ параметра D3DPRESENT должно быть присвоено значение D3DSWAPEFFECT \_ Discard.</span><span class="sxs-lookup"><span data-stu-id="4643e-126">To use multisampling, the SwapEffect member of D3DPRESENT\_PARAMETER must be set to D3DSWAPEFFECT\_DISCARD.</span></span>

<span data-ttu-id="4643e-127">Последний шаг — включить многовыборочное сглаживание, вызвав метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) и УСТАНОВИВ \_ для D3DRS мултисамплеантиалиас **значение true**.</span><span class="sxs-lookup"><span data-stu-id="4643e-127">The last step is to enable multisampling antialiasing by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and setting the D3DRS\_MULTISAMPLEANTIALIAS to **TRUE**.</span></span> <span data-ttu-id="4643e-128">После установки этого значения в значение **true** для любой визуализации, к которой применена многовыборка, применяется.</span><span class="sxs-lookup"><span data-stu-id="4643e-128">After setting this value to **TRUE**, any rendering that you do will have multisampling applied to it.</span></span> <span data-ttu-id="4643e-129">Может потребоваться включить и отключить множественную выборку в зависимости от того, что вы выводяте.</span><span class="sxs-lookup"><span data-stu-id="4643e-129">You might want to enable and disable multisampling, depending on what you are rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4643e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4643e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4643e-131">Сглаживания</span><span class="sxs-lookup"><span data-stu-id="4643e-131">Antialiasing</span></span>](antialiasing.md)
</dt> </dl>

 

 
