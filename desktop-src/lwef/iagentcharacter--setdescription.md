---
title: Иажентчарактер SetDescription
description: Иажентчарактер SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d96765d3faddafef00a28826ec5a9fdd92acb6884ac3aa659ad88ba2c091a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609824"
---
# <a name="iagentcharactersetdescription"></a>Иажентчарактер:: SetDescription

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

Задает описание символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*бсздескриптион*
</dt> <dd>

Значение типа BSTR, которое задает описание символа. Описание символа по умолчанию определяется при его компиляции с помощью редактора символов Microsoft Agent. Параметр description является необязательным и не может быть указан для всех символов. Описание символа можно изменить с помощью **иажентчарактер:: setDescription**; Однако это значение не является постоянным (постоянно хранится). Описание символа возвращается к значению по умолчанию при первой загрузке символа клиентом.

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иажентчарактер::, описание**](iagentcharacter--getdescription.md)


 

 




