---
title: Как выровняйте текст
description: Текст DirectWrite можно выстроить с помощью метода Сеттексталигнмент интерфейса Идвритетекстформат.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfd7a025769dea34444236805ebb8e5530ea06c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792666"
---
# <a name="how-to-align-text"></a>Как выровняйте текст

Текст [DirectWrite](direct-write-portal.md) можно выстроить с помощью метода [**сеттексталигнмент**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) интерфейса [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , как показано в следующем коде, который выравнивает текст по центру.


```C++
if (SUCCEEDED(hr))
{
    hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
}
```



Текст можно выровнять по начальному или нижнему краям поля макета или по центру. На следующем рисунке показан текст с выравниванием, имеющим [**значение \_ дврите \_ Выравнивание \_ текста в начале**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), в [**\_ \_ \_ центре выравнивания текста Дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), а также в [**\_ \_ \_ конце выравнивания текста дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), соответственно.

![Иллюстрация текстовых абзацев с выравниванием в начале, по центру и в конце](images/textalignment.png)

> [!Note]  
> Выравнивание зависит от направления чтения, приведенное выше для направления чтения слева направо. Для направления чтения справа налево это будет противоположным.

 

Объект [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) будет использовать выравнивание, которое было назначено для [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , предоставленного при создании макета. Чтобы изменить выравнивание текста, используйте [**идвритетекстлайаут:: сеттексталигнмент**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).

 

 