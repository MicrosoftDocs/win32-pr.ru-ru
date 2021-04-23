---
title: Spinner
description: Счетчик представляет собой составной элемент управления, состоящий из кнопки инкремента, кнопки декремента и элемента управления Edit, который используется для предоставления приложению десятичных значений.
ms.assetid: 63689ed3-7326-4f7a-b700-d89e9b501ef1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0875fb31d0dac73c88f3bd502746c473dc1c2b1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "105691689"
---
# <a name="spinner"></a><span data-ttu-id="907fa-103">Spinner</span><span class="sxs-lookup"><span data-stu-id="907fa-103">Spinner</span></span>

<span data-ttu-id="907fa-104">Счетчик представляет собой составной элемент управления, состоящий из кнопки инкремента, кнопки декремента и элемента управления Edit, который используется для предоставления приложению десятичных значений.</span><span class="sxs-lookup"><span data-stu-id="907fa-104">The Spinner is a composite control that consists of an increment button, a decrement button, and an edit control, all of which are used to provide decimal values to the application.</span></span>

-   [<span data-ttu-id="907fa-105">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="907fa-105">Details</span></span>](#details)
-   [<span data-ttu-id="907fa-106">Свойства счетчика</span><span class="sxs-lookup"><span data-stu-id="907fa-106">Spinner Properties</span></span>](#spinner-properties)
-   [<span data-ttu-id="907fa-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="907fa-107">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="907fa-108">См. также</span><span class="sxs-lookup"><span data-stu-id="907fa-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="907fa-109">Сведения</span><span class="sxs-lookup"><span data-stu-id="907fa-109">Details</span></span>

<span data-ttu-id="907fa-110">На следующем снимке экрана показана центрифуга на ленте.</span><span class="sxs-lookup"><span data-stu-id="907fa-110">The following screen shot illustrates the Ribbon Spinner.</span></span>

![снимок экрана элемента управления "Счетчик" на ленте Windows Live кинорежиссер.](images/controls/spinner.png)

## <a name="spinner-properties"></a><span data-ttu-id="907fa-112">Свойства счетчика</span><span class="sxs-lookup"><span data-stu-id="907fa-112">Spinner Properties</span></span>

<span data-ttu-id="907fa-113">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "Счетчик".</span><span class="sxs-lookup"><span data-stu-id="907fa-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Spinner control.</span></span>

<span data-ttu-id="907fa-114">Как правило, свойство счетчика обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="907fa-114">Typically, a Spinner property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="907fa-115">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="907fa-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="907fa-116">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="907fa-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="907fa-117">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="907fa-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="907fa-118">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="907fa-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="907fa-119">В следующей таблице перечислены ключи свойств, связанные с элементом управления "Счетчик".</span><span class="sxs-lookup"><span data-stu-id="907fa-119">The following table lists the property keys that are associated with the Spinner control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="907fa-120">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="907fa-120">Property Key</span></span></th>
<th><span data-ttu-id="907fa-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="907fa-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="907fa-122"><a href="windowsribbon-reference-properties-uipkey-decimalplaces.md">UI_PKEY_DecimalPlaces</a></span><span class="sxs-lookup"><span data-stu-id="907fa-122"><a href="windowsribbon-reference-properties-uipkey-decimalplaces.md">UI_PKEY_DecimalPlaces</a></span></span></td>
<td><span data-ttu-id="907fa-123">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-123">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="907fa-124"><a href="windowsribbon-reference-properties-uipkey-decimalvalue.md">UI_PKEY_DecimalValue</a></span><span class="sxs-lookup"><span data-stu-id="907fa-124"><a href="windowsribbon-reference-properties-uipkey-decimalvalue.md">UI_PKEY_DecimalValue</a></span></span></td>
<td><span data-ttu-id="907fa-125">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="907fa-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="907fa-126">Если команда, связанная с элементом управления, становится недействительной при вызове <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>иуифрамеворк:: инвалидатеуикомманд</strong></a>, платформа запрашивает это свойство, когда в <code>UI_INVALIDATIONS_VALUE</code> качестве значения <em>флагов</em>передается.</span><span class="sxs-lookup"><span data-stu-id="907fa-126">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="907fa-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="907fa-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="907fa-128">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="907fa-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="907fa-129"><a href="windowsribbon-reference-properties-uipkey-formatstring.md">UI_PKEY_FormatString</a></span><span class="sxs-lookup"><span data-stu-id="907fa-129"><a href="windowsribbon-reference-properties-uipkey-formatstring.md">UI_PKEY_FormatString</a></span></span></td>
<td><span data-ttu-id="907fa-130">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="907fa-131"><a href="windowsribbon-reference-properties-uipkey-increment.md">UI_PKEY_Increment</a></span><span class="sxs-lookup"><span data-stu-id="907fa-131"><a href="windowsribbon-reference-properties-uipkey-increment.md">UI_PKEY_Increment</a></span></span></td>
<td><span data-ttu-id="907fa-132">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="907fa-133"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="907fa-133"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="907fa-134">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="907fa-135"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="907fa-135"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="907fa-136">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="907fa-137"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="907fa-137"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="907fa-138">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-138">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="907fa-139"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="907fa-139"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="907fa-140">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-140">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="907fa-141"><a href="windowsribbon-reference-properties-uipkey-maxvalue.md">UI_PKEY_MaxValue</a></span><span class="sxs-lookup"><span data-stu-id="907fa-141"><a href="windowsribbon-reference-properties-uipkey-maxvalue.md">UI_PKEY_MaxValue</a></span></span></td>
<td><span data-ttu-id="907fa-142">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-142">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="907fa-143"><a href="windowsribbon-reference-properties-uipkey-minvalue.md">UI_PKEY_MinValue</a></span><span class="sxs-lookup"><span data-stu-id="907fa-143"><a href="windowsribbon-reference-properties-uipkey-minvalue.md">UI_PKEY_MinValue</a></span></span></td>
<td><span data-ttu-id="907fa-144">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="907fa-145"><a href="windowsribbon-reference-properties-uipkey-representativestring.md">UI_PKEY_RepresentativeString</a></span><span class="sxs-lookup"><span data-stu-id="907fa-145"><a href="windowsribbon-reference-properties-uipkey-representativestring.md">UI_PKEY_RepresentativeString</a></span></span></td>
<td><span data-ttu-id="907fa-146">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="907fa-147"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="907fa-147"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="907fa-148">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-148">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="907fa-149"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="907fa-149"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="907fa-150">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-150">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="907fa-151"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="907fa-151"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="907fa-152">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-152">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="907fa-153"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="907fa-153"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="907fa-154">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="907fa-154">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="907fa-155">В следующем разделе кода показано, как обновляются различные свойства элемента управления "Счетчик" в методе [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="907fa-155">The following section of code demonstrates how various properties of the Spinner control are updated in the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method.</span></span>


```C++
//
//  FUNCTION:    UpdateProperty()
//
//  PURPOSE:    Called by the Ribbon framework when a command property needs 
//                to be updated.
//
//  COMMENTS:    This function is used to provide new command property values for 
//                the spinner when requested by the Ribbon framework.  
//    
STDMETHODIMP CCommandHandler::UpdateProperty(
    UINT nCmdID,
    REFPROPERTYKEY key,
    const PROPVARIANT* ppropvarCurrentValue,
    PROPVARIANT* ppropvarNewValue)
{
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;

    if (nCmdID == IDR_CMD_SPINNER_RESIZE)
    {
        // Set the minimum value
        if (IsEqualPropertyKey(key, UI_PKEY_MinValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(-10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the maximum value
        else if (IsEqualPropertyKey(key, UI_PKEY_MaxValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the increment
        else if (IsEqualPropertyKey(key, UI_PKEY_Increment))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(2.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the number of decimal places
        else if (IsEqualPropertyKey(key, UI_PKEY_DecimalPlaces))
        {
            hr = InitPropVariantFromUInt32(1, ppropvarNewValue);
            hr = S_OK;
        }

        // Set the format string
        else if (IsEqualPropertyKey(key, UI_PKEY_FormatString))
        {
            hr = InitPropVariantFromString(L"px", ppropvarNewValue);
            hr = S_OK;
        }

        // Set the representative string
        else if (IsEqualPropertyKey(key, UI_PKEY_RepresentativeString))
        {
            hr = InitPropVariantFromString(L"AAAAAAA", ppropvarNewValue);
            hr = S_OK;
        }
    }
    return hr;
}
```



## <a name="remarks"></a><span data-ttu-id="907fa-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="907fa-156">Remarks</span></span>

<span data-ttu-id="907fa-157">Если минимальное значение ([UI \_ PKEY класса \_ MinValue](windowsribbon-reference-properties-uipkey-minvalue.md)) для счетчика инициализируется значением 0,0, приложение должно гарантировать, что любое последующее значение, предоставленное элементом управления, не будет равно-0,0 (отрицательный нуль).</span><span class="sxs-lookup"><span data-stu-id="907fa-157">If the minimum value ([UI\_PKEY\_MinValue](windowsribbon-reference-properties-uipkey-minvalue.md)) of a Spinner is initialized to 0.0, the application should ensure that any subsequent value supplied by the control does not equal -0.0 (negative zero).</span></span> <span data-ttu-id="907fa-158">Если счетчик предоставляет значение-0,0, приложение должно сбросить это значение до 0,0 (положительный нуль), используя метод [**иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , как показано в следующем примере метода [**Иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) для элемента управления "Счетчик".</span><span class="sxs-lookup"><span data-stu-id="907fa-158">If the Spinner supplies a value of -0.0, the application should reset this value to 0.0 (positive zero) using the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method as shown in the following example of an [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method for a Spinner control.</span></span>

> [!Note]  
> <span data-ttu-id="907fa-159">Если этот тест не выполняется и значение остается неисправленным, в поле редактирования элемента управления отображается строка "Auto".</span><span class="sxs-lookup"><span data-stu-id="907fa-159">If this test is not performed and the value left uncorrected, the edit field of the control displays the string "Auto".</span></span>

 


```C++
//
//  FUNCTION:    Execute()
//
//  PURPOSE:    Called by the Ribbon framework when a command is executed by the user.  
//                For this sample, when an increment or decrement button is pressed or
//                a new value is entered in the Spinner edit field.
//
STDMETHODIMP CCommandHandler::Execute(
      UINT nCmdID,
      UI_EXECUTIONVERB verb,
      const PROPERTYKEY* key,
      const PROPVARIANT* ppropvarValue,
      IUISimplePropertySet* pCommandExecutionProperties)
{
    UNREFERENCED_PARAMETER(pCommandExecutionProperties);

    HRESULT hr = E_NOTIMPL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        RenderParam param;
        g_renderer.GetRenderParam(&param);

        if (nCmdID == IDR_CMD_SPINNER_RESIZE)
        {
            // Spinner value is negative.
            if (!(ppropvarValue->decVal.sign == 0))
            {
                // Check if the value supplied by the Spinner is -0
                // and correct the value if necessary.
                // If this value is left uncorrected, the edit field 
                // of the control will display the string "Auto" when 
                // UI_PKEY_MinValue is set to 0.
                if (ppropvarValue->decVal.Lo64 == 0)
                {
                    // Initialize a new PROPVARIANT structure.
                    PROPVARIANT m_varNewVal;
                    PropVariantInit(&m_varNewVal);

                    // The replacement DECIMAL value.
                    DECIMAL m_dVal;
                    hr = VarDecFromI4(0, &m_dVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                    
                    // Initialize the new DECIMAL value.
                    UIInitPropertyFromDecimal(UI_PKEY_DecimalValue, m_dVal, &m_varNewVal);

                    // Set the UI_PKEY_DecimalValue to the new DECIMAL value.
                    hr = g_pFramework->SetUICommandProperty(nCmdID, UI_PKEY_DecimalValue, m_varNewVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                }
                // Decrease size of shape in document space.
                param.iShapeSizeIncrement = -ppropvarValue->intVal;
            }
            // Spinner value is positive.
            else
            {
                // Increase size of shape in document space.
                param.iShapeSizeIncrement = ppropvarValue->intVal;
            }
        }
        g_renderer.UpdateRenderParam(param);
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="907fa-160">См. также</span><span class="sxs-lookup"><span data-stu-id="907fa-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="907fa-161">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="907fa-161">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="907fa-162">**Элемент разметки счетчика**</span><span class="sxs-lookup"><span data-stu-id="907fa-162">**Spinner markup element**</span></span>](windowsribbon-element-spinner.md)
</dt> </dl>

