---
description: Метод ЖетдвдтекстлангуажелЦид извлекает код локали (LCID) для указанного блока текстовой строки.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Метод ЖетдвдтекстлангуажелЦид
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536626"
---
# <a name="getdvdtextlanguagelcid-method"></a>Метод ЖетдвдтекстлангуажелЦид

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetDVDTextLanguageLCID`Метод получает код локали (LCID) для указанного блока текстовой строки.

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*илангиндекс*
</dt> <dd>

Задает языковой блок текста на диске в виде целого числа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение LCID, содержащее сведения, указывающие язык, на котором написаны строки.

## <a name="remarks"></a>Комментарии

Дополнительные текстовые строки хранятся в смежных блоках на диске. Каждый язык имеет один блок строк. Приложение задает эти блоки по индексу, который должен быть меньше значения, возвращаемого функцией [**жетдвдтекстнумберофлангуажес**](getdvdtextnumberoflanguages-method.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объект Мсвебдвд](mswebdvd-object.md)
</dt> <dt>

[**жетлангфромлангид**](getlangfromlangid-method.md)
</dt> </dl>

 

 



