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
# <a name="how-to-use-tab-methods-in-tom"></a>Использование методов Tab в TOM

В следующем примере представлены функции C, иллюстрирующие использование методов Tab в объектной модели текста (TOM). Предполагается, что большинство приложений включают панель инструментов, в которой отображается текущее положение и тип вкладок выбранного абзаца.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="use-a-tab-method"></a>Использование метода Tab

В следующем примере кода показано, как обновить панель инструментов, используя сведения о текущей вкладке.


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



### <a name="copy-tab-information"></a>Копировать сведения вкладки

В следующем примере показано, как скопировать только сведения вкладки из одного интерфейса [**итекстпара**](/windows/desktop/api/Tom/nn-tom-itextpara) в другой. Он принимает два параметра: **итекстпара** \* *ппарафром* (абзац, из которого нужно скопировать вкладки) и **итекстпара** \* *ппарафром* (абзац, в который копируются вкладки).


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование объектной модели текста](using-the-text-object-model.md)
</dt> <dt>

[Использование элементов управления Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




