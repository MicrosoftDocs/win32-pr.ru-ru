---
title: UI_PKEY_FontProperties_Bold
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Bold.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444385"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="100fe-103">Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ Bold</span><span class="sxs-lookup"><span data-stu-id="100fe-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="100fe-104">Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Bold.</span><span class="sxs-lookup"><span data-stu-id="100fe-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="100fe-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="100fe-105">Remarks</span></span>

<span data-ttu-id="100fe-106">UI \_ PKEY \_ фонтпропертиес \_ Bold используется приложением для запроса состояния кнопки **полужирный** .</span><span class="sxs-lookup"><span data-stu-id="100fe-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="100fe-107">Значение свойства находится в перечислении [**\_ Фонтпропертиес пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="100fe-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="100fe-108">Значение по умолчанию — `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="100fe-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="100fe-109">В следующей таблице описаны свойства и результат пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="100fe-109">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="100fe-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="100fe-110">Property</span></span>                    |    <span data-ttu-id="100fe-111">Результат пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="100fe-111">UI Result</span></span>                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="100fe-112">Кнопка **полужирного начертания** отключена и может быть установлена только приложением.</span><span class="sxs-lookup"><span data-stu-id="100fe-112">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="100fe-113">Кнопка **полужирного шрифта** не выбрана.</span><span class="sxs-lookup"><span data-stu-id="100fe-113">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="100fe-114">Выбрана **Полужирная** кнопка.</span><span class="sxs-lookup"><span data-stu-id="100fe-114">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="100fe-115">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="100fe-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="100fe-116">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="100fe-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="100fe-117">**фонтпропертиес пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="100fe-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="100fe-118">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="100fe-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 