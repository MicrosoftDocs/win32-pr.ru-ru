---
title: Динамическая сериализация буфера
description: При использовании динамического стиля буфера сериализации буфер маршалинга выделяется заглушкой, а данные кодируются в этот буфер и передаются обратно. При распаковке Вы предоставляете буфер, содержащий данные.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486792"
---
# <a name="dynamic-buffer-serialization"></a><span data-ttu-id="9eb9c-104">Динамическая сериализация буфера</span><span class="sxs-lookup"><span data-stu-id="9eb9c-104">Dynamic Buffer Serialization</span></span>

<span data-ttu-id="9eb9c-105">При использовании динамического стиля буфера сериализации буфер маршалинга выделяется заглушкой, а данные кодируются в этот буфер и передаются обратно.</span><span class="sxs-lookup"><span data-stu-id="9eb9c-105">When using the dynamic buffer style of serialization, the marshalling buffer is allocated by the stub, and the data is encoded into this buffer and passed back to you.</span></span> <span data-ttu-id="9eb9c-106">При распаковке Вы предоставляете буфер, содержащий данные.</span><span class="sxs-lookup"><span data-stu-id="9eb9c-106">When unmarshaling, you supply the buffer that contains the data.</span></span>

<span data-ttu-id="9eb9c-107">Динамический стиль буфера для сериализации использует следующие подпрограммы:</span><span class="sxs-lookup"><span data-stu-id="9eb9c-107">The dynamic buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="9eb9c-108">**месенкодединбуфферхандлекреате**</span><span class="sxs-lookup"><span data-stu-id="9eb9c-108">**MesEncodeDynBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [<span data-ttu-id="9eb9c-109">**месдекодебуфферхандлекреате**</span><span class="sxs-lookup"><span data-stu-id="9eb9c-109">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="9eb9c-110">**месбуфферхандлересет**</span><span class="sxs-lookup"><span data-stu-id="9eb9c-110">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="9eb9c-111">**мешандлефри**</span><span class="sxs-lookup"><span data-stu-id="9eb9c-111">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="9eb9c-112">Функция [**месенкодединбуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) выделяет память, необходимую для маркера кодирования, а затем инициализирует ее.</span><span class="sxs-lookup"><span data-stu-id="9eb9c-112">The [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) function allocates the memory needed for the encoding handle and then initializes it.</span></span> <span data-ttu-id="9eb9c-113">Приложение может вызвать [**месбуфферхандлересет**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) для повторной инициализации маркера.</span><span class="sxs-lookup"><span data-stu-id="9eb9c-113">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle.</span></span> <span data-ttu-id="9eb9c-114">Он вызывает [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree) для освобождения памяти обработчика.</span><span class="sxs-lookup"><span data-stu-id="9eb9c-114">It calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="9eb9c-115">Чтобы создать маркер декодирования, соответствующий маркеру динамической кодировки буфера, используйте [**месдекодебуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="9eb9c-115">To create a decoding handle corresponding to the dynamic buffer encoding handle, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

 

 




