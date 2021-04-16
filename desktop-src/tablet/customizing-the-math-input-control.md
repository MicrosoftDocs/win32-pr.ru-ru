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
# <a name="customizing-the-math-input-control"></a><span data-ttu-id="6e70f-103">Настройка элемента управления Math input</span><span class="sxs-lookup"><span data-stu-id="6e70f-103">Customizing the Math Input Control</span></span>

<span data-ttu-id="6e70f-104">Можно изменить внешний вид элемента управления математическими вводами, чтобы он лучше подходит для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="6e70f-104">It is possible to change the look and feel of the math input control so that it is better suited to your application.</span></span> <span data-ttu-id="6e70f-105">В этом разделе объясняются различные способы настройки элемента управления для математических входов.</span><span class="sxs-lookup"><span data-stu-id="6e70f-105">This topic explains the various ways that developers can customize the math input control.</span></span>

<span data-ttu-id="6e70f-106">Возможны следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="6e70f-106">The following customizations are possible:</span></span>

-   [<span data-ttu-id="6e70f-107">Изменение отображаемых кнопок</span><span class="sxs-lookup"><span data-stu-id="6e70f-107">Changing the Displayed Buttons</span></span>](#changing-the-displayed-buttons)
-   [<span data-ttu-id="6e70f-108">Изменение заголовка элемента управления</span><span class="sxs-lookup"><span data-stu-id="6e70f-108">Changing the Control Caption</span></span>](#changing-the-control-caption)
-   [<span data-ttu-id="6e70f-109">Изменение размера области просмотра элемента управления</span><span class="sxs-lookup"><span data-stu-id="6e70f-109">Changing the Control's Preview Area Size</span></span>](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a><span data-ttu-id="6e70f-110">Изменение отображаемых кнопок</span><span class="sxs-lookup"><span data-stu-id="6e70f-110">Changing the Displayed Buttons</span></span>

<span data-ttu-id="6e70f-111">Можно изменить кнопки, отображаемые в элементе управления математическими данными, чтобы элемент управления был на экране расширенной функциональности или отображаться меньше.</span><span class="sxs-lookup"><span data-stu-id="6e70f-111">You can change the buttons that are displayed on the math input control so that the control has extended functionality or appears smaller on the screen.</span></span> <span data-ttu-id="6e70f-112">При включении расширенного набора кнопок будут отображаться кнопки **повторить** и **отменить** .</span><span class="sxs-lookup"><span data-stu-id="6e70f-112">Enabling the extended button set will show the **Redo** and **Undo** buttons.</span></span> <span data-ttu-id="6e70f-113">В следующем коде показано, как включить набор расширенных кнопок.</span><span class="sxs-lookup"><span data-stu-id="6e70f-113">The following code shows how to enable the extended button set.</span></span>


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



<span data-ttu-id="6e70f-114">На следующем рисунке показан элемент управления с расширенным набором кнопок.</span><span class="sxs-lookup"><span data-stu-id="6e70f-114">The following image shows the control with the extended set of buttons.</span></span>

![элемент управления Math для ввода с расширенным набором кнопок](images/mic.png)

<span data-ttu-id="6e70f-116">На следующем рисунке показан элемент управления без расширенного набора кнопок.</span><span class="sxs-lookup"><span data-stu-id="6e70f-116">The following image shows the control without the extended set of buttons.</span></span>

![элемент управления Math для ввода без расширенного набора кнопок](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a><span data-ttu-id="6e70f-118">Изменение заголовка элемента управления</span><span class="sxs-lookup"><span data-stu-id="6e70f-118">Changing the Control Caption</span></span>

<span data-ttu-id="6e70f-119">Можно изменить заголовок элемента управления для ввода математических элементов, чтобы задать заголовок для окна элемента управления математическими данными.</span><span class="sxs-lookup"><span data-stu-id="6e70f-119">You can change the control caption for the math input control in order to set the caption on the math input control's window.</span></span> <span data-ttu-id="6e70f-120">В следующем коде показано, как задать заголовок.</span><span class="sxs-lookup"><span data-stu-id="6e70f-120">The following code shows how to set the caption.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



<span data-ttu-id="6e70f-121">На следующем рисунке элемент управления отображается после задания заголовка.</span><span class="sxs-lookup"><span data-stu-id="6e70f-121">The following image shows the control after the caption has been set.</span></span>

![элемент управления математическими данными с набором заголовков](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a><span data-ttu-id="6e70f-123">Изменение размера области просмотра элемента управления</span><span class="sxs-lookup"><span data-stu-id="6e70f-123">Changing the Control's Preview Area Size</span></span>

<span data-ttu-id="6e70f-124">Элемент управления математическими данными можно настроить таким образом, чтобы элемент управления явно задает свой размер области просмотра.</span><span class="sxs-lookup"><span data-stu-id="6e70f-124">You can customize the math input control so that the control explicitly sets its preview-area size.</span></span> <span data-ttu-id="6e70f-125">При этом создается большая область, в которой отображаются математические формулы.</span><span class="sxs-lookup"><span data-stu-id="6e70f-125">This creates a larger area in which the math formulas are displayed.</span></span> <span data-ttu-id="6e70f-126">В следующем коде показано, как задать размер области просмотра.</span><span class="sxs-lookup"><span data-stu-id="6e70f-126">The following code shows how to set the preview area size.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



<span data-ttu-id="6e70f-127">На следующих изображениях показан элемент управления с областями просмотра с разными размерами.</span><span class="sxs-lookup"><span data-stu-id="6e70f-127">The following images show a control with differently sized preview areas.</span></span>

![элемент управления математическим вводом с размером области предварительного просмотра по умолчанию](images/mic.png)![элемент управления Math для ввода с областью более крупного просмотра](images/mic-big-preview.png)

 

 



