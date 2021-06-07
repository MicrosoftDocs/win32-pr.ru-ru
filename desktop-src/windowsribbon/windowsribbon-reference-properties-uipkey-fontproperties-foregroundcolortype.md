---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f261256a36ee7a387c6c3a695d8c1182898690c2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444355"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a><span data-ttu-id="d4b2a-103">UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе</span><span class="sxs-lookup"><span data-stu-id="d4b2a-103">UI\_PKEY\_FontProperties\_ForegroundColorType</span></span>

<span data-ttu-id="d4b2a-104">Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе.</span><span class="sxs-lookup"><span data-stu-id="d4b2a-104">Identifies the UI\_PKEY\_FontProperties\_ForegroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="d4b2a-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="d4b2a-105">Remarks</span></span>

<span data-ttu-id="d4b2a-106">UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе используется приложением в сочетании с [UI \_ PKEY \_ фонтпропертиес \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md)для запроса параметров коллекции **цветов текста** .</span><span class="sxs-lookup"><span data-stu-id="d4b2a-106">UI\_PKEY\_FontProperties\_ForegroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), to query **Text color** gallery settings.</span></span>

<span data-ttu-id="d4b2a-107">Значение свойства находится в перечислении [**\_ Сватчколортипе пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="d4b2a-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="d4b2a-108">Значение по умолчанию — `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="d4b2a-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="d4b2a-109">В следующей таблице описаны значения свойств.</span><span class="sxs-lookup"><span data-stu-id="d4b2a-109">The following table describes the property values.</span></span>



|     <span data-ttu-id="d4b2a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d4b2a-110">Value</span></span>                           |     <span data-ttu-id="d4b2a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d4b2a-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="d4b2a-112">Не поддерживается [**фонтконтрол**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="d4b2a-112">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="d4b2a-113">Приложение должно запрашивать соответствующую метрику системы для значения цвета, как правило, текущего **цвета текста** темы Windows, получаемого с помощью ЖЕТСИСКОЛОР (цветная \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="d4b2a-113">Application should query the appropriate system metric for the color value typically the current Windows theme **text color** that is retrieved with GetSysColor(COLOR\_WINDOWTEXT).</span></span>                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="d4b2a-114">Приложение должно запрашивать [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) для значения цвета.</span><span class="sxs-lookup"><span data-stu-id="d4b2a-114">Application should query [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) for the color value.</span></span> <span data-ttu-id="d4b2a-115">Значение цвета [UI \_ PKEY \_ фонтпропертиес \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) отображается на кнопке **Цвет текста** и выбирается в коллекции **цветов текста** .</span><span class="sxs-lookup"><span data-stu-id="d4b2a-115">The color value of [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) is displayed on the **Text color** button and selected in the **Text color** gallery.</span></span><br/> |



 

<span data-ttu-id="d4b2a-116">UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе передается методу обратного вызова [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) при выборе цвета в коллекции **цветов текста** [**фонтконтрол**](windowsribbon-element-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="d4b2a-116">UI\_PKEY\_FontProperties\_ForegroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="d4b2a-117">Настоятельно рекомендуется, чтобы приложение задали только исходное значение **цвета текста** и не задали его повторно при перемещении курсора в пределах документа.</span><span class="sxs-lookup"><span data-stu-id="d4b2a-117">It is highly recommended that the application only set an initial **Text color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="d4b2a-118">Последний выбор должен поддерживаться, чтобы избежать необходимости повторно выбирать нужный цвет.</span><span class="sxs-lookup"><span data-stu-id="d4b2a-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d4b2a-119">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d4b2a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4b2a-120">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="d4b2a-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="d4b2a-121">**сватчколортипе пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="d4b2a-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="d4b2a-122">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="d4b2a-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

