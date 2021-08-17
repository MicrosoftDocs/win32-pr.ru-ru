---
title: Параметр/d
description: Параметр/D определяет имя и необязательное значение, передаваемое препроцессору C, как при помощи директивы \ define. В командной строке можно использовать несколько директив/D.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- Параметр/d Switch
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa8bc01a978949ec0f0cc4ff78289a1cb442046966f1cea954c6b65cc232f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385781"
---
# <a name="d-switch"></a>Параметр/d

Параметр **/d** определяет имя и необязательное значение, передаваемое препроцессору C, как при помощи директивы **\# define** . В командной строке можно использовать несколько директив **/d** .

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*name* 
</dt> <dd>

Указывает определенное имя, которое передается препроцессору C при наличии ключа [**/КПП \_ cmd**](-cpp-cmd.md) и [**/КПП \_ OPT**](-cpp-opt.md) .

</dd> <dt>

*definition* 
</dt> <dd>

Указывает значение, связанное с определенным именем.

</dd> </dl>

## <a name="remarks"></a>Remarks

Пробел между параметром **/d** и определенным именем является необязательным.

Если параметр [**\_ cmd/КПП**](-cpp-cmd.md) имеет значение, а параметр [**/КПП \_ OPT**](-cpp-opt.md) — нет, компилятор MIDL объединяет строку, указанную параметром **/КПП \_ cmd** , с параметрами [**/i**](-i.md), **/d** и [**/u**](-u.md) и использует эту объединенную строку для вызова препроцессора C для каждого исходного файла IDL и ACF.

Параметр компилятора MIDL **/d** игнорируется, если указан параметр компилятора MIDL [/но \_ cpp](-no-cpp-nocpp.md) или [**/КПП \_ OPT**](-cpp-opt.md) .

## <a name="examples"></a>Примеры

**MIDL-ДУНИКОДЕ filename. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**/КПП \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/КПП \_ OPT**](-cpp-opt.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/но \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[**/U**](-u.md)
</dt> </dl>

 

 




