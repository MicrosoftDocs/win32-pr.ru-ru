---
title: Отображение ленты
description: Платформа Windows Ribbon предоставляет набор свойств, позволяющих приложению указать способ отображения ленты во время выполнения.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Лента Windows, Настройка цветов
- Лента, Настройка цветов
- Настройка цветов ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090c77c5b47afd673bc7132a87e3de336683d876
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070296"
---
# <a name="displaying-the-ribbon"></a><span data-ttu-id="d6e3b-106">Отображение ленты</span><span class="sxs-lookup"><span data-stu-id="d6e3b-106">Displaying the Ribbon</span></span>

<span data-ttu-id="d6e3b-107">Платформа Windows Ribbon предоставляет набор свойств, позволяющих приложению указать способ отображения ленты во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-107">The Windows Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon UI is displayed at run time.</span></span>

-   [<span data-ttu-id="d6e3b-108">Введение</span><span class="sxs-lookup"><span data-stu-id="d6e3b-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d6e3b-109">Уменьшение ленты</span><span class="sxs-lookup"><span data-stu-id="d6e3b-109">Minimize the Ribbon</span></span>](#minimize-the-ribbon)
-   [<span data-ttu-id="d6e3b-110">Скрыть ленту</span><span class="sxs-lookup"><span data-stu-id="d6e3b-110">Hide the Ribbon</span></span>](#hide-the-ribbon)
-   [<span data-ttu-id="d6e3b-111">Пример</span><span class="sxs-lookup"><span data-stu-id="d6e3b-111">Example</span></span>](#example)
-   [<span data-ttu-id="d6e3b-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d6e3b-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="d6e3b-113">Введение</span><span class="sxs-lookup"><span data-stu-id="d6e3b-113">Introduction</span></span>

<span data-ttu-id="d6e3b-114">Чтобы максимально увеличить область, доступную для пространства документа (или порта представления) для приложения платформы Ribbon, приложение может указать, является ли пользовательский интерфейс ленты видимым или скрытым и, когда видим, находится ли лента в развернутом или свернутом состоянии.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-114">To maximize the area available for the document space (or view port) of a Ribbon framework application, an application can specify whether the ribbon UI is visible or hidden and, when visible, whether the ribbon is in an expanded or collapsed state.</span></span>

<span data-ttu-id="d6e3b-115">[Ключи свойств платформы](windowsribbon-reference-properties-framework.md) , перечисленные в следующей таблице, используются для явного задания отображаемых характеристик ленты в приложении платформы Ribbon.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-115">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to explicitly set the display characteristics of the ribbon UI in a Ribbon framework application.</span></span> <span data-ttu-id="d6e3b-116">Эти свойства не влияют на отображение всплывающего элемента управления [контекстом](windowsribbon-controls-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="d6e3b-116">These properties have no effect on the display of the [Context Popup](windowsribbon-controls-contextpopup.md) control.</span></span>



| <span data-ttu-id="d6e3b-117">Состояние отображения</span><span class="sxs-lookup"><span data-stu-id="d6e3b-117">Display State</span></span>         | <span data-ttu-id="d6e3b-118">Ключ свойства ленты</span><span class="sxs-lookup"><span data-stu-id="d6e3b-118">Ribbon Property Key</span></span>                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d6e3b-119">Развернутый или свернутый</span><span class="sxs-lookup"><span data-stu-id="d6e3b-119">Expanded or collapsed</span></span> | [<span data-ttu-id="d6e3b-120">Пользовательский интерфейс (PKEY) — \_ \_ сведенный</span><span class="sxs-lookup"><span data-stu-id="d6e3b-120">UI\_PKEY\_Minimized</span></span>](windowsribbon-reference-properties-uipkey-minimized.md) |
| <span data-ttu-id="d6e3b-121">Видимый или скрытый</span><span class="sxs-lookup"><span data-stu-id="d6e3b-121">Visible or hidden</span></span>     | [<span data-ttu-id="d6e3b-122">Доступен пользовательский интерфейс \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="d6e3b-122">UI\_PKEY\_Viewable</span></span>](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a><span data-ttu-id="d6e3b-123">Уменьшение ленты</span><span class="sxs-lookup"><span data-stu-id="d6e3b-123">Minimize the Ribbon</span></span>

<span data-ttu-id="d6e3b-124">Приложение платформы Ribbon может динамически задавать состояние панели команд ленты с помощью значения **true** или **false** для параметра неограниченный [Пользовательский интерфейс \_ \_](windowsribbon-reference-properties-uipkey-minimized.md) .</span><span class="sxs-lookup"><span data-stu-id="d6e3b-124">A Ribbon framework application can dynamically set the minimized state of the ribbon command bar by setting the value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="d6e3b-125">Состояние отображения</span><span class="sxs-lookup"><span data-stu-id="d6e3b-125">Display State</span></span> | <span data-ttu-id="d6e3b-126">Значение ключа свойства</span><span class="sxs-lookup"><span data-stu-id="d6e3b-126">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="d6e3b-127">Расширенный</span><span class="sxs-lookup"><span data-stu-id="d6e3b-127">Expanded</span></span>      | <span data-ttu-id="d6e3b-128">**false**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-128">**false**</span></span>          |
| <span data-ttu-id="d6e3b-129">Свернуто</span><span class="sxs-lookup"><span data-stu-id="d6e3b-129">Collapsed</span></span>     | <span data-ttu-id="d6e3b-130">**true**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-130">**true**</span></span>           |



 

<span data-ttu-id="d6e3b-131">Когда пользовательский интерфейс ленты находится в режиме сворачивания, строка вкладки ленты остается видимой и полностью функциональной.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-131">When the ribbon UI is in a minimized state, the ribbon Tab row remains visible and fully functional.</span></span>

<span data-ttu-id="d6e3b-132">На следующем снимке экрана показана лента в состоянии сворачивания.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-132">The following screen shot shows the ribbon in the minimized state.</span></span>

![снимок экрана с уменьшенным пользовательским интерфейсом ленты.](images/overviews/ribbon-minimized.png)

> [!Note]  
> <span data-ttu-id="d6e3b-134">Платформа Ribbon предоставляет эту функцию конечному пользователю с помощью выбора "сворачивания ленты" в контекстном меню ленты.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-134">The Ribbon framework exposes this functionality to the end user through the "Minimize the Ribbon" selection of the ribbon context menu.</span></span>

 

## <a name="hide-the-ribbon"></a><span data-ttu-id="d6e3b-135">Скрыть ленту</span><span class="sxs-lookup"><span data-stu-id="d6e3b-135">Hide the Ribbon</span></span>

<span data-ttu-id="d6e3b-136">Приложение платформы Ribbon может динамически задавать отображаемое состояние панели команд ленты, устанавливая значение **true** или **false** для ключа [ \_ \_ отображаемого свойства PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-viewable.md) .</span><span class="sxs-lookup"><span data-stu-id="d6e3b-136">A Ribbon framework application can dynamically set the viewable state of the ribbon command bar by setting the value of the [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="d6e3b-137">Состояние отображения</span><span class="sxs-lookup"><span data-stu-id="d6e3b-137">Display State</span></span> | <span data-ttu-id="d6e3b-138">Значение ключа свойства</span><span class="sxs-lookup"><span data-stu-id="d6e3b-138">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="d6e3b-139">Видимый</span><span class="sxs-lookup"><span data-stu-id="d6e3b-139">Visible</span></span>       | <span data-ttu-id="d6e3b-140">**false**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-140">**false**</span></span>          |
| <span data-ttu-id="d6e3b-141">Скрытый</span><span class="sxs-lookup"><span data-stu-id="d6e3b-141">Hidden</span></span>        | <span data-ttu-id="d6e3b-142">**true**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-142">**true**</span></span>           |



 

<span data-ttu-id="d6e3b-143">В отличие от свойства [с \_ \_ минимальным пользовательским интерфейсом](windowsribbon-reference-properties-uipkey-minimized.md) , параметр [UI \_ PKEY, \_ видимый](windowsribbon-reference-properties-uipkey-viewable.md) в **значение false** , отображает невидимый пользовательский интерфейс ленты и полностью непригоден для использования конечному пользователю.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-143">In contrast to the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property, setting [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) to **false** renders the ribbon UI invisible and completely unusable to an end user.</span></span>

<span data-ttu-id="d6e3b-144">На следующем снимке экрана показана лента в скрытом состоянии.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-144">The following screen shot shows the ribbon in the hidden state.</span></span>

![снимок экрана с скрытым пользовательским интерфейсом ленты.](images/overviews/ribbon-viewable.png)

## <a name="example"></a><span data-ttu-id="d6e3b-146">Пример</span><span class="sxs-lookup"><span data-stu-id="d6e3b-146">Example</span></span>

<span data-ttu-id="d6e3b-147">В следующем примере показано, как задать состояние пользовательского интерфейса ленты во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-147">The following example demonstrates how to set the state of the ribbon UI at run time.</span></span>

<span data-ttu-id="d6e3b-148">В этом случае функция [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) используется для разворачивания или сворачивания пользовательского интерфейса ленты на основе состояния переключателя [переключателя.](windowsribbon-controls-togglebutton.md)</span><span class="sxs-lookup"><span data-stu-id="d6e3b-148">In this case, the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) function is used to expand or collapse the ribbon UI based on the toggle state of a [Toggle Button](windowsribbon-controls-togglebutton.md).</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d6e3b-149">См. также</span><span class="sxs-lookup"><span data-stu-id="d6e3b-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6e3b-150">Свойства ленты</span><span class="sxs-lookup"><span data-stu-id="d6e3b-150">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 