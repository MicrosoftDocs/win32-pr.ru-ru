---
title: Иажентбаллун Сетфонтсизе
description: Иажентбаллун Сетфонтсизе
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6e19d79429ddf98f67a281cd11aefb1dc6bc2e54b1289e36c7cfb5a62bd538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976474"
---
# <a name="iagentballoonsetfontsize"></a>Иажентбаллун:: Сетфонтсизе

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




