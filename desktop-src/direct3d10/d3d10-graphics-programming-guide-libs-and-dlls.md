---
description: Для правильной работы приложения на главном компьютере должны быть установлены соответствующие библиотеки DLL. Эти библиотеки DLL могут предоставляться либо операционной системой, либо распространяемым пакетом приложений.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Связывание статических и динамических библиотек (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692012"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a><span data-ttu-id="3a9c3-104">Связывание статических и динамических библиотек (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3a9c3-104">Linking Static and Dynamic Libraries (Direct3D 10)</span></span>

<span data-ttu-id="3a9c3-105">Для правильной работы приложения на главном компьютере должны быть установлены соответствующие библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-105">For an application to run properly, the host computer must have the appropriate DLLs installed.</span></span> <span data-ttu-id="3a9c3-106">Эти библиотеки DLL могут предоставляться либо операционной системой, либо распространяемым пакетом приложений.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-106">These DLLs may be provided by either the operating system, or the applications' redistributable package.</span></span>

## <a name="libraries-load-appropriate-dlls"></a><span data-ttu-id="3a9c3-107">Библиотеки загружают соответствующие библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="3a9c3-107">Libraries Load Appropriate DLLs</span></span>

<span data-ttu-id="3a9c3-108">Библиотеки, поставляемые с пакетом SDK для DirectX, автоматически загружают соответствующие библиотеки DLL во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-108">The libraries included with the DirectX SDK will automatically load the proper DLLs at runtime.</span></span> <span data-ttu-id="3a9c3-109">Исключением из этого правила является d3dx10. lib/d3dx10d. lib, которое загружает d3dx10.dll, которое было отправлено в эту версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-109">The exception to this rule is d3dx10.lib/d3dx10d.lib, which will load the d3dx10.dll that was shipped with that version of the SDK.</span></span> <span data-ttu-id="3a9c3-110">Например, если загруженный пакет SDK содержит d3dx10 \_33.dll и d3dx10 \_34.dll, то библиотека (d3dx10. lib), которая поставляется вместе с этим ПАКЕТом SDK, загрузит d3dx10 \_34.dll.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-110">For example, if the downloaded SDK includes d3dx10\_33.dll and d3dx10\_34.dll, then the library (d3dx10.lib) that shipped with that SDK will load d3dx10\_34.dll.</span></span> <span data-ttu-id="3a9c3-111">Если последующий пакет SDK установлен позднее, содержащий d3dx10 \_ 35. lib, d3dx10. lib из предыдущего пакета SDK все еще будет загружать d3dx10 \_34.dll.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-111">If a subsequent SDK is installed later containing d3dx10\_35.lib, the d3dx10.lib from the previous SDK will still load d3dx10\_34.dll.</span></span> <span data-ttu-id="3a9c3-112">D3dx10. lib из нового пакета SDK будет загружать d3dx10 \_35.dll.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-112">The d3dx10.lib from the newer SDK will load d3dx10\_35.dll.</span></span>

## <a name="redistributing-binaries"></a><span data-ttu-id="3a9c3-113">Распространение двоичных файлов</span><span class="sxs-lookup"><span data-stu-id="3a9c3-113">Redistributing Binaries</span></span>

<span data-ttu-id="3a9c3-114">Распространять можно только d3dx10.dll (и последующие версии одного и того же файла).</span><span class="sxs-lookup"><span data-stu-id="3a9c3-114">Only d3dx10.dll (and subsequent versions of the same file) can be redistributed.</span></span> <span data-ttu-id="3a9c3-115">Чтобы повторно распространить этот файл, необходимо использовать функцию **директкссетуп** .</span><span class="sxs-lookup"><span data-stu-id="3a9c3-115">To redistribute this file, you must use the **DirectXSetup** function.</span></span> <span data-ttu-id="3a9c3-116">Дополнительные сведения об использовании этой функции и объединении распространяемого пакета см. в разделе [Установка DirectX с помощью директсетуп](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="3a9c3-116">For details on using this function and putting together a redistributable package, see [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span></span> <span data-ttu-id="3a9c3-117">Все остальные необходимые двоичные файлы включены в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-117">All other necessary binaries are included in Windows Vista.</span></span> <span data-ttu-id="3a9c3-118">Единственные двоичные файлы, которые можно распространить, находятся в следующем каталоге.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-118">The only binaries that can be redistributed are those located in the following directory.</span></span>


```
(SDK root)\Redist
```



<span data-ttu-id="3a9c3-119">В следующей таблице описаны разработчики двоичных файлов, о которых следует знать.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-119">The following table describes the binaries developers should be aware of.</span></span>



| <span data-ttu-id="3a9c3-120">Двоичные файлы Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="3a9c3-120">Direct3D 10 Binaries</span></span>   | <span data-ttu-id="3a9c3-121">Описание</span><span class="sxs-lookup"><span data-stu-id="3a9c3-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a9c3-122">d3dx10.dllИ d3dx10d.dll</span><span class="sxs-lookup"><span data-stu-id="3a9c3-122">d3dx10.dll/d3dx10d.dll</span></span> | <span data-ttu-id="3a9c3-123">Компоненты D3DX10 Retail и Debug; компоненты розничной торговли можно распространять в CAB-файле Redist.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-123">Retail and debug D3DX10 components; the retail components can be redistributed in the REDIST CAB.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3a9c3-124">d3d10ref.dll</span><span class="sxs-lookup"><span data-stu-id="3a9c3-124">d3d10ref.dll</span></span>           | <span data-ttu-id="3a9c3-125">Ссылка на средство программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-125">Reference Rasterizer.</span></span> <span data-ttu-id="3a9c3-126">Предоставляет программную реализацию графического конвейера.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-126">Provides software implementation of the graphics pipeline.</span></span> <span data-ttu-id="3a9c3-127">Включается только в состав Windows SDK или устаревшей версии пакета SDK DirectX и не может распространяться повторно.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-127">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> <span data-ttu-id="3a9c3-128">Средство программной прорисовки ссылок предназначено только для отладки.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-128">The Reference Rasterizer is intended for debugging only.</span></span> <span data-ttu-id="3a9c3-129">Явное связывание не требуется; попытка создать эталонное устройство (см. [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) загрузит эту библиотеку DLL, если она есть.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-129">Explicit linking is not necessary; attempting to create a reference device (see [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) will load this dll if it is present.</span></span>                                                                                                    |
| <span data-ttu-id="3a9c3-130">d3d10sdklayers.dll</span><span class="sxs-lookup"><span data-stu-id="3a9c3-130">d3d10sdklayers.dll</span></span>     | <span data-ttu-id="3a9c3-131">Ряд служебных программ SDK, которые действуют как слой между вызовами API и выполнением среды выполнения, включая [слой отладки](d3d10-graphics-programming-guide-api-features-layers.md) и слой переключения на ссылки.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-131">A series of SDK utilities that act as a layer between API calls and runtime execution, including the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) and the switch-to-reference layer.</span></span> <span data-ttu-id="3a9c3-132">Явное связывание не требуется; Если устройство создается с соответствующим флагом слоя, эта библиотека DLL загружается автоматически.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-132">Explicit linking is not necessary; if a device is created with the appropriate layer flag, this DLL is loaded automatically.</span></span> <span data-ttu-id="3a9c3-133">Этот компонент предназначен только для целей разработки и отладки.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-133">This component is meant for development and debugging purposes only.</span></span> <span data-ttu-id="3a9c3-134">Включается только в состав Windows SDK или устаревшей версии пакета SDK DirectX и не может распространяться повторно.</span><span class="sxs-lookup"><span data-stu-id="3a9c3-134">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3a9c3-135">См. также</span><span class="sxs-lookup"><span data-stu-id="3a9c3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a9c3-136">Рекомендации по программированию для Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="3a9c3-136">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="3a9c3-137">Графика Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="3a9c3-137">Direct3D 10 Graphics</span></span>](d3d10-graphics.md)
</dt> </dl>

 

 



