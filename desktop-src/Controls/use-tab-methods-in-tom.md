---
title: Использование методов Tab в TOM
description: В следующем примере представлены функции C, иллюстрирующие использование методов Tab в объектной модели текста (TOM).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103890344"
---
# <a name="how-to-use-tab-methods-in-tom"></a><span data-ttu-id="2a45b-103">Использование методов Tab в TOM</span><span class="sxs-lookup"><span data-stu-id="2a45b-103">How to Use Tab Methods in TOM</span></span>

<span data-ttu-id="2a45b-104">В следующем примере представлены функции C, иллюстрирующие использование методов Tab в объектной модели текста (TOM).</span><span class="sxs-lookup"><span data-stu-id="2a45b-104">The following example provides C functions that illustrate the use of the tab methods in the Text Object Model (TOM).</span></span> <span data-ttu-id="2a45b-105">Предполагается, что большинство приложений включают панель инструментов, в которой отображается текущее положение и тип вкладок выбранного абзаца.</span><span class="sxs-lookup"><span data-stu-id="2a45b-105">It is assumed that most applications include a toolbar that shows the current position and type of the tabs for the currently selected paragraph.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2a45b-106">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="2a45b-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2a45b-107">Технологии</span><span class="sxs-lookup"><span data-stu-id="2a45b-107">Technologies</span></span>

-   [<span data-ttu-id="2a45b-108">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="2a45b-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2a45b-109">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="2a45b-109">Prerequisites</span></span>

-   <span data-ttu-id="2a45b-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="2a45b-110">C/C++</span></span>
-   <span data-ttu-id="2a45b-111">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="2a45b-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2a45b-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="2a45b-112">Instructions</span></span>

### <a name="use-a-tab-method"></a><span data-ttu-id="2a45b-113">Использование метода Tab</span><span class="sxs-lookup"><span data-stu-id="2a45b-113">Use a Tab Method</span></span>

<span data-ttu-id="2a45b-114">В следующем примере кода показано, как обновить панель инструментов, используя сведения о текущей вкладке.</span><span class="sxs-lookup"><span data-stu-id="2a45b-114">The following code example demonstrates how to update a toolbar with the current tab details.</span></span>


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a><span data-ttu-id="2a45b-115">Копировать сведения вкладки</span><span class="sxs-lookup"><span data-stu-id="2a45b-115">Copy Tab Information</span></span>

<span data-ttu-id="2a45b-116">В следующем примере показано, как скопировать только сведения вкладки из одного интерфейса [**итекстпара**](/windows/desktop/api/Tom/nn-tom-itextpara) в другой.</span><span class="sxs-lookup"><span data-stu-id="2a45b-116">The following example shows how to copy only the tab information from one [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) interface to another.</span></span> <span data-ttu-id="2a45b-117">Он принимает два параметра: **итекстпара** \* *ппарафром* (абзац, из которого нужно скопировать вкладки) и **итекстпара** \* *ппарафром* (абзац, в который копируются вкладки).</span><span class="sxs-lookup"><span data-stu-id="2a45b-117">It takes two parameters: **ITextPara** \* *pParaFrom* (the paragraph from which to copy tabs) and **ITextPara** \* *pParaFrom* (the paragraph to which to copy tabs).</span></span>


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a><span data-ttu-id="2a45b-118">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2a45b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a45b-119">Использование объектной модели текста</span><span class="sxs-lookup"><span data-stu-id="2a45b-119">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="2a45b-120">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="2a45b-120">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="2a45b-121">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="2a45b-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




