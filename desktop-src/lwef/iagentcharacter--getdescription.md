---
title: Иажентчарактер, описание
description: Иажентчарактер, описание
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23216f1a7b013a54de1e64351c2a9d3a3d3359d90e0516cd6852a003baa047c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716194"
---
# <a name="iagentcharactergetdescription"></a>Иажентчарактер::, описание

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




