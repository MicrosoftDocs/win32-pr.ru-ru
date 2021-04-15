---
description: Свойство Куррентаудиостреам задает или получает номер включенного звукового потока.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Куррентаудиостреам, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655587"
---
# <a name="currentaudiostream-property"></a>Куррентаудиостреам, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`CurrentAudioStream`Свойство задает или получает номер включенного звукового потока.

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение от 0 до 7, указывающее текущий аудиопоток.

## <a name="remarks"></a>Комментарии

Это свойство доступно для чтения и записи и не имеет значения по умолчанию. Прежде чем пытаться задать новый аудиопоток, вызовите [**исаудиостреаменаблед**](isaudiostreamenabled-method.md) , чтобы убедиться, что поток доступен.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**аудиостреамсаваилабле**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



