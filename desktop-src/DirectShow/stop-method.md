---
description: Метод Stop останавливает воспроизведение.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Метод завершения (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9eb216c3ad5c98dd1722ff941131198cfe662d025b20c3f71fe9ea758e0a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050114"
---
# <a name="stop-method-directshow"></a>Метод завершения (DirectShow)

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`Stop`Метод останавливает воспроизведение.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Если для [**енаблересетонстоп**](enableresetonstop-property.md) задано значение true, вызов `Stop` помещает Навигатор DVD вместе с остальной частью графа фильтра в остановленное состояние, что означает, что при следующем нажатии кнопки **воспроизведения** воспроизведение начинается в начале диска. Если для **енаблересетонстоп** задано значение true, воспроизведение возобновляется, когда пользователь выдает следующую команду **Play** .

 

 



