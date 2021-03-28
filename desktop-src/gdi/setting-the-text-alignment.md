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
# <a name="setting-the-text-alignment"></a><span data-ttu-id="8d8a6-103">Настройка выравнивания текста</span><span class="sxs-lookup"><span data-stu-id="8d8a6-103">Setting the Text Alignment</span></span>

<span data-ttu-id="8d8a6-104">Можно запрашивать и задавать выравнивание текста для контекста устройства с помощью функций [**жеттексталигн**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) и [**сеттексталигн**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) .</span><span class="sxs-lookup"><span data-stu-id="8d8a6-104">You can query and set the text alignment for a device context by using the [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) and [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) functions.</span></span> <span data-ttu-id="8d8a6-105">Параметры выравнивания текста определяют расположение текста относительно указанного расположения.</span><span class="sxs-lookup"><span data-stu-id="8d8a6-105">The text-alignment settings determine how text is positioned relative to a specified location.</span></span> <span data-ttu-id="8d8a6-106">Текст можно выровнять по правому или левому краю или по центру. его также можно выстроить над или под точкой.</span><span class="sxs-lookup"><span data-stu-id="8d8a6-106">Text can be aligned to the right or left of the position or centered over it; it can also be aligned above or below the point.</span></span>

<span data-ttu-id="8d8a6-107">В следующем примере показан метод определения установленного флага горизонтального выравнивания.</span><span class="sxs-lookup"><span data-stu-id="8d8a6-107">The following example shows a method for determining which horizontal alignment flag is set:</span></span>


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



<span data-ttu-id="8d8a6-108">Можно также использовать функцию [**сеттексталигн**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) для обновления текущей позицией при вызове функции вывода текста.</span><span class="sxs-lookup"><span data-stu-id="8d8a6-108">You can also use the [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) function to update the current position when a text-output function is called.</span></span> <span data-ttu-id="8d8a6-109">Например, в следующем примере функция [**сеттексталигн**](/windows/win32/api/wingdi/nf-wingdi-settextalign) используется для обновления текущей позицией при вызове функции [**Text**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) .</span><span class="sxs-lookup"><span data-stu-id="8d8a6-109">For instance, the following example uses the [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) function to update the current position when the [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function is called.</span></span> <span data-ttu-id="8d8a6-110">В этом примере параметр *кариал* является целым числом, указывающим число шрифтов Arial.</span><span class="sxs-lookup"><span data-stu-id="8d8a6-110">In this example, the *cArial* parameter is an integer that specifies the number of Arial fonts.</span></span>


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
> <span data-ttu-id="8d8a6-111">При использовании Скриптстрингаут не следует использовать [**сеттексталигн**](/windows/win32/api/wingdi/nf-wingdi-settextalign) с параметром TA \_ упдатекп [](/windows/win32/api/usp10/nf-usp10-scriptstringout), так как выделенный текст отображается неправильно.</span><span class="sxs-lookup"><span data-stu-id="8d8a6-111">You should not use [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) with TA\_UPDATECP when you are using [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), because selected text is not rendered correctly.</span></span> <span data-ttu-id="8d8a6-112">Если необходимо использовать этот флаг, можно удалить и сбросить его по мере необходимости, чтобы избежать проблемы.</span><span class="sxs-lookup"><span data-stu-id="8d8a6-112">If you must use this flag, you can unset and reset it as necessary to avoid the problem.</span></span>

 

 

 
