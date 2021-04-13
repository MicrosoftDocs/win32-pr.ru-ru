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
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412847"
---
# <a name="oldtlb-switch"></a>/oldtlb, параметр

Параметр **/oldtlb** направляет компилятор MIDL для создания библиотеки типов старого формата.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Комментарии

Параметр **/oldtlb** переопределяет значение по умолчанию и направляет компилятор MIDL для создания библиотек типов старого формата даже в текущих версиях Windows с помощью [креатетипелиб](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) вместо [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).

## <a name="examples"></a>Примеры

**MIDL/oldtlb filename. idl**

**MIDL/oldtlb мйолдодл. odl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 