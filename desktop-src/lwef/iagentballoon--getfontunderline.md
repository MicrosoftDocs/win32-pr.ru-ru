---
title: Иажентбаллун Жетфонтундерлине
description: Иажентбаллун Жетфонтундерлине
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325f383aa76c55068ca7244b4ce0f822602651fa196ee336060fcc21fe3ab068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962364"
---
# <a name="iagentballoongetfontunderline"></a>Иажентбаллун:: Жетфонтундерлине

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




