---
title: Иажентбаллун Жетфонтболд
description: Иажентбаллун Жетфонтболд
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258587"
---
# <a name="iagentballoongetfontbold"></a>Иажентбаллун:: Жетфонтболд

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

Указывает, является ли шрифт, используемый в выноске слова, полужирным.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*пбфонтболд*
</dt> <dd>

Адрес значения, которое принимает значение **true** , если шрифт имеет полужирное начертание, и **значение false** , если он не является полужирным.

</dd> </dl>

Стиль шрифта, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent. Оно не может быть изменено приложением. Однако пользователь может переопределить параметры шрифта для всех символов на странице свойств Microsoft Agent.

 

 




