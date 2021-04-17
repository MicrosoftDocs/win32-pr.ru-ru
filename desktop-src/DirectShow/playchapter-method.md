---
description: Метод Плайчаптер запускает воспроизведение из указанной главы в текущем заголовке.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Метод Плайчаптер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682177"
---
# <a name="playchapter-method"></a>Метод Плайчаптер

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

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

## <a name="remarks"></a>Комментарии

По достижении конца указанной главы этот метод продолжит играть в последующие главы, если таковые имеются. Если вы хотите воспроизвести только указанную главу, используйте [**плайчаптерсаутостоп**](playchaptersautostop-method.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**плайчаптеринтитле**](playchapterintitle-method.md)
</dt> </dl>

 

 



