---
title: Иажентчарактер Жетсаундеффектсон
description: Иажентчарактер Жетсаундеффектсон
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a40f18a4fb8e7778c116c54391a7dc50e5267af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691389"
---
# <a name="iagentcharactergetsoundeffectson"></a>Иажентчарактер:: Жетсаундеффектсон

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

Получает значение, указывающее, включен ли параметр звуковых эффектов для символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*пбон*
</dt> <dd>

Адрес переменной, принимающей **значение true** , если включен параметр звуковых эффектов для символа, **значение false** , если значение отключено.

</dd> </dl>

Параметр звуковых эффектов для символа определяет, будут ли воспроизводиться звуковые эффекты, скомпилированные как часть символа, при воспроизведении связанной анимации. Параметр подчиняется параметру глобальные звуковые эффекты пользователя в [**иажентаудиуутпутпропертиес:: жетусингсаундеффектс**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: сетсаундеффектсон**](iagentcharacter--setsoundeffectson.md), [ **иажентаудиуутпутпропертиес:: жетусингсаундеффектс**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




