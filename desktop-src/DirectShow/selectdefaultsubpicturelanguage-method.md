---
description: Метод Селектдефаултсубпиктурелангуаже задает текущий язык подизображения по умолчанию в объекте Мсвебдвд.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Метод Селектдефаултсубпиктурелангуаже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805836"
---
# <a name="selectdefaultsubpicturelanguage-method"></a>Метод Селектдефаултсубпиктурелангуаже

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`SelectDefaultSubpictureLanguage`Метод задает текущий язык подизображения по умолчанию в объекте **мсвебдвд** .

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*иланг*
</dt> <dd>

Задает язык в виде целого числа.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*иекст*
</dt> <dd>

Задает расширение языка субтитров в виде целого числа.



| Значение | Описание                    |
|-------|--------------------------------|
| 0     | Расширение не указано        |
| 1     | Обычные субтитры                |
| 2     | Крупные субтитры                   |
| 3     | Субтитры детей            |
| 5     | Обычные закрытые субтитры         |
| 6     | Большие закрытые субтитры            |
| 7     | Закрытые субтитры детей     |
| 9     | Принудительно                         |
| 13    | Обычные комментарии режиссера     |
| 14    | Комментарии для крупного директора        |
| 15    | Комментарии Директор'с детей |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Расширение языка субтитров предоставляет дополнительные сведения о подизображении.

 

 



