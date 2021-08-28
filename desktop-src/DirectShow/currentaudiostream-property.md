---
description: Свойство Куррентаудиостреам задает или получает номер включенного звукового потока.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Куррентаудиостреам, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd814d5b560ed55ea312fbebb8678c67b1422b0cf3d47917fbf772f56a0d3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075974"
---
# <a name="currentaudiostream-property"></a>Куррентаудиостреам, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`CurrentAudioStream`Свойство задает или получает номер включенного звукового потока.

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение от 0 до 7, указывающее текущий аудиопоток.

## <a name="remarks"></a>Remarks

Это свойство доступно для чтения и записи и не имеет значения по умолчанию. Прежде чем пытаться задать новый аудиопоток, вызовите [**исаудиостреаменаблед**](isaudiostreamenabled-method.md) , чтобы убедиться, что поток доступен.

## <a name="see-also"></a>См. также

<dl> <dt>

[**аудиостреамсаваилабле**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



