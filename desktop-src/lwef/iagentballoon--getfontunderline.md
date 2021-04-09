---
title: Иажентбаллун Жетфонтундерлине
description: Иажентбаллун Жетфонтундерлине
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068561"
---
# <a name="iagentballoongetfontunderline"></a>Иажентбаллун:: Жетфонтундерлине

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

Указывает, установлен ли стиль подчеркивания для шрифта, используемого в тексте всплывающей подсказки.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*пбфонтундерлине*
</dt> <dd>

Адрес значения, которое принимает значение **true** , если задан стиль подчеркивания шрифта, и **значение false** в противном случае.

</dd> </dl>

Стиль шрифта, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent. Оно не может быть изменено приложением. Однако пользователь может переопределить параметры шрифта для всех символов с помощью страницы свойств Microsoft Agent.

 

 




