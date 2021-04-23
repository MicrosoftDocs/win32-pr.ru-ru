---
description: Получает события регистрации окна Ишеллвиндовс.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Объект Дшеллвиндовсевентс (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987551"
---
# <a name="dshellwindowsevents-object"></a><span data-ttu-id="13fdc-103">Объект Дшеллвиндовсевентс</span><span class="sxs-lookup"><span data-stu-id="13fdc-103">DShellWindowsEvents object</span></span>

<span data-ttu-id="13fdc-104">Получает события регистрации окна [**ишеллвиндовс**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) .</span><span class="sxs-lookup"><span data-stu-id="13fdc-104">Receives [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) window registration events.</span></span>

## <a name="members"></a><span data-ttu-id="13fdc-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="13fdc-105">Members</span></span>

<span data-ttu-id="13fdc-106">Объект **дшеллвиндовсевентс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="13fdc-106">The **DShellWindowsEvents** object has these types of members:</span></span>

-   [<span data-ttu-id="13fdc-107">Методы</span><span class="sxs-lookup"><span data-stu-id="13fdc-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="13fdc-108">Методы</span><span class="sxs-lookup"><span data-stu-id="13fdc-108">Methods</span></span>

<span data-ttu-id="13fdc-109">Объект **дшеллвиндовсевентс** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="13fdc-109">The **DShellWindowsEvents** object has these methods.</span></span>



| <span data-ttu-id="13fdc-110">Метод</span><span class="sxs-lookup"><span data-stu-id="13fdc-110">Method</span></span>                                                           | <span data-ttu-id="13fdc-111">Описание</span><span class="sxs-lookup"><span data-stu-id="13fdc-111">Description</span></span>                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="13fdc-112">**виндоврегистеред**</span><span class="sxs-lookup"><span data-stu-id="13fdc-112">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md) | <span data-ttu-id="13fdc-113">Вызывается, когда окно регистрируется как окно оболочки.</span><span class="sxs-lookup"><span data-stu-id="13fdc-113">Called when a window is registered as a Shell window.</span></span> <br/> |
| [<span data-ttu-id="13fdc-114">**виндовревокед**</span><span class="sxs-lookup"><span data-stu-id="13fdc-114">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)       | <span data-ttu-id="13fdc-115">Вызывается при отмене регистрации окна оболочки.</span><span class="sxs-lookup"><span data-stu-id="13fdc-115">Called when a Shell window's registration is revoked.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="13fdc-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="13fdc-116">Remarks</span></span>

<span data-ttu-id="13fdc-117">Используйте **дшеллвиндовсевентс** для отслеживания регистрации или отзыва окна оболочки.</span><span class="sxs-lookup"><span data-stu-id="13fdc-117">Use **DShellWindowsEvents** to monitor when a Shell window is registered or revoked.</span></span> <span data-ttu-id="13fdc-118">Дополнительные сведения см. в разделе [**ишеллвиндовс**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span><span class="sxs-lookup"><span data-stu-id="13fdc-118">For more information, see [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span></span>

## <a name="requirements"></a><span data-ttu-id="13fdc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="13fdc-119">Requirements</span></span>



| <span data-ttu-id="13fdc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="13fdc-120">Requirement</span></span> | <span data-ttu-id="13fdc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="13fdc-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13fdc-122">Продукт</span><span class="sxs-lookup"><span data-stu-id="13fdc-122">Product</span></span><br/> | <span data-ttu-id="13fdc-123">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="13fdc-123">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="13fdc-124">Header</span><span class="sxs-lookup"><span data-stu-id="13fdc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="13fdc-125"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="13fdc-125"><dt>Exdisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="13fdc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="13fdc-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="13fdc-127"><dt>Shdocvw.dll (версия 5.00.2014.0216 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="13fdc-127"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |
| <span data-ttu-id="13fdc-128">IID</span><span class="sxs-lookup"><span data-stu-id="13fdc-128">IID</span></span><br/>     | <span data-ttu-id="13fdc-129">IID \_ ишеллвиндовс</span><span class="sxs-lookup"><span data-stu-id="13fdc-129">IID\_IShellWindows</span></span><br/>                                                                                            |



## <a name="see-also"></a><span data-ttu-id="13fdc-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13fdc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13fdc-131">**шеллвиндовс**</span><span class="sxs-lookup"><span data-stu-id="13fdc-131">**ShellWindows**</span></span>](shellwindows.md)
</dt> </dl>

 

 




