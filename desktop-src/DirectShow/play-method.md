---
description: Метод Play воспроизводит текущее название DVD-диска.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Метод Play (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537124"
---
# <a name="play-method-directshow"></a>Метод Play (DirectShow)

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`Play`Метод воспроизводит текущее название DVD-диска.

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Если воспроизведение приостановлено или остановлено, а [**енаблересетонстоп**](enableresetonstop-property.md) имеет значение true, вызов **Play** продолжит воспроизведение с обычной скоростью в текущем расположении. Если воспроизведение остановлено и **енаблересетонстоп** имеет значение false, вызов **Play** приведет к тому, что диск начнет играть в начале первого заголовка.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Возобновить**](resume-method.md)
</dt> </dl>

 

 



