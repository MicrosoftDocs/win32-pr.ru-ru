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
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a><span data-ttu-id="26145-103">Убедитесь, что текст отображается с правильным направлением чтения</span><span class="sxs-lookup"><span data-stu-id="26145-103">Ensure text is displayed with the correct reading direction</span></span>

<span data-ttu-id="26145-104">Для некоторых языков, таких как арабский и иврит, требуется направление чтения справа налево.</span><span class="sxs-lookup"><span data-stu-id="26145-104">Some languages, such as Arabic and Hebrew, require a right-to-left reading direction.</span></span> <span data-ttu-id="26145-105">Для объекта текстового формата [DirectWrite](direct-write-portal.md) направлением чтения по умолчанию является слева направо.</span><span class="sxs-lookup"><span data-stu-id="26145-105">For a [DirectWrite](direct-write-portal.md) text format object, the default reading direction is left-to-right.</span></span> <span data-ttu-id="26145-106">DirectWrite не автоматически определяет направление чтения из языкового стандарта, поэтому вам необходимо сделать это самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="26145-106">DirectWrite does not automatically infer the reading direction from the locale, so you must do this yourself.</span></span>

<span data-ttu-id="26145-107">Сначала получите флаги расширенного стиля для окна, в которое будет визуализирован текст, с помощью макроса Жетвиндовстиликс, определенного в виндовскс. h.</span><span class="sxs-lookup"><span data-stu-id="26145-107">First, get the extended style flags for the window that the text will be rendered to by using the GetWindowStyleEx macro defined in windowsx.h.</span></span>


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



<span data-ttu-id="26145-108">Макрос возвращает значение DWORD, состоящие из нескольких флагов, в сочетании с побитовыми операциями OR.</span><span class="sxs-lookup"><span data-stu-id="26145-108">The macro returns a DWORD value made up of several flags combined with bitwise OR operations.</span></span> <span data-ttu-id="26145-109">Необходимо определить, есть ли в нем определенные флаги, влияющие на направление чтения.</span><span class="sxs-lookup"><span data-stu-id="26145-109">You must determine if the specific flags affecting reading direction are there.</span></span>

<span data-ttu-id="26145-110">Существует два разных флага, связанных с направлением чтения: WS \_ ex \_ ЛАЙАУТРТЛ и WS \_ ex \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="26145-110">There are 2 different flags that are related to the reading direction: WS\_EX\_LAYOUTRTL and WS\_EX\_RTLREADING.</span></span>

<span data-ttu-id="26145-111">Используйте оператор побитового и (&) с переменной Двстиле и \_ \_ макросом WS ex лайаутртл, чтобы сохранить логическое значение, которое указывает, является ли макет зеркальным.</span><span class="sxs-lookup"><span data-stu-id="26145-111">Use the bitwise AND operator (&) with the dwStyle variable and the WS\_EX\_LAYOUTRTL macro to store a BOOL value that indicates if the layout is mirrored.</span></span>


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



<span data-ttu-id="26145-112">Сделайте то же самое для \_ \_ флага WS ex RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="26145-112">Do the same thing for the WS\_EX\_RTLREADING flag.</span></span>


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



<span data-ttu-id="26145-113">Задайте направление чтения с помощью метода [**идвритетекстформат:: сетреадингдиректион**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) .</span><span class="sxs-lookup"><span data-stu-id="26145-113">Set the reading direction by using the [**IDWriteTextFormat::SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) method.</span></span> <span data-ttu-id="26145-114">По умолчанию используется слева направо, поэтому необходимо задать направление чтения справа налево.</span><span class="sxs-lookup"><span data-stu-id="26145-114">The default is left-to-right, so you only need to set the reading direction if it is right-to-left.</span></span>

> [!Note]  
> <span data-ttu-id="26145-115">WS \_ ex \_ лайаутртл отражает весь макет и подразумевает направление чтения справа налево, поэтому задайте направление чтения только при наличии одного из этих флагов.</span><span class="sxs-lookup"><span data-stu-id="26145-115">WS\_EX\_LAYOUTRTL mirrors the whole layout and implies right-to-left reading direction, so set the reading direction only if one of these flags is present.</span></span> <span data-ttu-id="26145-116">Если оба они существуют, они отменяют друг друга, а направление чтения для текстового формата должно быть слева направо.</span><span class="sxs-lookup"><span data-stu-id="26145-116">If both are present, they cancel one another out and the reading direction for the text format should be left-to-right.</span></span>

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
