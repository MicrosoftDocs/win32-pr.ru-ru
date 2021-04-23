---
title: Использование дубликатов шрифта
description: В этом разделе объясняется, как использовать дубликат шрифта для применения нескольких изменений к текстовому диапазону одновременно.
ms.assetid: CF0123E5-313F-4583-872F-6FE954F1C9E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dce0481b59fe9955b93a00b2c0d703c5c695ef
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103987296"
---
# <a name="how-to-use-a-font-duplicate"></a><span data-ttu-id="7ef63-103">Использование дубликатов шрифта</span><span class="sxs-lookup"><span data-stu-id="7ef63-103">How to Use a Font Duplicate</span></span>

<span data-ttu-id="7ef63-104">В этом разделе объясняется, как использовать дубликат шрифта для применения нескольких изменений к текстовому диапазону одновременно.</span><span class="sxs-lookup"><span data-stu-id="7ef63-104">This section explains how to use a font duplicate to apply a number of changes to a text range, all at once.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7ef63-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="7ef63-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7ef63-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="7ef63-106">Technologies</span></span>

-   [<span data-ttu-id="7ef63-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="7ef63-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7ef63-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7ef63-108">Prerequisites</span></span>

-   <span data-ttu-id="7ef63-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="7ef63-109">C/C++</span></span>
-   <span data-ttu-id="7ef63-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="7ef63-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7ef63-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="7ef63-111">Instructions</span></span>

### <a name="use-a-font-duplicate"></a><span data-ttu-id="7ef63-112">Использовать дубликат шрифта</span><span class="sxs-lookup"><span data-stu-id="7ef63-112">Use a Font Duplicate</span></span>

<span data-ttu-id="7ef63-113">В следующем примере показано, как можно использовать дубликат шрифта для одновременного применения нескольких изменений к диапазону.</span><span class="sxs-lookup"><span data-stu-id="7ef63-113">The following example shows how a font duplicate can be used to apply a number of changes to a range at once.</span></span>


```C++
void ChangeFontNameSizeBold(ITextSelection *pSel)
{
    ITextFont *pFontSel      = NULL
    ITextFont *FontDuplicate = NULL;
    
    // Get ITextFont version of non-duplicated font.
    if (FAILED(pSel->GetFont( &pFontSel))
        return;

    // Duplicate the font.
    pFontSel->GetValue(&pFontDuplicate);
    pFontSel->Release();
    
    if(!pFontDuplicate)
        return;

   // Changes here happen only to the underlying data structure, 
   // such as a CHARFORMAT, in the duplicate - NOT to the actual story text.

    BSTR bstrTemp = UnicodeBstrFromAnsi("Times New Roman");   // Font name
    
    pFontDuplicate->SetName(bstrTemp);
    SysFreeString(bstrTemp);
    
    pFontDuplicate->SetBold(tomTrue);                        // Bold
    pFontDuplicate->SetSize(10.5);                           // 10.5 point font.
    pFontDuplicate->SetAnimation(tomBlackMarchingAnts);

    // Apply the change to text as one change: one screen update, one undo. 
    // You can also apply the font object to different ranges before you free it.
    
    pSel->SetFont(pFontDuplicate);
    
    pFontDuplicate->Release();
    
}
```



## <a name="related-topics"></a><span data-ttu-id="7ef63-114">См. также</span><span class="sxs-lookup"><span data-stu-id="7ef63-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ef63-115">Использование объектной модели текста</span><span class="sxs-lookup"><span data-stu-id="7ef63-115">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="7ef63-116">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="7ef63-116">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="7ef63-117">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="7ef63-117">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




