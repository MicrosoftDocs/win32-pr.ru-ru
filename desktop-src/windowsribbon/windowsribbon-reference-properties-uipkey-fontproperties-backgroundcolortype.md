---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487796"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="065c0-103">UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе</span><span class="sxs-lookup"><span data-stu-id="065c0-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="065c0-104">Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе.</span><span class="sxs-lookup"><span data-stu-id="065c0-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="065c0-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="065c0-105">Remarks</span></span>

<span data-ttu-id="065c0-106">UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе используется приложением в сочетании с [UI \_ PKEY \_ фонтпропертиес \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)для запроса параметров коллекции **цветов выделения текста** .</span><span class="sxs-lookup"><span data-stu-id="065c0-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="065c0-107">Значение свойства находится в перечислении [**\_ Сватчколортипе пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="065c0-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="065c0-108">Значение по умолчанию — `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="065c0-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="065c0-109">В следующей таблице описаны значения свойств.</span><span class="sxs-lookup"><span data-stu-id="065c0-109">The following table describes the property values.</span></span>



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="065c0-110">Приложение должно запрашивать соответствующую метрику системы для значения цвета, как правило, текущего **цвета фона окна** темы Windows, получаемого с помощью жетсисколор ( \_ окно цвета).</span><span class="sxs-lookup"><span data-stu-id="065c0-110">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="065c0-111">Не поддерживается [**фонтконтрол**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="065c0-111">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="065c0-112">Приложение должно запрашивать [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) для значения цвета.</span><span class="sxs-lookup"><span data-stu-id="065c0-112">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="065c0-113">Значение цвета [UI \_ PKEY \_ фонтпропертиес \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) отображается на кнопке **Цвет выделения текста** и выбрано в коллекции **цветов выделения текста** .</span><span class="sxs-lookup"><span data-stu-id="065c0-113">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="065c0-114">UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе передается методу обратного вызова [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) при выборе цвета в коллекции **цветов подсветки текста** [**фонтконтрол**](windowsribbon-element-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="065c0-114">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="065c0-115">Настоятельно рекомендуется, чтобы приложение задали только исходное значение **цвета выделения текста** и не задали его повторно при перемещении курсора в пределах документа.</span><span class="sxs-lookup"><span data-stu-id="065c0-115">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="065c0-116">Последний выбор должен поддерживаться, чтобы избежать необходимости повторно выбирать нужный цвет.</span><span class="sxs-lookup"><span data-stu-id="065c0-116">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="065c0-117">См. также</span><span class="sxs-lookup"><span data-stu-id="065c0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="065c0-118">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="065c0-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="065c0-119">**сватчколортипе пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="065c0-119">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="065c0-120">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="065c0-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

