---
title: UI_PKEY_FontProperties_Underline
description: Определяет \_ \_ \_ свойство подчеркивания UI PKEY фонтпропертиес.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066027e5f62416667619937eea7dbe493a3ff279
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443785"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="2b984-103">Подчеркивание пользовательского интерфейса \_ PKEY \_ фонтпропертиес \_</span><span class="sxs-lookup"><span data-stu-id="2b984-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="2b984-104">Определяет \_ \_ \_ свойство подчеркивания UI PKEY фонтпропертиес.</span><span class="sxs-lookup"><span data-stu-id="2b984-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="2b984-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="2b984-105">Remarks</span></span>

<span data-ttu-id="2b984-106">Подчеркивание пользовательского интерфейса \_ PKEY \_ фонтпропертиес \_ используется приложением для запроса состояния кнопки **подчеркивания** .</span><span class="sxs-lookup"><span data-stu-id="2b984-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="2b984-107">Значение свойства находится в перечислении [**\_ Фонтундерлине пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) .</span><span class="sxs-lookup"><span data-stu-id="2b984-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="2b984-108">Значение по умолчанию — `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="2b984-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="2b984-109">На следующем снимке экрана показана кнопка **подчеркивания** ленты [**фонтконтрол**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="2b984-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![снимок экрана элемента фонтконтрол с атрибутом ричфонт, для которого установлено значение true.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="2b984-111">В следующей таблице описаны свойства и результат пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2b984-111">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="2b984-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="2b984-112">Property</span></span>                   |       <span data-ttu-id="2b984-113">Результат пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2b984-113">UI Result</span></span>                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="2b984-114">Кнопка **подчеркивания** отключена и может быть задана только приложением.</span><span class="sxs-lookup"><span data-stu-id="2b984-114">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="2b984-115">Кнопка **подчеркивания** не выбрана.</span><span class="sxs-lookup"><span data-stu-id="2b984-115">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="2b984-116">Кнопка **подчеркивания** выбрана.</span><span class="sxs-lookup"><span data-stu-id="2b984-116">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="2b984-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2b984-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b984-118">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="2b984-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="2b984-119">**фонтундерлине пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="2b984-119">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="2b984-120">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="2b984-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 