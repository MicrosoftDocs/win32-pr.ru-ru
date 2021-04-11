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
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133158"
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

## <a name="remarks"></a>Комментарии

В командной строке можно использовать несколько директив **/u** . Пробел между параметром **/u** и неопределенное имя является необязательным.

Если параметр [**\_ cmd/КПП**](-cpp-cmd.md) имеет значение, а параметр [**/КПП \_ OPT**](-cpp-opt.md) — нет, компилятор MIDL объединяет строку, указанную параметром/КПП \_ cmd, с параметрами [**/i**](-i.md), [**/d**](-d.md)и **/U** и использует эту объединенную строку для вызова препроцессора C для каждого исходного файла IDL и ACF. Параметр компилятора MIDL **/u** игнорируется, если указан параметр компилятора MIDL **/но \_ cpp** или **/КПП \_ OPT** .

## <a name="examples"></a>Примеры

**MIDL/УУНИКОДЕ filename. idl**

## <a name="see-also"></a>См. также раздел

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

 

 




