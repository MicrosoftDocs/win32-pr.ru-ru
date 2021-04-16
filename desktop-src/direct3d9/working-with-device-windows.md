---
description: В этом разделе перечислены проблемы, которые могут возникнуть при работе с окнами устройств в приложениях Direct3D.
ms.assetid: 7cfd2ad6-fb85-4303-9fa4-6fe7d16d9951
title: Работа с окнами устройств (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56352ef0ec66def620a0ae0995d92d8b421722e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710577"
---
# <a name="working-with-device-windows-direct3d-9"></a><span data-ttu-id="50875-103">Работа с окнами устройств (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="50875-103">Working with Device Windows (Direct3D 9)</span></span>

<span data-ttu-id="50875-104">В этом разделе перечислены проблемы, которые могут возникнуть при работе с окнами устройств в приложениях Direct3D.</span><span class="sxs-lookup"><span data-stu-id="50875-104">This section lists an issue that you might encounter when working with device windows in Direct3D applications.</span></span>

-   <span data-ttu-id="50875-105">Direct3D подключается только к окнам фокуса, а не к окну устройства с помощью функции обработки сообщений Direct3D и обрабатывает только сообщения окна фокуса.</span><span class="sxs-lookup"><span data-stu-id="50875-105">Direct3D only hooks up the focus windows instead of the device window with the Direct3D message processing function, and only processes the focus window messages.</span></span> <span data-ttu-id="50875-106">Таким образом, окно фокуса должно быть родительским для любого окна устройства.</span><span class="sxs-lookup"><span data-stu-id="50875-106">So, the focus window should be the parent of any device window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50875-107">См. также</span><span class="sxs-lookup"><span data-stu-id="50875-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50875-108">Советы по программированию</span><span class="sxs-lookup"><span data-stu-id="50875-108">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



