---
title: Иажентчарактер Сетсаундеффектсон
description: Иажентчарактер Сетсаундеффектсон
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71abb6adebf09182d4329202e77355e7dc365899291995e97eca66305a00ab94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725024"
---
# <a name="iagentcharactersetsoundeffectson"></a>Иажентчарактер:: Сетсаундеффектсон

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентчарактер:: жетсаундеффектсон**](iagentcharacter--getsoundeffectson.md), [ **иажентаудиуутпутпропертиес:: жетусингсаундеффектс**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




