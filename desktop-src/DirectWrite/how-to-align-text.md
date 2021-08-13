---
title: Как выровняйте текст
description: DirectWrite текст можно вычислить с помощью метода сеттексталигнмент интерфейса идвритетекстформат.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a9d73443577468d794e43dc62d19e7dd24a86227ba6b5e5d8c3542cdded8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650373"
---
# <a name="how-to-align-text"></a>Как выровняйте текст

[DirectWrite](direct-write-portal.md) текст можно вычислить с помощью метода [**сеттексталигнмент**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) интерфейса [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , как показано в следующем коде, который выравнивает текст по центру.


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



Текст можно выровнять по начальному или нижнему краям поля макета или по центру. На следующем рисунке показан текст с выравниванием, имеющим [**значение \_ дврите \_ Выравнивание \_ текста в начале**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), в [**\_ \_ \_ центре выравнивания текста Дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), а также в [**\_ \_ \_ конце выравнивания текста дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), соответственно.

![Иллюстрация текстовых абзацев с выравниванием в начале, по центру и в конце](images/textalignment.png)

> [!Note]  
> Выравнивание зависит от направления чтения, приведенное выше для направления чтения слева направо. Для направления чтения справа налево это будет противоположным.

 

Объект [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) будет использовать выравнивание, которое было назначено для [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , предоставленного при создании макета. Чтобы изменить выравнивание текста, используйте [**идвритетекстлайаут:: сеттексталигнмент**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).

 

 
