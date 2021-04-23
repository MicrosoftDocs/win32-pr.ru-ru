---
title: Сведения об объекте Плайераппликатион
description: Сведения об объекте Плайераппликатион
ms.assetid: 4b77bf16-d7e1-4119-91c2-46136db13e81
keywords:
- Проигрыватель Windows Media, объект Плайераппликатион
- Объектная модель проигрывателя Windows Media, объект Плайераппликатион
- Объектная модель, объект Плайераппликатион
- Элемент управления ActiveX проигрывателя Windows Media, объект Плайераппликатион
- Элемент управления ActiveX, объект Плайераппликатион
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Плайераппликатион
- Проигрыватель Windows Media Mobile, объект Плайераппликатион
- Объект Плайераппликатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d197614ba75a51bdc8ec5398ca757e410f918a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888832"
---
# <a name="about-the-playerapplication-object"></a><span data-ttu-id="c4a12-111">Сведения об объекте Плайераппликатион</span><span class="sxs-lookup"><span data-stu-id="c4a12-111">About the PlayerApplication Object</span></span>

<span data-ttu-id="c4a12-112">Объект **плайераппликатион** используется для удаленного взаимодействия проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c4a12-112">The **PlayerApplication** object is used for remoting Windows Media Player.</span></span> <span data-ttu-id="c4a12-113">Он предоставляет функциональные возможности, необходимые для переключения между удаленным элементом управления проигрывателя Windows Media и полноэкранным режимом проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="c4a12-113">It provides the functionality required to switch between a remoted Windows Media Player control and the full mode of the Player.</span></span>

<span data-ttu-id="c4a12-114">Удаленное взаимодействие позволяет элементу управления проигрывателя Windows Media, внедренному в приложение C++, использовать тот же модуль воспроизведения, что и проигрыватель.</span><span class="sxs-lookup"><span data-stu-id="c4a12-114">Remoting enables a Windows Media Player control embedded in a C++ application to use the same playback engine as the Player.</span></span> <span data-ttu-id="c4a12-115">Это означает, что обычно вы будете использовать объект **плайераппликатион** в коде C++ с помощью COM-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="c4a12-115">This means that usually you will use the **PlayerApplication** object in C++ code using the COM interfaces.</span></span> <span data-ttu-id="c4a12-116">Однако существует особый случай, в котором можно встроить элемент управления проигрывателя Windows Media, который отображает обложку проигрывателя Windows Media в качестве пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c4a12-116">There is a special case, however, where you can embed the Windows Media Player control that displays a Windows Media Player skin as its user interface.</span></span> <span data-ttu-id="c4a12-117">В этом случае **плайераппликатион** можно программировать с помощью JScript в коде обложки.</span><span class="sxs-lookup"><span data-stu-id="c4a12-117">In this case, **PlayerApplication** can be programmed using JScript in the skin code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4a12-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c4a12-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4a12-119">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="c4a12-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="c4a12-120">**Объект Плайераппликатион**</span><span class="sxs-lookup"><span data-stu-id="c4a12-120">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> </dl>

 

 




