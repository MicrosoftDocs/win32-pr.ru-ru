---
title: Иажентчарактер имя
description: Иажентчарактер имя
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332763"
---
# <a name="iagentcharactergetname"></a>Иажентчарактер:: Name

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

Возвращает имя символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*пбсзнаме*
</dt> <dd>

Адрес объекта BSTR, который получает значение имени для символа.

</dd> </dl>

Имя символа по умолчанию определяется при компиляции с помощью редактора символов Microsoft Agent. Имя символа может отличаться в зависимости от идентификатора языка символа. Символы могут быть скомпилированы с разными именами для разных языков.

Можно также задать имя символа с помощью **иажентчарактер: SetName**; Однако имена всех текущих клиентов символа изменяются.

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: SetName**](iagentcharacter--setname.md)


 

 




