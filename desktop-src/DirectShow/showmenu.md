---
description: Событие Шовмену отправляется, когда диск включает или отключает отображение меню.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: шовмену
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990148"
---
# <a name="showmenu"></a>шовмену

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

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

 

 



