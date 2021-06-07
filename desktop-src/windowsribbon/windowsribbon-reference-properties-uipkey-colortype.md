---
title: UI_PKEY_ColorType
description: Определяет свойство UI \_ PKEY \_ колортипе.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443895"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="87cf3-103">UI \_ PKEY \_ колортипе</span><span class="sxs-lookup"><span data-stu-id="87cf3-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="87cf3-104">Определяет свойство UI \_ PKEY \_ колортипе.</span><span class="sxs-lookup"><span data-stu-id="87cf3-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="87cf3-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="87cf3-105">Remarks</span></span>

<span data-ttu-id="87cf3-106">UI \_ PKEY \_ колортипе используется приложением для запроса параметра Color элемента управления [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="87cf3-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="87cf3-107">Значение свойства находится в перечислении [**\_ Сватчколортипе пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="87cf3-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|    <span data-ttu-id="87cf3-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="87cf3-108">Property</span></span>                            |    <span data-ttu-id="87cf3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="87cf3-109">Description</span></span>                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87cf3-110">UI \_ СВАТЧКОЛОРТИПЕ \_ Color</span><span class="sxs-lookup"><span data-stu-id="87cf3-110">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="87cf3-111">Приложение должно рассматривать параметр цвета как прозрачный.</span><span class="sxs-lookup"><span data-stu-id="87cf3-111">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="87cf3-112">Обычно используется в сочетании с параметром **нет** цветового цвета.</span><span class="sxs-lookup"><span data-stu-id="87cf3-112">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="87cf3-113">Пользовательский интерфейс \_ сватчколортипе \_ автоматически</span><span class="sxs-lookup"><span data-stu-id="87cf3-113">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="87cf3-114">Приложение должно запрашивать [жетсисколор (цветная \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span><span class="sxs-lookup"><span data-stu-id="87cf3-114">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="87cf3-115">Обычно используется в сочетании с параметром **автоматического** цвета.</span><span class="sxs-lookup"><span data-stu-id="87cf3-115">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="87cf3-116">сватчколортипе пользовательского интерфейса \_ \_ RGB</span><span class="sxs-lookup"><span data-stu-id="87cf3-116">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="87cf3-117">Приложение должно запрашивать [ \_ \_ цвет пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-color.md) для параметра цвета.</span><span class="sxs-lookup"><span data-stu-id="87cf3-117">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="87cf3-118">UI \_ PKEY \_ колортипе передается методу обратного вызова [**Иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) при выборе цветовой палитры в [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="87cf3-118">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="87cf3-119">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="87cf3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87cf3-120">Свойства выбора цвета</span><span class="sxs-lookup"><span data-stu-id="87cf3-120">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 