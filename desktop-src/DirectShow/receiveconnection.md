---
description: рецеивеконнектион
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: рецеивеконнектион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140099"
---
# <a name="receiveconnection"></a><span data-ttu-id="30844-103">рецеивеконнектион</span><span class="sxs-lookup"><span data-stu-id="30844-103">ReceiveConnection</span></span>

<span data-ttu-id="30844-104">Этот механизм позволяет выходному закреплениям предложить изменение формата для его подчиненного однорангового узла, если для нового формата требуется больший буфер.</span><span class="sxs-lookup"><span data-stu-id="30844-104">This mechanism enables an output pin to propose a format change to its downstream peer, when the new format requires a larger buffer.</span></span> <span data-ttu-id="30844-105">Закрепление вывода выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="30844-105">The output pin does the following:</span></span>

1.  <span data-ttu-id="30844-106">Вызывает [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) для входного ПИН-кода нисходящего входа.</span><span class="sxs-lookup"><span data-stu-id="30844-106">Calls [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the downstream input pin.</span></span>
2.  <span data-ttu-id="30844-107">Если операция `ReceiveConnection` выполнена, вызывается [**имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="30844-107">If `ReceiveConnection` succeeds, calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) on the input pin.</span></span>

<span data-ttu-id="30844-108">Кроме того, для изменения размеров буфера может потребоваться вызвать [**имемаллокатор:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) , а затем открепить и повторно зафиксировать распределитель.</span><span class="sxs-lookup"><span data-stu-id="30844-108">In addition, the output pin may need to call [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) and then decommit and recommit the allocator in order to change buffer sizes.</span></span> <span data-ttu-id="30844-109">Перед изменением размера буфера обязательно Доставьте все ожидающие выборки в старом формате.</span><span class="sxs-lookup"><span data-stu-id="30844-109">Make sure to deliver all pending samples in the old format before changing the buffer size.</span></span>

<span data-ttu-id="30844-110">Некоторые декодеры MPEG-2 используют этот механизм для переключения между выходными данными MPEG-1 и MPEG-2, а также при изменении размера видео.</span><span class="sxs-lookup"><span data-stu-id="30844-110">Some MPEG-2 decoders use this mechanism to switch between MPEG-1 and MPEG-2 output or if the video size changes.</span></span>

 

 



