---
title: Иажентбаллун Сетфонтнаме
description: Иажентбаллун Сетфонтнаме
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068559"
---
# <a name="iagentballoonsetfontname"></a>Иажентбаллун:: Сетфонтнаме

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

Задает шрифт, отображаемый в подсказке к слову.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*бсзфонтнаме*
</dt> <dd>

Значение типа BSTR, которое задает шрифт, отображаемый в подсказке к слову.

</dd> </dl>

Шрифт по умолчанию, используемый в подсказке для символа, определен в редакторе символов Microsoft Agent. Его можно изменить с помощью **иажентбаллун:: сетфонтнаме**. Однако пользователь может переопределить параметр шрифта для всех символов с помощью страницы свойств Microsoft Agent.

## <a name="see-also"></a>См. также:

[**Иажентбаллун:: Visible**](iagentballoon--getvisible.md)


 

 




