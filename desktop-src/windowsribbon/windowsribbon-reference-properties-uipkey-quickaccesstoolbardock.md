---
title: UI_PKEY_QuickAccessToolbarDock
description: Определяет свойство UI \_ PKEY \_ куиккакцесстулбардокк.
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e28ec2e153755fd243bf78ee389cad40485a348
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443765"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a><span data-ttu-id="09a93-103">UI \_ PKEY \_ куиккакцесстулбардокк</span><span class="sxs-lookup"><span data-stu-id="09a93-103">UI\_PKEY\_QuickAccessToolbarDock</span></span>

<span data-ttu-id="09a93-104">Определяет свойство UI \_ PKEY \_ куиккакцесстулбардокк.</span><span class="sxs-lookup"><span data-stu-id="09a93-104">Identifies the UI\_PKEY\_QuickAccessToolbarDock property.</span></span>

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a><span data-ttu-id="09a93-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="09a93-105">Remarks</span></span>

<span data-ttu-id="09a93-106">UI \_ PKEY \_ куиккакцесстулбардокк используется приложением для запроса состояния закрепления панели быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="09a93-106">UI\_PKEY\_QuickAccessToolbarDock is used by an application to query the dock-state of the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="09a93-107">Значение свойства находится в перечислении [**\_ Контролдокк пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) .</span><span class="sxs-lookup"><span data-stu-id="09a93-107">The property value is from the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) enumeration.</span></span>



|    <span data-ttu-id="09a93-108">Перечисление</span><span class="sxs-lookup"><span data-stu-id="09a93-108">Enumeration</span></span>                     |    <span data-ttu-id="09a93-109">Описание</span><span class="sxs-lookup"><span data-stu-id="09a93-109">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a93-110">контролдокк пользовательского интерфейса ( \_ \_ вверху)</span><span class="sxs-lookup"><span data-stu-id="09a93-110">UI\_CONTROLDOCK\_TOP</span></span>    | <span data-ttu-id="09a93-111">QAT закрепляется в неклиентской области хост-приложения ленты, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="09a93-111">The QAT is docked in the nonclient area of the Ribbon host application, as shown in the following screen shot.</span></span>![снимок экрана панели быстрого доступа, закрепленной над лентой в неклиентской области.](images/properties/qat-docktop.png)<br/> |
| <span data-ttu-id="09a93-113">\_КОНТРОЛДОКК ИП \_ снизу</span><span class="sxs-lookup"><span data-stu-id="09a93-113">UI\_CONTROLDOCK\_BOTTOM</span></span> | <span data-ttu-id="09a93-114">QAT закрепляется как визуальная панель под лентой, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="09a93-114">The QAT is docked as a visually integral band below the Ribbon, as shown in the following screen shot.</span></span> ![снимок экрана панели быстрого доступа, закрепленной под лентой.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="09a93-116">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="09a93-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09a93-117">Свойства ленты</span><span class="sxs-lookup"><span data-stu-id="09a93-117">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

