---
title: Справочник по MIDL Command-Line
description: В этом разделе содержатся справочные сведения по каждому параметру командной строки и переключателю, распознаваемым компилятором Microsoft RPC MIDL.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Язык MIDL MIDL, Справочник
- Справочник по командной строке MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1569e29daf8a2976379576a5f1671f5117e7990c
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105662001"
---
# <a name="midl-command-line-reference"></a>Справочник по MIDL Command-Line

В этом разделе содержатся справочные сведения по каждому параметру командной строки и переключателю, распознаваемым компилятором Microsoft RPC MIDL. Записи переключателей упорядочены в алфавитном порядке. [Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md) описывает общий синтаксис командной строки.

<dl>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)  
[Команда файла ответа](the-response-file-command.md)  
[**/акф**](-acf.md)  
[**/align**](-align.md)  
[**/amd64**](-amd64.md)  
[**\_Конфигурация/АПП**](-app-config.md)  
[совместимость с/бакквард \_](-backward-compat.md)  
[**/c \_ ext**](-c-ext.md)  
[**/каукс**](-caux.md)  
[**/Char**](-char.md)  
[**/Client**](-client.md)  
[**/конфирм**](-confirm.md)  
[**/КПП \_ cmd**](-cpp-cmd.md)  
[**/КПП \_ OPT**](-cpp-opt.md)  
[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)  
[**/D**](-d.md)  
[**/dlldata**](-dlldata.md)  
[**/env**](-env.md)  
[**/Error**](-error.md)  
[**/Error**](-error.md)  
[**/h**](-h.md)  
[**/Header**](-header.md)  
[**/Help (/?)**](-help-.md)  
[**/ia64**](-ia64.md)  
[**/I**](-i.md)  
[**/IID**](-iid.md)  
[**/Import**](-import.md)  
[**/LCID**](-lcid.md)  
[**/mktyplib203**](-mktyplib203.md)  
[**/МС \_ ext**](-ms-ext.md)  
[**\_объединение/МС**](-ms-union.md)  
[**/МСК \_ ver**](-msc-ver.md)  
[**/New**](-new.md)  
[**/newtlb**](-newtlb.md)  
[**/но \_ cpp,/нокпп**](-no-cpp-nocpp.md)  
[**/но \_ по умолчанию \_ ЕПВ**](-no-default-epv.md)  
[**\_идир/но DEF \_**](-no-def-idir.md)  
[**/но в \_ формате \_ OPT**](-no-format-opt.md)  
[**/но \_ надежность**](-no-robust.md)  
[**\_предупреждение/но**](-no-warn.md)  
[**/nologo**](-nologo.md)  
[**/notlb**](-notlb.md)  
[**/o**](-o.md)  
[**/Oi**](-oi.md)  
[**/Old**](-old.md)  
[**/oldtlb**](-oldtlb.md)  
[**/oldnames**](-oldnames.md)  
[**/OS**](-os.md)  
[**/осф**](-osf.md)  
[**/out**](-out.md)  
[**/Pack**](-pack.md)  
[**/префикс**](-prefix.md)  
[**/протокол**](-protocol.md)  
[**/Proxy**](-proxy.md)  
[**/robust**](-robust.md)  
[**/рпксс**](-rpcss.md)  
[**/сал**](-sal.md)  
[**/Сал \_ локальный**](-sal-local.md)  
[**/саукс**](-saux.md)  
[**/савепп**](-savepp.md)  
[**/sstub**](-sstub.md)  
[**\_Проверка/синтакс**](-syntax-check.md)  
[**/<system>**](-system-.md)  
[**/Target**](-target.md)  
[**/TLB**](-tlb.md)  
[**/U**](-u.md)  
[**/TestCleanup используется \_ ЕПВ**](-use-epv.md)  
[**\_Метка/Version**](-version-stamp.md)  
[**/W**](-w.md)  
[**/warn**](-warn.md)  
[**/win32**](-win32.md)  
[**/win64**](-win64.md)  
[**/WX**](-wx.md)  
[**/ZP**](-zp.md)  
[**/ZS**](-zs.md)  
</dl>

Компилятор MIDL может создавать код для различных платформ и системных выпусков. Дополнительные сведения о предлагаемых параметрах и способах создания кода, оптимизированного для конкретного выпуска, см. в параметре [**/Target**](-target.md) .

Обратите внимание, что знак минус (–) может быть заменен на косую черту (/) во всех параметрах командной строки MIDL, начинающихся с косой черты (/). В следующем примере демонстрируется их эквивалентность при вызове компилятора MIDL.

## <a name="examples"></a>Примеры

**MIDL/АКФ My \_ ACF. ACF** *имя_файла * * *. idl**

**MIDL-ACF My \_ ACF. ACF** *имя_файла * * *. idl**

 

 




