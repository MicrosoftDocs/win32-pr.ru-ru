---
title: UI_PKEY_ColorType
description: Определяет свойство UI \_ PKEY \_ колортипе.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338228"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="46092-103">UI \_ PKEY \_ колортипе</span><span class="sxs-lookup"><span data-stu-id="46092-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="46092-104">Определяет свойство UI \_ PKEY \_ колортипе.</span><span class="sxs-lookup"><span data-stu-id="46092-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="46092-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46092-105">Remarks</span></span>

<span data-ttu-id="46092-106">UI \_ PKEY \_ колортипе используется приложением для запроса параметра Color элемента управления [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="46092-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="46092-107">Значение свойства находится в перечислении [**\_ Сватчколортипе пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="46092-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46092-108">UI \_ СВАТЧКОЛОРТИПЕ \_ Color</span><span class="sxs-lookup"><span data-stu-id="46092-108">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="46092-109">Приложение должно рассматривать параметр цвета как прозрачный.</span><span class="sxs-lookup"><span data-stu-id="46092-109">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="46092-110">Обычно используется в сочетании с параметром **нет** цветового цвета.</span><span class="sxs-lookup"><span data-stu-id="46092-110">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="46092-111">Пользовательский интерфейс \_ сватчколортипе \_ автоматически</span><span class="sxs-lookup"><span data-stu-id="46092-111">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="46092-112">Приложение должно запрашивать [жетсисколор (цветная \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span><span class="sxs-lookup"><span data-stu-id="46092-112">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="46092-113">Обычно используется в сочетании с параметром **автоматического** цвета.</span><span class="sxs-lookup"><span data-stu-id="46092-113">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="46092-114">сватчколортипе пользовательского интерфейса \_ \_ RGB</span><span class="sxs-lookup"><span data-stu-id="46092-114">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="46092-115">Приложение должно запрашивать [ \_ \_ цвет пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-color.md) для параметра цвета.</span><span class="sxs-lookup"><span data-stu-id="46092-115">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="46092-116">UI \_ PKEY \_ колортипе передается методу обратного вызова [**Иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) при выборе цветовой палитры в [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="46092-116">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46092-117">См. также</span><span class="sxs-lookup"><span data-stu-id="46092-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46092-118">Свойства выбора цвета</span><span class="sxs-lookup"><span data-stu-id="46092-118">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 