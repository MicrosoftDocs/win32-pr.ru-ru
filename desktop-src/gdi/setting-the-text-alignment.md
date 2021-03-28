---
description: Можно запрашивать и задавать выравнивание текста для контекста устройства с помощью функций Жеттексталигн и Сеттексталигн.
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: Настройка выравнивания текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538a8da060f9d854890ea004c855e2317986fd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985384"
---
# <a name="setting-the-text-alignment"></a>Настройка выравнивания текста

Можно запрашивать и задавать выравнивание текста для контекста устройства с помощью функций [**жеттексталигн**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) и [**сеттексталигн**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) . Параметры выравнивания текста определяют расположение текста относительно указанного расположения. Текст можно выровнять по правому или левому краю или по центру. его также можно выстроить над или под точкой.

В следующем примере показан метод определения установленного флага горизонтального выравнивания.


```C++
switch ((TA_LEFT | TA_RIGHT | TA_CENTER) & GetTextAlign(hdc)) 
{ 
    case TA_LEFT: 
       . 
       . 
       . 
    case TA_RIGHT: 
       . 
       . 
       . 
    case TA_CENTER: 
       . 
       . 
       . 
} 
```



Можно также использовать функцию [**сеттексталигн**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) для обновления текущей позицией при вызове функции вывода текста. Например, в следующем примере функция [**сеттексталигн**](/windows/win32/api/wingdi/nf-wingdi-settextalign) используется для обновления текущей позицией при вызове функции [**Text**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . В этом примере параметр *кариал* является целым числом, указывающим число шрифтов Arial.


```C++
UINT uAlignPrev; 
char szCount[8];
HRESULT hr;
size_t * pcch; 
 
uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
MoveToEx(hdc, 10, 50, (LPPOINT) NULL); 
TextOut(hdc, 0, 0, "Number of Arial fonts: ", 23); 
itoa(cArial, szCount, 10); 

hr = StringCchLength(szCount, 9, pcch);
if (FAILED(hr))
{
// TODO: write error handler 
}
 
TextOut(hdc, 0, 0, (LPSTR) szCount, *pcch); 
SetTextAlign(hdc, uAlignPrev); 
```



> [!Note]  
> При использовании Скриптстрингаут не следует использовать [**сеттексталигн**](/windows/win32/api/wingdi/nf-wingdi-settextalign) с параметром TA \_ упдатекп [](/windows/win32/api/usp10/nf-usp10-scriptstringout), так как выделенный текст отображается неправильно. Если необходимо использовать этот флаг, можно удалить и сбросить его по мере необходимости, чтобы избежать проблемы.

 

 

 
