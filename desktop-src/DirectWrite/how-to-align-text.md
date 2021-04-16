---
title: Как выровняйте текст
description: Текст DirectWrite можно выстроить с помощью метода Сеттексталигнмент интерфейса Идвритетекстформат.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb765860f2fbaac94409aa9ec20c2269beb45cbb
ms.sourcegitcommit: 3b9424e1dcd951b2a73e47de3c7f4d734de4263b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "106103869"
---
# <a name="how-to-align-text"></a><span data-ttu-id="50ebe-103">Как выровняйте текст</span><span class="sxs-lookup"><span data-stu-id="50ebe-103">How to Align Text</span></span>

<span data-ttu-id="50ebe-104">Текст [DirectWrite](direct-write-portal.md) можно выстроить с помощью метода [**сеттексталигнмент**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) интерфейса [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , как показано в следующем коде, который выравнивает текст по центру.</span><span class="sxs-lookup"><span data-stu-id="50ebe-104">You can align [DirectWrite](direct-write-portal.md) text by using the [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) method of the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface, as shown in the following code that centers the text.</span></span>


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



<span data-ttu-id="50ebe-105">Текст можно выровнять по начальному или нижнему краям поля макета или по центру.</span><span class="sxs-lookup"><span data-stu-id="50ebe-105">The text can be aligned to the leading or trailing edge of the layout box, or it can be centered.</span></span> <span data-ttu-id="50ebe-106">На следующем рисунке показан текст с выравниванием, имеющим [**значение \_ дврите \_ Выравнивание \_ текста в начале**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), в [**\_ \_ \_ центре выравнивания текста Дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), а также в [**\_ \_ \_ конце выравнивания текста дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), соответственно.</span><span class="sxs-lookup"><span data-stu-id="50ebe-106">The following illustration shows text with the alignment set to [**DWRITE\_TEXT\_ALIGNMENT\_LEADING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE\_TEXT\_ALIGNMENT\_CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), and [**DWRITE\_TEXT\_ALIGNMENT\_TRAILING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectively.</span></span>

![Иллюстрация текстовых абзацев с выравниванием в начале, по центру и в конце](images/textalignment.png)

> [!Note]  
> <span data-ttu-id="50ebe-108">Выравнивание зависит от направления чтения, приведенное выше для направления чтения слева направо.</span><span class="sxs-lookup"><span data-stu-id="50ebe-108">The alignment is dependent on reading direction, the above is for left-to-right reading direction.</span></span> <span data-ttu-id="50ebe-109">Для направления чтения справа налево это будет противоположным.</span><span class="sxs-lookup"><span data-stu-id="50ebe-109">For right-to-left reading direction it would be the opposite.</span></span>

 

<span data-ttu-id="50ebe-110">Объект [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) будет использовать выравнивание, которое было назначено для [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , предоставленного при создании макета.</span><span class="sxs-lookup"><span data-stu-id="50ebe-110">An [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object will use the alignment that has been designated for the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provided by you when creating the layout.</span></span> <span data-ttu-id="50ebe-111">Чтобы изменить выравнивание текста, используйте [**идвритетекстлайаут:: сеттексталигнмент**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span><span class="sxs-lookup"><span data-stu-id="50ebe-111">To change the text alignment, use [**IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span></span>

 

 
