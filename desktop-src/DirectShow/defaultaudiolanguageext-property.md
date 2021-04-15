---
description: Свойство Дефаултаудиолангуажеекст извлекает расширение языка DVD-звука по умолчанию.
ms.assetid: 628af2aa-e528-4689-953b-558e13e1d513
title: Дефаултаудиолангуажеекст, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5ce89099cd8e31cde9beb8bb3c8a9f1e16b3b0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536875"
---
# <a name="defaultaudiolanguageext-property"></a>Дефаултаудиолангуажеекст, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`DefaultAudioLanguageExt`Свойство получает расширение языка DVD-звука по умолчанию.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultAudioLanguageExt
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, указывающее расширение языка звука по умолчанию. Возможные значения см. в разделе Примечания.

## <a name="remarks"></a>Комментарии

Это свойство доступно только для чтения и не имеет значения по умолчанию. В следующей таблице приведены возможные значения для расширений языка DVD Audio.



| Значение | Описание       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Субтитры          |
| 2     | висуаллимпаиред  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

 

 



