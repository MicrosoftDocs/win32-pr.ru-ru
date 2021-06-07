---
title: UI_PKEY_FontProperties_Italic
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Italic.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443815"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="3c848-103">Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ курсивом</span><span class="sxs-lookup"><span data-stu-id="3c848-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="3c848-104">Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Italic.</span><span class="sxs-lookup"><span data-stu-id="3c848-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="3c848-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="3c848-105">Remarks</span></span>

<span data-ttu-id="3c848-106">UI \_ PKEY \_ фонтпропертиес \_ Italic используется приложением для запроса состояния кнопки **курсив** .</span><span class="sxs-lookup"><span data-stu-id="3c848-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="3c848-107">Значение свойства находится в перечислении [**\_ Фонтпропертиес пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="3c848-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="3c848-108">Значение по умолчанию — `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="3c848-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="3c848-109">В следующей таблице описаны свойства и результат пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3c848-109">The following table describes the properties and the UI result.</span></span>



|    <span data-ttu-id="3c848-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="3c848-110">Property</span></span>                      |       <span data-ttu-id="3c848-111">Результат пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="3c848-111">UI Result</span></span>                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="3c848-112">Кнопка с **курсивом** отключена и может быть установлена только приложением.</span><span class="sxs-lookup"><span data-stu-id="3c848-112">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="3c848-113">Кнопка с **курсивом** не выбрана.</span><span class="sxs-lookup"><span data-stu-id="3c848-113">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="3c848-114">Выбрана **курсивная** кнопка.</span><span class="sxs-lookup"><span data-stu-id="3c848-114">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="3c848-115">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3c848-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c848-116">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="3c848-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="3c848-117">**фонтпропертиес пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="3c848-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="3c848-118">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="3c848-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 