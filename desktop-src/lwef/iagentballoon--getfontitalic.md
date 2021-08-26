---
title: Иажентбаллун Жетфонтиталик
description: Иажентбаллун Жетфонтиталик
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5535896cc3c40ae3cb04c3078621cc91df4869649cbe72cb106c3d99ec0299ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062024"
---
# <a name="iagentballoongetfontitalic"></a>Иажентбаллун:: Жетфонтиталик

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

Указывает, является ли шрифт, используемый в выноске слова, курсивом.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*пбфонтиталик*
</dt> <dd>

Адрес значения, которое принимает значение **true** , если шрифт является курсивом, и **значение false** , если он не является курсивом.

</dd> </dl>

Стиль шрифта, используемый в подсказке к слову, определяется в редакторе символов Microsoft Agent. Оно не может быть изменено приложением. Однако пользователь может переопределить параметры шрифта для всех символов на странице свойств Microsoft Agent.

 

 




