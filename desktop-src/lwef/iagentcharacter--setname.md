---
title: Иажентчарактер SetName
description: Иажентчарактер SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710173"
---
# <a name="iagentcharactersetname"></a>Иажентчарактер:: SetName

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

Задает имя символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*бсзнаме*
</dt> <dd>

Значение типа BSTR, задающее имя символа. Имя символа по умолчанию определяется при компиляции с помощью редактора символов Microsoft Agent. Его можно изменить с помощью **иажентчарактер:: SetName**; Однако это изменяет имя символа для всех текущих клиентов символа. Это свойство не является постоянным (хранится без возможности восстановления). Имя символа возвращается к имени по умолчанию при первой загрузке символа клиентом.

Имя символа может также зависеть от идентификатора языка. Символы могут быть скомпилированы с разными именами для разных языков.

Сервер использует параметр имени символа в частях интерфейса Microsoft Agent, например, заголовок окна «Voice Commands», если символ является входным и находится во всплывающем меню Microsoft Agent панели задач.

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: Name**](iagentcharacter--getname.md)


 

 




