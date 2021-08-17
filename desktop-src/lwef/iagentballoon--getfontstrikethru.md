---
title: Иажентбаллун Жетфонтстрикесру
description: Иажентбаллун Жетфонтстрикесру
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b15bfbc120f7c8d614839f55ec985a3bdbdb3f840e5a07d615f7de0dfc75e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751028"
---
# <a name="iagentballoongetfontstrikethru"></a>Иажентбаллун:: Жетфонтстрикесру

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

Указывает, задан ли стиль перечеркивания для шрифта, используемого в тексте всплывающей подсказки.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*пбфонтстрикесру*
</dt> <dd>

Адрес значения, которое принимает значение **true** , если задан стиль перечеркивания шрифта, и **значение false** в противном случае.

</dd> </dl>

Стиль шрифта, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent. Оно не может быть изменено приложением. Однако пользователь может переопределить параметры шрифта для всех символов с помощью страницы свойств Microsoft Agent.

 

 




