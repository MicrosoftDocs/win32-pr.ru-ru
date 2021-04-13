---
title: Иажентбаллун Жетфонтстрикесру
description: Иажентбаллун Жетфонтстрикесру
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411358"
---
# <a name="iagentballoongetfontstrikethru"></a>Иажентбаллун:: Жетфонтстрикесру

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




