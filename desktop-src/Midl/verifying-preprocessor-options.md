---
title: Проверка параметров препроцессора
description: Компилятор MIDL неявно вызывает препроцессор и не отображает его параметры препроцессора.
ms.assetid: 2f402af4-18d7-480c-a8d2-d16f402ef87a
keywords:
- MIDL компилятора MIDL, проверка параметров препроцессора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a047980c9f2f9dc8deffdcf85de767e4dc8705
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888559"
---
# <a name="verifying-preprocessor-options"></a>Проверка параметров препроцессора

Компилятор MIDL неявно вызывает препроцессор и не отображает его параметры препроцессора. В отсутствие параметра/КПП, соответствующего параметру MIDL, Командная строка препроцессора состоит из всех ключей [**/i**](-i.md), [**/d**](-d.md) и [**/u**](-u.md) , используемых в командной строке MIDL, а также переключателей **/e** и [**/nologo**](-nologo.md) . [**\_**](-cpp-opt.md) Чтобы просмотреть параметры, передаваемые в препроцессор, используйте параметр компилятора [**/конфирм**](-confirm.md) .

Например, следующая строка

**midl.exe-D \_ Win32 \_ WinNT = 0x501-НАДЕЖЕН-днтенв = 1-ID: \\ NT \\ Public \\ SDK \\ Inc-Confirm-оикф-env Win32-out x86 заглушка. idl**

создает следующие выходные данные:

``` syntax
32 bit arguments
          input file -  stub.idl
          app_config -  No
               c_ext -  Yes
              client -  stub
                char -  signed
             confirm -  Yes
             cpp_cmd -  cl.exe
             cpp_opt -  -Id:\nt\public\sdk\inc -D_WIN32_WINNT=0x501 -DNTENV=1  -
E -nologo
             msc_ver -  1100
               cstub -  i386\stub_c.c
                   D -  -D_WIN32_WINNT=0x501 -DNTENV=1
                 env -  win32
            append64 -  No
               rpcss -  No
             use_epv -  No
      no_default_epv -  No
               error -  allocation ref bounds_check enum stub_data
              header -  i386\stub.h
                   I -  -Id:\nt\public\sdk\inc
              nologo -  No
              ms_ext -  Yes
            ms_union -  No
       no_format_opt -  No
            oldnames -  No
                 out -  i386\
              server -  stub
               sstub -  i386\stub_s.c
                   O -  interpreted stubs
                   W -  1
                  Zp -  8
```

 

 




