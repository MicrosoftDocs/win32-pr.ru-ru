---
description: Метод Step перемещает DVD-Video поток на указанное число кадров.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Метод Step
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674168"
---
# <a name="step-method"></a>Метод Step

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`Step`Метод перемещает DVD-Video поток на указанное число кадров.

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*IFRAME*
</dt> <dd>

Указывает количество кадров для шага в виде целого числа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Перед вызовом этого метода вызовите [**канстеп**](canstep-method.md) , чтобы определить, поддерживает ли декодер пошаговое выполнение.

Если DVD-Video воспроизводится в обратном режиме при вызове этого метода, а декодер поддерживает обратный шаг за кадром, то пошаговое выполнение пакета выполняется в обратную.

 

 



