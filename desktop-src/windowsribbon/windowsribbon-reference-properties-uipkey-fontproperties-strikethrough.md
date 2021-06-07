---
title: UI_PKEY_FontProperties_Strikethrough
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Зачеркнутый.
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b684704fdd90a8dd1b88b14db2b52540b15fccb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443795"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="4bb96-103">Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ Зачеркнутый</span><span class="sxs-lookup"><span data-stu-id="4bb96-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="4bb96-104">Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Зачеркнутый.</span><span class="sxs-lookup"><span data-stu-id="4bb96-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="4bb96-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="4bb96-105">Remarks</span></span>

<span data-ttu-id="4bb96-106">UI \_ PKEY \_ фонтпропертиес \_ Зачеркнутый используется приложением для запроса состояния кнопки **перечеркивания** .</span><span class="sxs-lookup"><span data-stu-id="4bb96-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="4bb96-107">Значение свойства находится в перечислении [**\_ Фонтпропертиес пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="4bb96-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="4bb96-108">Значение по умолчанию — `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="4bb96-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="4bb96-109">На следующем снимке экрана показана кнопка **зачеркивания** ленты [**фонтконтрол**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="4bb96-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![снимок экрана элемента фонтконтрол с атрибутом ричфонт, для которого установлено значение true.](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="4bb96-111">В следующей таблице описаны свойства и результат пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4bb96-111">The following table describes the properties and the UI result.</span></span>



|   <span data-ttu-id="4bb96-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="4bb96-112">Property</span></span>                       |    <span data-ttu-id="4bb96-113">Результат пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4bb96-113">UI Result</span></span>                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="4bb96-114">Кнопка **перечеркивания** отключена и может быть задана только приложением.</span><span class="sxs-lookup"><span data-stu-id="4bb96-114">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="4bb96-115">Кнопка **перечеркивания** не выбрана.</span><span class="sxs-lookup"><span data-stu-id="4bb96-115">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="4bb96-116">Кнопка **перечеркивания** выбрана.</span><span class="sxs-lookup"><span data-stu-id="4bb96-116">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="4bb96-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4bb96-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bb96-118">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="4bb96-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="4bb96-119">**фонтпропертиес пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="4bb96-119">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="4bb96-120">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="4bb96-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 