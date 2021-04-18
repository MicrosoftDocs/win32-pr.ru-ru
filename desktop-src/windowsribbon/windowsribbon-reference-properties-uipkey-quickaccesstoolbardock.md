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
# <a name="ui_pkey_quickaccesstoolbardock"></a>UI \_ PKEY \_ куиккакцесстулбардокк

Определяет свойство UI \_ PKEY \_ куиккакцесстулбардокк.

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ куиккакцесстулбардокк используется приложением для запроса состояния закрепления панели быстрого доступа (QAT).

Значение свойства находится в перечислении [**\_ Контролдокк пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) .



|                         |                                                                                                                                                                                                                                                       |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| контролдокк пользовательского интерфейса ( \_ \_ вверху)    | QAT закрепляется в неклиентской области хост-приложения ленты, как показано на следующем снимке экрана.![снимок экрана панели быстрого доступа, закрепленной над лентой в неклиентской области.](images/properties/qat-docktop.png)<br/> |
| \_КОНТРОЛДОКК ИП \_ снизу | QAT закрепляется как визуальная панель под лентой, как показано на следующем снимке экрана. ![снимок экрана панели быстрого доступа, закрепленной под лентой.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства ленты](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

