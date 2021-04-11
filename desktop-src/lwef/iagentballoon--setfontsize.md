---
title: Иажентбаллун Сетфонтсизе
description: Иажентбаллун Сетфонтсизе
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332248"
---
# <a name="iagentballoonsetfontsize"></a>Иажентбаллун:: Сетфонтсизе

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

Задает размер шрифта, отображаемого в подсказке к слову.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*лфонтсизе*
</dt> <dd>

Размер шрифта.

</dd> </dl>

Размер шрифта по умолчанию, используемый в подсказке для символа, определяется в редакторе символов Microsoft Agent. Его можно изменить с помощью **иажентбаллун:: сетфонтсизе**. Однако пользователь может переопределить параметр размера шрифта для всех символов с помощью страницы свойств Microsoft Agent.

## <a name="see-also"></a>См. также:

[**Иажентбаллун:: FontSize**](iagentballoon--getfontsize.md)


 

 




