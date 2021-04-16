---
description: Объясняет, как изменить внешний вид элемента управления вводом математических символов.
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: Настройка элемента управления Math input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3cab7c6efe003738c46a89d07866fcc9302ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566867"
---
# <a name="customizing-the-math-input-control"></a>Настройка элемента управления Math input

Можно изменить внешний вид элемента управления математическими вводами, чтобы он лучше подходит для вашего приложения. В этом разделе объясняются различные способы настройки элемента управления для математических входов.

Возможны следующие настройки:

-   [Изменение отображаемых кнопок](#changing-the-displayed-buttons)
-   [Изменение заголовка элемента управления](#changing-the-control-caption)
-   [Изменение размера области просмотра элемента управления](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a>Изменение отображаемых кнопок

Можно изменить кнопки, отображаемые в элементе управления математическими данными, чтобы элемент управления был на экране расширенной функциональности или отображаться меньше. При включении расширенного набора кнопок будут отображаться кнопки **повторить** и **отменить** . В следующем коде показано, как включить набор расширенных кнопок.


```
  void CMath_Input_Control_testDlg::OnBnClickedToggleBtns()
  {
    static bool enabled = true;
    HRESULT hr = S_OK;

    hr = g_spMIC->Hide();    
    if(!enabled){
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
        enabled = true;
      }
    }else{
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_FALSE);
        enabled = false;
      }
    }
    if (SUCCEEDED(hr)){
      hr = g_spMIC->Show();
    }
  }
  
```



На следующем рисунке показан элемент управления с расширенным набором кнопок.

![элемент управления Math для ввода с расширенным набором кнопок](images/mic.png)

На следующем рисунке показан элемент управления без расширенного набора кнопок.

![элемент управления Math для ввода без расширенного набора кнопок](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a>Изменение заголовка элемента управления

Можно изменить заголовок элемента управления для ввода математических элементов, чтобы задать заголовок для окна элемента управления математическими данными. В следующем коде показано, как задать заголовок.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



На следующем рисунке элемент управления отображается после задания заголовка.

![элемент управления математическими данными с набором заголовков](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a>Изменение размера области просмотра элемента управления

Элемент управления математическими данными можно настроить таким образом, чтобы элемент управления явно задает свой размер области просмотра. При этом создается большая область, в которой отображаются математические формулы. В следующем коде показано, как задать размер области просмотра.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



На следующих изображениях показан элемент управления с областями просмотра с разными размерами.

![элемент управления математическим вводом с размером области предварительного просмотра по умолчанию](images/mic.png)![элемент управления Math для ввода с областью более крупного просмотра](images/mic-big-preview.png)

 

 



