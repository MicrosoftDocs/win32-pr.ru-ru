---
title: Иажентчарактер SetDescription
description: Иажентчарактер SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411447"
---
# <a name="iagentcharactersetdescription"></a>Иажентчарактер:: SetDescription

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




