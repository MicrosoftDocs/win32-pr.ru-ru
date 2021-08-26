---
title: /системный коммутатор
description: Параметр/System указывает компилятору MIDL создать библиотеку типов для указанной системы. По умолчанию используется текущая операционная система.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /системный коммутатор MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01b6455807aedb99d7bd525c69fffc524dbe25d4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882791"
---
# <a name="ltsystemgt-switch"></a>/&lt;системный &gt; коммутатор

**/ &lt; Системный &gt;** параметр направляет компилятор MIDL для создания библиотеки типов для указанной системы. По умолчанию используется текущая операционная система.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Windows 2000, Windows XP, Windows Vista, Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * *


</dt> <dd>

64-разрядная Windowsная среда на базе Intel, например Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista или Windows 7.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>AMD64 * * * *


</dt> <dd>

Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista или Windows 7, на основе 64-разрядной Windows в сша.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

**/ &lt; Системный &gt;** коммутатор функционально аналогичен параметру MIDL [**/env**](-env.md) и распознается компилятором MIDL исключительно для обеспечения обратной совместимости с MkTypLib. При создании нового файла makefile используйте параметр **/env** .

## <a name="examples"></a>Примеры

**MIDL/Win32 filename. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> </dl>

 

 




