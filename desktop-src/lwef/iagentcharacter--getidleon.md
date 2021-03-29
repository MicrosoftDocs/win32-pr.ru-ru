---
title: Иажентчарактер Жетидлеон
description: Иажентчарактер Жетидлеон
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780129"
---
# <a name="iagentcharactergetidleon"></a>Иажентчарактер:: Жетидлеон

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

Указывает состояние обработки автоматического простоя для символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*пбон*
</dt> <dd>

Адрес переменной, которая получает **значение true** , если сервер Microsoft Agent автоматически воспроизводит анимацию состояния **состояние простоя** для символа и **значение false** в противном случае.

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: Сетидлеон**](iagentcharacter--setidleon.md)


 

 




