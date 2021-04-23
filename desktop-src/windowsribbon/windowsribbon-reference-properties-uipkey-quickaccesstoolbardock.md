---
title: UI_PKEY_QuickAccessToolbarDock
description: Определяет свойство UI \_ PKEY \_ куиккакцесстулбардокк.
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ae48cb9ef2ee665739de2f3aacab197b461665
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413044"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a><span data-ttu-id="a1220-103">UI \_ PKEY \_ куиккакцесстулбардокк</span><span class="sxs-lookup"><span data-stu-id="a1220-103">UI\_PKEY\_QuickAccessToolbarDock</span></span>

<span data-ttu-id="a1220-104">Определяет свойство UI \_ PKEY \_ куиккакцесстулбардокк.</span><span class="sxs-lookup"><span data-stu-id="a1220-104">Identifies the UI\_PKEY\_QuickAccessToolbarDock property.</span></span>

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a><span data-ttu-id="a1220-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1220-105">Remarks</span></span>

<span data-ttu-id="a1220-106">UI \_ PKEY \_ куиккакцесстулбардокк используется приложением для запроса состояния закрепления панели быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="a1220-106">UI\_PKEY\_QuickAccessToolbarDock is used by an application to query the dock-state of the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="a1220-107">Значение свойства находится в перечислении [**\_ Контролдокк пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) .</span><span class="sxs-lookup"><span data-stu-id="a1220-107">The property value is from the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) enumeration.</span></span>



|                         |                                                                                                                                                                                                                                                       |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1220-108">контролдокк пользовательского интерфейса ( \_ \_ вверху)</span><span class="sxs-lookup"><span data-stu-id="a1220-108">UI\_CONTROLDOCK\_TOP</span></span>    | <span data-ttu-id="a1220-109">QAT закрепляется в неклиентской области хост-приложения ленты, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="a1220-109">The QAT is docked in the nonclient area of the Ribbon host application, as shown in the following screen shot.</span></span>![снимок экрана панели быстрого доступа, закрепленной над лентой в неклиентской области.](images/properties/qat-docktop.png)<br/> |
| <span data-ttu-id="a1220-111">\_КОНТРОЛДОКК ИП \_ снизу</span><span class="sxs-lookup"><span data-stu-id="a1220-111">UI\_CONTROLDOCK\_BOTTOM</span></span> | <span data-ttu-id="a1220-112">QAT закрепляется как визуальная панель под лентой, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="a1220-112">The QAT is docked as a visually integral band below the Ribbon, as shown in the following screen shot.</span></span> ![снимок экрана панели быстрого доступа, закрепленной под лентой.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="a1220-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a1220-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1220-115">Свойства ленты</span><span class="sxs-lookup"><span data-stu-id="a1220-115">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

