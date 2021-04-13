---
title: Иажентчарактер, описание
description: Иажентчарактер, описание
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411455"
---
# <a name="iagentcharactergetdescription"></a>Иажентчарактер::, описание

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

Извлекает описание символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*пбсздескриптион*
</dt> <dd>

Адрес объекта BSTR, который получает значение описания символа. Описание символа определяется при его компиляции с помощью редактора символов Microsoft Agent. Параметр description является необязательным и не может быть указан для всех символов.

</dd> </dl>

 

 




