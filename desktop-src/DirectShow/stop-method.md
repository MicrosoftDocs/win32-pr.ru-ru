---
description: Метод Stop останавливает воспроизведение.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Метод «завершение» (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999156"
---
# <a name="stop-method-directshow"></a>Метод «завершение» (DirectShow)

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`Stop`Метод останавливает воспроизведение.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Если для [**енаблересетонстоп**](enableresetonstop-property.md) задано значение true, вызов `Stop` помещает Навигатор DVD вместе с остальной частью графа фильтра в остановленное состояние, что означает, что при следующем нажатии кнопки **воспроизведения** воспроизведение начинается в начале диска. Если для **енаблересетонстоп** задано значение true, воспроизведение возобновляется, когда пользователь выдает следующую команду **Play** .

 

 



