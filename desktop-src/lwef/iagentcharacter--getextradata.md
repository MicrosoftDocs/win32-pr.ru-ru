---
title: Иажентчарактер Жетекстрадата
description: Иажентчарактер Жетекстрадата
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133054"
---
# <a name="iagentcharactergetextradata"></a>Иажентчарактер:: Жетекстрадата

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

Извлекает дополнительные данные, хранящиеся как часть символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*пбсзекстрадата*
</dt> <dd>

Адрес объекта BSTR, который получает значение дополнительных данных для символа. Дополнительные данные символов определяются при компиляции с помощью редактора символов Microsoft Agent. Разработчик символов может предоставить эту строку, отредактировав. Файл ACD для символа. Этот параметр является необязательным и может быть не указан для всех символов, а также не может быть определен или изменен во время выполнения. Кроме того, значение предоставленных данных определяется разработчиком символов.

</dd> </dl>

 

 




