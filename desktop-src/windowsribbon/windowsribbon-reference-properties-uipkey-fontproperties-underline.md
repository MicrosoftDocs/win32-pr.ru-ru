---
title: UI_PKEY_FontProperties_Underline
description: Определяет \_ \_ \_ свойство подчеркивания UI PKEY фонтпропертиес.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 380c3fdadb636775f80b789a585c42ff2369234a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487956"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="ee4f2-103">Подчеркивание пользовательского интерфейса \_ PKEY \_ фонтпропертиес \_</span><span class="sxs-lookup"><span data-stu-id="ee4f2-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="ee4f2-104">Определяет \_ \_ \_ свойство подчеркивания UI PKEY фонтпропертиес.</span><span class="sxs-lookup"><span data-stu-id="ee4f2-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="ee4f2-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee4f2-105">Remarks</span></span>

<span data-ttu-id="ee4f2-106">Подчеркивание пользовательского интерфейса \_ PKEY \_ фонтпропертиес \_ используется приложением для запроса состояния кнопки **подчеркивания** .</span><span class="sxs-lookup"><span data-stu-id="ee4f2-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="ee4f2-107">Значение свойства находится в перечислении [**\_ Фонтундерлине пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) .</span><span class="sxs-lookup"><span data-stu-id="ee4f2-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="ee4f2-108">Значение по умолчанию — `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="ee4f2-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="ee4f2-109">На следующем снимке экрана показана кнопка **подчеркивания** ленты [**фонтконтрол**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="ee4f2-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![снимок экрана элемента фонтконтрол с атрибутом ричфонт, для которого установлено значение true.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="ee4f2-111">В следующей таблице описаны свойства и результат пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ee4f2-111">The following table describes the properties and the UI result.</span></span>



|                                 |                                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="ee4f2-112">Кнопка **подчеркивания** отключена и может быть задана только приложением.</span><span class="sxs-lookup"><span data-stu-id="ee4f2-112">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="ee4f2-113">Кнопка **подчеркивания** не выбрана.</span><span class="sxs-lookup"><span data-stu-id="ee4f2-113">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="ee4f2-114">Кнопка **подчеркивания** выбрана.</span><span class="sxs-lookup"><span data-stu-id="ee4f2-114">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="ee4f2-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ee4f2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee4f2-116">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="ee4f2-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="ee4f2-117">**фонтундерлине пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="ee4f2-117">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="ee4f2-118">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="ee4f2-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 