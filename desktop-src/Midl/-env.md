---
title: /env, параметр
description: Параметр/env выбирает среду, в которой выполняется приложение.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- MIDL/env Switch
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412830"
---
# <a name="env-switch"></a>/env, параметр

Параметр **/env** выбирает среду, в которой выполняется приложение.

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Направляет компилятор MIDL для создания файлов заглушек или файла библиотеки типов для 32-разрядной среды.

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * *


</dt> <dd>

Направляет компилятор MIDL для создания файлов заглушек или файла библиотеки типов для среды архитектуры Intel 64-bit (IA64).

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>AMD64 * * * *


</dt> <dd>

Направляет компилятор MIDL для создания файлов заглушек или файла библиотеки типов для среды с расширенными микроустройствами 64-бит (AMD64).

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span id="win64"></span><span id="WIN64"></span>Win64 * * * *


</dt> <dd>

Такое же поведение, что и для *ia64*.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Параметр **/env** в основном влияет на уровень упаковки, используемый для структур в этой среде. Убедитесь, что задан один и тот же параметр уровня упаковки для компилятора MIDL и компилятора C.

Параметр **/env** определяет уровень упаковки и другие параметры следующим образом.

-   При указании **Win32** созданные заглушки используют для всех типов, участвующих в удаленных операциях, уровень упаковки C-компилятора 8. Типы данных [**int**](int.md) — 32 бит. Указатели — это 32 бит.
-   При указании **ia64** или **AMD64** компилятор MIDL выполняется в режиме кросс-компилятора для указанной (Intel или AMD) 64-разрядной платформы. Созданные заглушки используют для всех типов, участвующих в удаленных операциях, уровень упаковки C-компилятора 8. Типы данных [**Long**](long.md) и [**int**](int.md) — 32 бит. Указатели — это 64 бит.

Параметры [**/align**](-align.md), [**/Pack**](-pack.md)и [**/Zp**](-zp.md) имеют приоритет над параметрами **/env** .

Дополнительные сведения о 64-разрядной поддержке MIDL и RPC см. в статье [Разработка интерфейсов, совместимых с 64](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).

## <a name="examples"></a>Примеры

**MIDL/env Win32 filename. idl**

**MIDL/env ia64 filename. idl**

**MIDL/env AMD64 filename. idl**

**MIDL/env Win64 filename. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 