---
description: Метод Селектдефаултаудиолангуаже задает текущий звуковой язык по умолчанию в объекте Мсвебдвд.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Метод Селектдефаултаудиолангуаже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537109"
---
# <a name="selectdefaultaudiolanguage-method"></a>Метод Селектдефаултаудиолангуаже

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`SelectDefaultAudioLanguage`Метод задает текущий звуковой язык по умолчанию в объекте мсвебдвд.

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*иланг*
</dt> <dd>

Задает язык в виде целочисленного значения LCID.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*иекст*
</dt> <dd>

Указывает расширение языка DVD-звука в виде целого значения.



| Значение | Описание       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Субтитры          |
| 2     | висуаллимпаиред  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объект Мсвебдвд](mswebdvd-object.md)
</dt> </dl>

 

 



