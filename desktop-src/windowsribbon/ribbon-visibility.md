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
# <a name="displaying-the-ribbon"></a>Отображение ленты

Платформа Windows Ribbon предоставляет набор свойств, позволяющих приложению указать способ отображения ленты во время выполнения.

-   [Введение](#introduction)
-   [Уменьшение ленты](#minimize-the-ribbon)
-   [Скрыть ленту](#hide-the-ribbon)
-   [Пример](#example)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

Чтобы максимально увеличить область, доступную для пространства документа (или порта представления) для приложения платформы Ribbon, приложение может указать, является ли пользовательский интерфейс ленты видимым или скрытым и, когда видим, находится ли лента в развернутом или свернутом состоянии.

[Ключи свойств платформы](windowsribbon-reference-properties-framework.md) , перечисленные в следующей таблице, используются для явного задания отображаемых характеристик ленты в приложении платформы Ribbon. Эти свойства не влияют на отображение всплывающего элемента управления [контекстом](windowsribbon-controls-contextpopup.md) .



| Состояние отображения         | Ключ свойства ленты                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| Развернутый или свернутый | [Пользовательский интерфейс (PKEY) — \_ \_ сведенный](windowsribbon-reference-properties-uipkey-minimized.md) |
| Видимый или скрытый     | [Доступен пользовательский интерфейс \_ PKEY \_](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a>Уменьшение ленты

Приложение платформы Ribbon может динамически задавать состояние панели команд ленты с помощью значения **true** или **false** для параметра неограниченный [Пользовательский интерфейс \_ \_](windowsribbon-reference-properties-uipkey-minimized.md) .



| Состояние отображения | Значение ключа свойства |
|---------------|--------------------|
| Расширенный      | **false**          |
| Свернуто     | **true**           |



 

Когда пользовательский интерфейс ленты находится в режиме сворачивания, строка вкладки ленты остается видимой и полностью функциональной.

На следующем снимке экрана показана лента в состоянии сворачивания.

![снимок экрана с уменьшенным пользовательским интерфейсом ленты.](images/overviews/ribbon-minimized.png)

> [!Note]  
> Платформа Ribbon предоставляет эту функцию конечному пользователю с помощью выбора "сворачивания ленты" в контекстном меню ленты.

 

## <a name="hide-the-ribbon"></a>Скрыть ленту

Приложение платформы Ribbon может динамически задавать отображаемое состояние панели команд ленты, устанавливая значение **true** или **false** для ключа [ \_ \_ отображаемого свойства PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-viewable.md) .



| Состояние отображения | Значение ключа свойства |
|---------------|--------------------|
| Видимый       | **false**          |
| Скрытый        | **true**           |



 

В отличие от свойства [с \_ \_ минимальным пользовательским интерфейсом](windowsribbon-reference-properties-uipkey-minimized.md) , параметр [UI \_ PKEY, \_ видимый](windowsribbon-reference-properties-uipkey-viewable.md) в **значение false** , отображает невидимый пользовательский интерфейс ленты и полностью непригоден для использования конечному пользователю.

На следующем снимке экрана показана лента в скрытом состоянии.

![снимок экрана с скрытым пользовательским интерфейсом ленты.](images/overviews/ribbon-viewable.png)

## <a name="example"></a>Пример

В следующем примере показано, как задать состояние пользовательского интерфейса ленты во время выполнения.

В этом случае функция [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) используется для разворачивания или сворачивания пользовательского интерфейса ленты на основе состояния переключателя [переключателя.](windowsribbon-controls-togglebutton.md)


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства ленты](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 