---
description: Событие Шовмену отправляется, когда диск включает или отключает отображение меню.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: шовмену
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56eb6767a8144bab3de832570db63bc4e2cdc012490f776f52b6c8977cce9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050454"
---
# <a name="showmenu"></a>шовмену

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`ShowMenu`Событие отправляется, когда диск включает или отключает отображение меню.

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*двдменуидконстантс*
</dt> <dd>

Указывает, какое меню было включено или отключено в качестве числового значения.



| Значение | Описание |
|-------|-------------|
| 2     | Название       |
| 3     | Root        |
| 4     | Субтитров  |
| 5     | звук;       |
| 6     | Angle       |
| 7     | Глава     |



 

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*бенаблед*
</dt> <dd>

Указывает, включена или отключена операция в качестве логического значения.

</dd> </dl>

 

 



