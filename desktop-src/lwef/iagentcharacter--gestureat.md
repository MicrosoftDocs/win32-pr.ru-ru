---
title: Иажентчарактер Жестуреат
description: Иажентчарактер Жестуреат
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411456"
---
# <a name="iagentcharactergestureat"></a><span data-ttu-id="a8f7e-103">Иажентчарактер:: Жестуреат</span><span class="sxs-lookup"><span data-stu-id="a8f7e-103">IAgentCharacter::GestureAt</span></span>

<span data-ttu-id="a8f7e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a8f7e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="a8f7e-105">Воспроизводит связанную анимацию состояния **жестуринг** на основе указанного расположения.</span><span class="sxs-lookup"><span data-stu-id="a8f7e-105">Plays the associated **Gesturing** state animation based on the specified location.</span></span>

-   <span data-ttu-id="a8f7e-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a8f7e-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="a8f7e-107">Когда функция возвращает значение, *пдврекид* содержит идентификатор запроса.</span><span class="sxs-lookup"><span data-stu-id="a8f7e-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="a8f7e-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="a8f7e-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="a8f7e-109">Координата по оси x указанного расположения в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="a8f7e-109">The x-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="a8f7e-110"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="a8f7e-110"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="a8f7e-111">Координата по оси y указанного расположения в пикселях относительно начала экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="a8f7e-111">The y-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="a8f7e-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="a8f7e-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="a8f7e-113">Адрес переменной, которая получает идентификатор запроса **жестуреат** .</span><span class="sxs-lookup"><span data-stu-id="a8f7e-113">Address of a variable that receives the **GestureAt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="a8f7e-114">Сервер автоматически определяет и воспроизводит соответствующую анимацию жестуринг на основе текущей позиции символа и указанного расположения.</span><span class="sxs-lookup"><span data-stu-id="a8f7e-114">The server automatically determines and plays the appropriate gesturing animation based on the character's current position and the specified location.</span></span> <span data-ttu-id="a8f7e-115">При использовании протокола HTTP для доступа к данным символов и анимации используйте метод [**Prepare**](iagentcharacter--prepare.md) , чтобы убедиться, что анимации доступны перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="a8f7e-115">When using the HTTP protocol to access character and animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure that the animations are available before calling this method.</span></span>

 

 




