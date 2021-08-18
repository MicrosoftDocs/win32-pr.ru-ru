---
title: " ifdef"
description: Директива \ ifdef управляет условной компиляцией файла ресурсов путем проверки указанного имени.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e834dc84d54e1d6f7725008b8bcf28f4ed49fc3fe45f36fb291ddc397d30eb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034482"
---
# <a name="ifdef"></a>\#ifdef

Директива **\# ifdef** управляет условной компиляцией файла ресурсов путем проверки указанного имени. Если имя было определено с помощью директивы **\# define** или с помощью параметра командной строки **/d** в компиляторе ресурсов, параметр **\# ifdef** направляет компилятору инструкцию сразу после директивы **\# ifdef** . Если имя не определено, то параметр **\# ifdef** направляет компилятору пропуск всех инструкций вплоть до следующей директивы **\# endif** .

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*безымян*
</dt> <dd>

Имя, проверяемое директивой.

</dd> </dl>

## <a name="example"></a>Пример

Этот пример компилирует оператор [**Bitmap**](bitmap-resource.md) , только если определен параметр debug:

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Директивы препроцессора](preprocessor-directives.md)
</dt> </dl>

 

 




