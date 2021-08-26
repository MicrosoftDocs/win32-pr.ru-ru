---
description: Метод Плайчаптер запускает воспроизведение из указанной главы в текущем заголовке.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Метод Плайчаптер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832b1da6940b26a3cc3a4ab5bdba8653806966f8a399b74eb5adf50600e22293
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102344"
---
# <a name="playchapter-method"></a>Метод Плайчаптер

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`PlayChapter`Метод запускает воспроизведение из указанной главы в текущем заголовке.

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ичаптер*
</dt> <dd>

Указывает индекс главы в текущем заголовке как целое число.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

По достижении конца указанной главы этот метод продолжит играть в последующие главы, если таковые имеются. Если вы хотите воспроизвести только указанную главу, используйте [**плайчаптерсаутостоп**](playchaptersautostop-method.md).

## <a name="see-also"></a>См. также

<dl> <dt>

[**плайчаптеринтитле**](playchapterintitle-method.md)
</dt> </dl>

 

 



