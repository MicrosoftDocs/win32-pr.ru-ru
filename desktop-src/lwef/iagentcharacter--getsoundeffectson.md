---
title: Иажентчарактер Жетсаундеффектсон
description: Иажентчарактер Жетсаундеффектсон
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f7133e41e4c291200feaf8fdb8ab3919cdb622ca927c155fc0941202fd555a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848644"
---
# <a name="iagentcharactergetsoundeffectson"></a>Иажентчарактер:: Жетсаундеффектсон

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентчарактер:: сетсаундеффектсон**](iagentcharacter--setsoundeffectson.md), [ **иажентаудиуутпутпропертиес:: жетусингсаундеффектс**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




