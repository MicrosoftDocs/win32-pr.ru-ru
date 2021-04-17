---
description: Метод Жетдвдтекстнумберофстрингс извлекает количество текстовых строк, доступных для указанного языка.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Метод Жетдвдтекстнумберофстрингс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673079"
---
# <a name="getdvdtextnumberofstrings-method"></a>Метод Жетдвдтекстнумберофстрингс

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetDVDTextNumberOfStrings`Метод получает количество текстовых строк, доступных для указанного языка.

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*илангиндекс*
</dt> <dd>

Задает язык в виде целого числа. Значение должно находиться в диапазоне от нуля до значения, возвращенного [**жетдвдтекстнумберофлангуажес**](getdvdtextnumberoflanguages-method.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, указывающее, сколько строк содержит диск на указанном языке.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объект Мсвебдвд](mswebdvd-object.md)
</dt> </dl>

 

 



