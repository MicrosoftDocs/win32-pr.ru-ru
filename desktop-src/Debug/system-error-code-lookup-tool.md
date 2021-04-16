---
description: Описание использования средства Microsoft Error Lookup для поиска текстовых объяснений шестнадцатеричных кодов ошибок в Windows.
title: Средство поиска ошибок (Майкрософт)
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719256"
---
# <a name="the-microsoft-error-lookup-tool"></a>Средство поиска ошибок (Майкрософт)

Средство поиска ошибок (Майкрософт) отображает текст сообщения, связанного с шестнадцатеричным кодом состояния (или другим кодом). Этот текст определен в различных файлах заголовков исходного кода Майкрософт, таких как Winerror. h, Setupapi. h и т. д.

Средство подписано цифровой подписью корпорации Майкрософт. Ниже приведены сведения о SHA256 для скачивания файла.  

|Алгоритм |Хэш |
| --- | --- |
|SHA256 |88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A |

> [!NOTE]
> Бизнес-среды могут ограничивать, какие файлы могут выполняться и откуда. Перед загрузкой и запуском этого средства ознакомьтесь со следующими сведениями:
> - Требуется ли разрешение или исключение безопасности для загрузки или запуска средства?
> - Можно ли хранить и запускать этот инструмент на компьютере (например, в папке "документы")? Или необходимо сохранить и запустить средство на специализированном компьютере, например на центральном файловом сервере?

## <a name="usage"></a>Использование

1. Скачайте средство, щелкнув [эту ссылку](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).
1. Если вы не указали расположение на шаге 1, перейдите в папку загрузки и скопируйте или переместите скачанный файл (Err_6.4.5.exe) в папку, в которой будет храниться средство. Не нужно расширять или устанавливать этот файл.
   > [!NOTE]
   > При копировании или перемещении файла в папку, указанную в переменной среды **path** операционной системы, она будет работать в любой командной строке.

1. Откройте окно командной строки и При необходимости измените каталог на расположение средства поиска ошибок.
1. Выполните следующую команду:
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > В этой команде \<*error code*> представляет шестнадцатеричный код, который требуется найти.

## <a name="examples"></a>Примеры

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a>Дополнительные сведения

Помните, что это средство «точка во времени». Средство поиска ошибок (Майкрософт) декодирует большинство кодов ошибок Майкрософт на дату компиляции инструмента. Новые выпуски Windows добавляют новые коды событий и ошибок, поэтому может потребоваться Скачать новую версию средства поиска ошибок. Проверьте наличие новой версии в центре загрузки Майкрософт или просмотрите [коды ошибок](system-error-codes.md).
