---
title: Иажентчарактер Жетидлеон
description: Иажентчарактер Жетидлеон
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a5ce64b39b615325a3de55c1643004cffaeecf89e2e0a024d317bb56e32d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478377"
---
# <a name="iagentcharactergetidleon"></a>Иажентчарактер:: Жетидлеон

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентчарактер:: Сетидлеон**](iagentcharacter--setidleon.md)


 

 




