---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b67e2a099b7ce02b3c94f7c9d799fcdda5e881
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070472"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a><span data-ttu-id="3526a-103">UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг</span><span class="sxs-lookup"><span data-stu-id="3526a-103">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>

<span data-ttu-id="3526a-104">Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг.</span><span class="sxs-lookup"><span data-stu-id="3526a-104">Identifies the UI\_PKEY\_FontProperties\_VerticalPositioning property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a><span data-ttu-id="3526a-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3526a-105">Remarks</span></span>

<span data-ttu-id="3526a-106">UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг используется приложением для запроса значения элементов управления " **надстрочный** " и " **индекс** ".</span><span class="sxs-lookup"><span data-stu-id="3526a-106">UI\_PKEY\_FontProperties\_VerticalPositioning is used by an application to query the value of the **Superscript** and **Subscript** controls.</span></span>

<span data-ttu-id="3526a-107">Значение свойства находится в перечислении [**\_ Фонтвертикалпоситион пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) .</span><span class="sxs-lookup"><span data-stu-id="3526a-107">The property value is from the [**UI\_FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) enumeration.</span></span>

<span data-ttu-id="3526a-108">Значение по умолчанию — `UI_FONTVERTICALPOSITION_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="3526a-108">The default value is `UI_FONTVERTICALPOSITION_NOTSET`.</span></span>

<span data-ttu-id="3526a-109">На следующем снимке экрана показаны кнопки **надстрочных** и **подстрочных индексов** на ленте [**фонтконтрол**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="3526a-109">The following screen shot shows the **Superscript** and **Subscript** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![снимок экрана элемента фонтконтрол с атрибутом ричфонт, для которого установлено значение true.](images/markup/fontcontrol-subsuper.png)

<span data-ttu-id="3526a-111">В следующей таблице описаны свойства и результат пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3526a-111">The following table describes the properties and the UI result.</span></span>



|                                        |                                                                                                |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | <span data-ttu-id="3526a-112">**Верхние** и нижние **индексы** отключены и могут быть установлены только приложением.</span><span class="sxs-lookup"><span data-stu-id="3526a-112">**Superscript** and **Subscript** buttons are disabled and can only be set by the application.</span></span> |
| `UI_FONTVERTICALPOSITION_NOTSET`       | <span data-ttu-id="3526a-113">Кнопки **надстрочных** и **подстрочных индексов** не выбраны.</span><span class="sxs-lookup"><span data-stu-id="3526a-113">**Superscript** and **Subscript** buttons are not selected.</span></span>                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | <span data-ttu-id="3526a-114">Выбрана кнопка **надстрочных знаков** .</span><span class="sxs-lookup"><span data-stu-id="3526a-114">**Superscript** button is selected.</span></span>                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | <span data-ttu-id="3526a-115">Выбрана кнопка **подстрочных индексов** .</span><span class="sxs-lookup"><span data-stu-id="3526a-115">**Subscript** button is selected.</span></span>                                                              |



 

> [!Note]  
> <span data-ttu-id="3526a-116">Невозможно одновременно выбрать **надстрочные** и **подстрочные** кнопки.</span><span class="sxs-lookup"><span data-stu-id="3526a-116">The **Superscript** and **Subscript** buttons cannot both be selected.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3526a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3526a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3526a-118">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="3526a-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="3526a-119">**фонтвертикалпоситион пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="3526a-119">**UI\_FONTVERTICALPOSITION**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[<span data-ttu-id="3526a-120">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="3526a-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 