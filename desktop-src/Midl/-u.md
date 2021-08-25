---
title: Параметр/u
description: Параметр/U удаляет все предыдущие определения имени, передавая имя в препроцессору C, как при помощи директивы \ undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U переключить MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9eab33e5aff861c1afecaafa52e04964ef286c5835e0a6992a3d369210f8927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895774"
---
# <a name="u-switch"></a>Параметр/u

Параметр **/u** удаляет все предыдущие определения имени, передавая имя в препроцессору C, как при помощи директивы **\# undefine** .

``` syntax
midl /U name
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*name* 
</dt> <dd>

Задает определенное имя, передаваемое препроцессору C, как если бы она была директивой **\# undefine** . Имя предопределено препроцессором C или ранее определенным пользователем.

</dd> </dl>

## <a name="remarks"></a>Remarks

В командной строке можно использовать несколько директив **/u** . Пробел между параметром **/u** и неопределенное имя является необязательным.

Если параметр [**\_ cmd/КПП**](-cpp-cmd.md) имеет значение, а параметр [**/КПП \_ OPT**](-cpp-opt.md) — нет, компилятор MIDL объединяет строку, указанную параметром/КПП \_ cmd, с параметрами [**/i**](-i.md), [**/d**](-d.md)и **/U** и использует эту объединенную строку для вызова препроцессора C для каждого исходного файла IDL и ACF. Параметр компилятора MIDL **/u** игнорируется, если указан параметр компилятора MIDL **/но \_ cpp** или **/КПП \_ OPT** .

## <a name="examples"></a>Примеры

**MIDL/УУНИКОДЕ filename. idl**

## <a name="see-also"></a>См. также

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/КПП \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/КПП \_ OPT**](-cpp-opt.md)
</dt> <dt>

[**/D**](-d.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[**/но \_ cpp**](-no-cpp-nocpp.md)
</dt> </dl>

 

 




