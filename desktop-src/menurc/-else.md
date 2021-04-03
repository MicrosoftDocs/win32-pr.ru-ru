---
title: " else"
description: Директива \ else помечает необязательное предложение блока условной компиляции, определенного директивой \ ifdef, \ ifndef или \ if. Директива \ else должна быть последней директивой перед директивой \ endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776448"
---
# <a name="else"></a>\#else

Директива **\# else** помечает необязательное предложение блока условной компиляции, определенного директивой **\# ifdef**, **\# ifndef** или **\# If** . Директива **\# else** должна быть последней директивой перед директивой **\# endif** .

``` syntax
#else
```

Эта директива не имеет параметров.

## <a name="example"></a>Пример

Этот пример компилирует второй оператор [**Bitmap**](bitmap-resource.md) , только если не ОПРЕДЕЛЕН параметр debug:

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Директивы препроцессора](preprocessor-directives.md)
</dt> </dl>

 

 




