---
title: Иажентчарактер Сетсаундеффектсон
description: Иажентчарактер Сетсаундеффектсон
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a454a6ebeecc763cb7e5a964bb1f2897df6c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710115"
---
# <a name="iagentcharactersetsoundeffectson"></a>Иажентчарактер:: Сетсаундеффектсон

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

Определяет, воспроизводятся ли звуковые эффекты символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Системе*
</dt> <dd>

Настройка звуковых эффектов. Если этот параметр имеет **значение true**, звуковые эффекты анимации воспроизводятся при воспроизведении анимации. Если задано **значение false**, звуковые эффекты не воспроизводятся.

</dd> </dl>

Этот параметр определяет, будут ли воспроизводиться звуковые эффекты, скомпилированные как часть символа, при воспроизведении связанной анимации. Параметр этого свойства применяется ко всем клиентам символа. Этот параметр также подчиняется параметру глобальные звуковые эффекты пользователя в [**иажентаудиуутпутпропертиес:: жетусингсаундеффектс**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>См. также:

[**Иажентчарактер:: жетсаундеффектсон**](iagentcharacter--getsoundeffectson.md), [ **иажентаудиуутпутпропертиес:: жетусингсаундеффектс**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




