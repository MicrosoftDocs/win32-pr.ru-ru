---
description: Создает разницу между исходным и целевым объектом (предоставленными в виде буферов) и возвращает выходной результат в виде буфера, выделенного Мсделта.
title: Функция CreateDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: ae13dfb82d4699bbb8cc222b4cd1aaa2615e8efaa578de60483f00552faf2086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826928"
---
# <a name="createdeltab-function"></a>Функция CreateDeltaB

Создает разницу между исходным и целевым объектом (предоставленными в виде буферов) и возвращает выходной результат в виде буфера, выделенного Мсделта.

> [!NOTE]
> Необходимо вызвать [делтафри](msdelta-deltafree.md) , чтобы освободить выходной буфер после завершения этой функции.

## <a name="syntax"></a>Синтаксис

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a>Параметры

*филетипесет*

окне Значение [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) , указывающее тип файла, который должен использоваться для процесса создания.

*сетфлагс*

окне Одно или несколько значений [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , указывающих флаги, которые будут использоваться в процессе создания, а также флаги по умолчанию.

*ресетфлагс*

окне Одно или несколько значений [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , указывающих флаги по умолчанию, которые будут сброшены во время процесса создания.

*Источник*

окне Структура [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) , содержащая указатель на буфер, содержащий исходные данные.

*Целевой объект*

окне Структура [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) , содержащая указатель на буфер, содержащий целевые данные.

*саурцеоптионс*

[in] Зарезервировано. Передайте [DELTA_INPUTную](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) структуру с *редактируемым* значением **false**, для *Лпстарт* задайте **значение NULL** , а для *усизе* — значение 0.

*таржетоптионс*

[in] Зарезервировано. Передайте [DELTA_INPUTную](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) структуру с *редактируемым* значением **false**, для *Лпстарт* задайте **значение NULL** , а для *усизе* — значение 0.

*GlobalOptions*

[in] Зарезервировано. Передайте [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) структуру с параметром *лпстарт* , имеющим значение **null** , а *усизе* значение 0.

*лптаржетфилетиме*

окне Метка времени, заданная для целевого файла после применения разностной разницы. Если **значение равно NULL**, то конечная отметка времени будет текущим временем в процессе создания.

*хашалгид*

окне ALG_ID алгоритм, используемый для создания целевой сигнатуры. Некоторые специальные значения:

- 0 = нет подписи
- 32 = 32-разрядная CRC, определенная в msdelta.dll

*лпделта*

заполняет Указатель на структуру [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) , в которой будет записана Дельта.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**. Если функция возвращает **значение false**, можно вызвать [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить соответствующий код системной ошибки Win32.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| Заголовок | мсделта. h |
| DLL | msdelta.dll |
| Юникод | Неприменимо |

## <a name="see-also"></a>См. также

[мсделта](msdelta.md)

[делтафри](msdelta-deltafree.md)
