---
description: Программа проверки системных файлов, Sfc.exe, позволяет администраторам сканировать все защищенные ресурсы, чтобы проверить их версии.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: " средство проверки системных файлов"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f751aa30c06dbff90b8d5221974236b45edf9f0f278c144f755568a0040f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330286"
---
# <a name="system-file-checker"></a> средство проверки системных файлов

Программа проверки системных файлов, Sfc.exe, позволяет администраторам сканировать все защищенные ресурсы, чтобы проверить их версии.

файлы, критические для перезапуска Windows, не соответствующие ожидаемой версии Windows, могут быть заменены на правильные версии. При восстановлении файла также восстанавливаются соответствующие данные реестра. защищенные файлы, не критические для перезапуска Windows, не восстанавливаются.

## <a name="syntax"></a>Синтаксис

Ниже приведен синтаксис командной строки для SFC.

**Параметры SFC \[ = полный путь к файлу\]**

## <a name="options"></a>Параметры

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/КАЧЕСИЗЕ =*x*
</dt> <dd>

Это значение не поддерживается.

**Windows Server 2003 и Windows XP:** Задает размер файлового кэша. Размер кэша по умолчанию — 0x32 (50 МБ).

</dd> <dt>

<span id="_CANCEL"></span><span id="_cancel"></span>/канцел
</dt> <dd>

Это значение не поддерживается.

</dd> <dt>

<span id="_ENABLE"></span><span id="_enable"></span>Разрешение
</dt> <dd>

Это значение не поддерживается.

</dd> <dt>

<span id="_FILESONLY"></span><span id="_filesonly"></span>/филесонли
</dt> <dd>

Проверьте или исправьте только файлы. Не проверять и не восстанавливать разделы реестра.

**Windows XP:** Не поддерживается.

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/оффбутдир
</dt> <dd>

Используйте этот параметр для автономного восстановления. Укажите расположение каталога автономной загрузки.

**Windows XP:** Не поддерживается.

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/оффвиндир
</dt> <dd>

Используйте этот параметр для автономного восстановления. укажите расположение автономного Windows каталога.

**Windows XP:** Не поддерживается.

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/пуржекаче
</dt> <dd>

Это значение не поддерживается.

**Windows Server 2003 и Windows XP:** Очищает файловый кэш и сканирует все защищенные системные файлы.

</dd> <dt>

<span id="_QUIET"></span><span id="_quiet"></span>/QUIET
</dt> <dd>

Это значение не поддерживается.

</dd> <dt>

<span id="_REVERT"></span><span id="_revert"></span>/реверт
</dt> <dd>

Вернитесь к параметрам по умолчанию.

**Windows Server 2008 и Windows Vista:** Не поддерживается.

</dd> <dt>

<span id="_SCANBOOT"></span><span id="_scanboot"></span>/сканбут
</dt> <dd>

Это значение не поддерживается.

**Windows Server 2003 и Windows XP:** Сканирует все защищенные системные файлы при каждой загрузке.

</dd> <dt>

<span id="_SCANFILE"></span><span id="_scanfile"></span>/сканфиле
</dt> <dd>

Сканирует и восстанавливает файл, расположенный по указанному полному пути.

**Windows XP:** Не поддерживается.

</dd> <dt>

<span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW
</dt> <dd>

Немедленно сканирует все защищенные системные файлы.

</dd> <dt>

<span id="_SCANONCE"></span><span id="_scanonce"></span>/сканонце
</dt> <dd>

Это значение не поддерживается.

**Windows Server 2003 и Windows XP:** Сканирует все защищенные системные файлы при следующей загрузке.

</dd> <dt>

<span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/верифифиле
</dt> <dd>

Проверяет файл по указанному полному пути. Этот параметр не восстанавливает файл.

**Windows XP:** Не поддерживается.

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/верифйонли
</dt> <dd>

Сканирует все защищенные системные файлы, но не восстанавливает их.

**Windows XP:** Не поддерживается.

</dd> </dl>

SFC устанавливает следующее значение реестра:

 = HKEY на \_ локальном \_ компьютере \\ программное обеспечение \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ сфкскан

Дополнительные сведения см. в разделе [значения реестра WFP](wfp-registry-values.md).

## <a name="remarks"></a>Remarks

только в Windows Vista для переменной среды **\_ \_ журнала трассировки Windows** можно задать расположение допустимого каталога для получения файла журнала.

## <a name="examples"></a>Примеры

В примерах командных строк приведены примеры синтаксиса sfc.exe.

**sfc/SCANNOW**

**SFC/ВЕРИФИФИЛЕ = c: \\ Windows \\ system32 \\kernel32.dll**

**SFC/СКАНФИЛЕ = d: \\ Windows \\ system32 \\kernel32.dll/оффбутдир = d: \\ /оффвиндир = d: \\ Windows**

**SFC/ВЕРИФЙОНЛИ/ФИЛЕСОНЛИ**

 

 



