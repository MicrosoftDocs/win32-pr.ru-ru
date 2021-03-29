---
title: Убедитесь, что текст отображается с правильным направлением чтения
description: Для некоторых языков, таких как арабский и иврит, требуется направление чтения справа налево.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d97eee49a830986718c04b4adab7443e488093
ms.sourcegitcommit: 43b2f5209d67eae96b17c03bac2a2afab1f4d30a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793777"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a>Убедитесь, что текст отображается с правильным направлением чтения

Для некоторых языков, таких как арабский и иврит, требуется направление чтения справа налево. Для объекта текстового формата [DirectWrite](direct-write-portal.md) направлением чтения по умолчанию является слева направо. DirectWrite не автоматически определяет направление чтения из языкового стандарта, поэтому вам необходимо сделать это самостоятельно.

Сначала получите флаги расширенного стиля для окна, в которое будет визуализирован текст, с помощью макроса Жетвиндовстиликс, определенного в виндовскс. h.


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



Макрос возвращает значение DWORD, состоящие из нескольких флагов, в сочетании с побитовыми операциями OR. Необходимо определить, есть ли в нем определенные флаги, влияющие на направление чтения.

Существует два разных флага, связанных с направлением чтения: WS \_ ex \_ ЛАЙАУТРТЛ и WS \_ ex \_ RTLREADING.

Используйте оператор побитового и (&) с переменной Двстиле и \_ \_ макросом WS ex лайаутртл, чтобы сохранить логическое значение, которое указывает, является ли макет зеркальным.


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



Сделайте то же самое для \_ \_ флага WS ex RTLREADING.


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



Задайте направление чтения с помощью метода [**идвритетекстформат:: сетреадингдиректион**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) . По умолчанию используется слева направо, поэтому необходимо задать направление чтения справа налево.

> [!Note]  
> WS \_ ex \_ лайаутртл отражает весь макет и подразумевает направление чтения справа налево, поэтому задайте направление чтения только при наличии одного из этих флагов. Если оба они существуют, они отменяют друг друга, а направление чтения для текстового формата должно быть слева направо.

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
