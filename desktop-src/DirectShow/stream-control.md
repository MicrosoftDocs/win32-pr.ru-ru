---
description: Потоковый элемент управления
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Потоковый элемент управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41cee586737e131d4a32508b9ba6dd9ef1bd3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911092"
---
# <a name="stream-control"></a><span data-ttu-id="e9e26-103">Потоковый элемент управления</span><span class="sxs-lookup"><span data-stu-id="e9e26-103">Stream Control</span></span>

<span data-ttu-id="e9e26-104">Интерфейс [**ивмрвидеостреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) на входных ПИН-кодах VMR позволяет приложениям и вышестоящим фильтрам управлять поведением компонента микшера, включая Z-порядок и активное состояние входных потоков VMR.</span><span class="sxs-lookup"><span data-stu-id="e9e26-104">The [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) interface on the VMR's input pin(s) enables applications and upstream filters to control the behavior of the mixer component, including the Z-order and the active state of the VMR's input streams.</span></span> <span data-ttu-id="e9e26-105">Несмотря на то, что этот интерфейс предоставляется на ПИН-кодах, он работает с компонентом микшера VMR, поэтому он доступен только при загрузке микшера, то есть когда VMR обрабатывает несколько входных потоков.</span><span class="sxs-lookup"><span data-stu-id="e9e26-105">Although this interface is exposed on the pins, it operates on the VMR's mixer component, so it is only available when the mixer is loaded, which is when the VMR is processing multiple input streams.</span></span> <span data-ttu-id="e9e26-106">Вышестоящий фильтр использует методы [**сетколоркэй**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) и [**жетколоркэй**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) для управления ключом цвета источника.</span><span class="sxs-lookup"><span data-stu-id="e9e26-106">Upstream filters use the [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) and [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) methods to control the source color key.</span></span> <span data-ttu-id="e9e26-107">Эти методы позволяют реализовать такие эффекты, как наложение анимации на видео.</span><span class="sxs-lookup"><span data-stu-id="e9e26-107">These methods enable effects such as the overlay of animation over video.</span></span> <span data-ttu-id="e9e26-108">Просто задайте цветовой ключ для цвета фона потока анимации, и VMR будет смешивать этот поток с другим видеопотоком.</span><span class="sxs-lookup"><span data-stu-id="e9e26-108">Simply set the color key to the animation stream's background color, and the VMR will mix that stream with another video stream.</span></span> <span data-ttu-id="e9e26-109">Приложениям следует не менять цветовой ключ на какое-либо значение, которое отличается от значения, используемого вышестоящим фильтром, например декодером.</span><span class="sxs-lookup"><span data-stu-id="e9e26-109">Applications should take care not to change the color key to some value that is different than the value being used by an upstream filter, such as a decoder.</span></span>

<span data-ttu-id="e9e26-110">Фильтры используют методы [**жетстреамактивестате**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) и [**сетстреамактивестате**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) , чтобы сообщить микшеру, следует ли рассчитывать входные данные из указанного пин-кода.</span><span class="sxs-lookup"><span data-stu-id="e9e26-110">Filters use the [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) and [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) methods to tell the mixer whether to expect input data from a specified pin.</span></span> <span data-ttu-id="e9e26-111">Например, декодер Line21 использует эти методы для активации входного ПИН-кода VMR для данных Line21 только при наличии этих данных в потоке.</span><span class="sxs-lookup"><span data-stu-id="e9e26-111">For example, the Line21 Decoder uses these methods to activate the VMR's input pin for Line21 data only when that data is present in the stream.</span></span> <span data-ttu-id="e9e26-112">Если задать ПИН-код неактивного состояния, то микшер не будет ждать передачи данных с указанного пин-кода перед компоновкой образа.</span><span class="sxs-lookup"><span data-stu-id="e9e26-112">Setting a pin to an inactive state instructs the mixer not to wait for data from a specified pin before compositing the image.</span></span>

 

 



