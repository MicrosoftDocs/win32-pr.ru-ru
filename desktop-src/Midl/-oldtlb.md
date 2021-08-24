---
title: /oldtlb, параметр
description: Параметр/oldtlb направляет компилятор MIDL для создания библиотеки типов старого формата.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- MIDL/oldtlb Switch
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b30a7bc905645523a81287eea2dfcdc408b8a4d172cc84282e0f1538e12cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895994"
---
# <a name="oldtlb-switch"></a>/oldtlb, параметр

Параметр **/oldtlb** направляет компилятор MIDL для создания библиотеки типов старого формата.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Remarks

параметр **/oldtlb** переопределяет значение по умолчанию и направляет компилятор MIDL создавать библиотеки типов старого формата даже в текущих версиях Windows с помощью [креатетипелиб](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) вместо [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).

## <a name="examples"></a>Примеры

**MIDL/oldtlb filename. idl**

**MIDL/oldtlb мйолдодл. odl**

## <a name="see-also"></a>См. также

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 