---
description: Использует разницу и источник (предоставленные в виде буферов) для создания новой копии целевых данных. Выходные данные возвращаются в буфер, выделенный Мсделта.
title: Функция ApplyDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 2a6034ca101a192be66db1b16a4ac7b27e7288d9453dfaaab5782e55e11d4c67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079764"
---
# <a name="applydeltab-function"></a>Функция ApplyDeltaB

Использует разницу и источник (предоставленные в виде буферов) для создания новой копии целевых данных. Выходные данные возвращаются в буфер, выделенный Мсделта.

> [!NOTE]
> Необходимо вызвать [делтафри](msdelta-deltafree.md) , чтобы освободить выходной буфер после завершения этой функции.

> [!NOTE]
> Если указанная Дельта была создана с помощью [патчапи](patchapi.md)и установлен флаг [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , мсделта будет вызывать патчапи для применения разницы.

## <a name="syntax"></a>Синтаксис

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a>Параметры

*апплифлагс*

окне Либо [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , либо [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).

*Источник*

окне Структура [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) , содержащая указатель на буфер, содержащий исходные данные.

*Разностная версия*

окне Структура [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) , содержащая указатель на буфер, содержащий разностные данные.

*лптаржет*

заполняет Указатель на структуру [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) , в которой будет записан целевой объект.

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
