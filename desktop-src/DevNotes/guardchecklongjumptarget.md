---
UID: ''
title: Функция Гуардчекклонгжумптаржет
description: Пытается проверить, является ли целевой объект longjmp допустимым.
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "105654277"
---
# <a name="guardchecklongjumptarget-function"></a>Функция Гуардчекклонгжумптаржет

## <a name="description"></a>Описание

Пытается проверить, является ли целевой объект [longjmp](/cpp/c-runtime-library/reference/longjmp) допустимым для процесса, в котором включена [Защита потока управления (cfg)](../secbp/control-flow-guard.md) .

Если целевой адрес соответствует сопоставлению изображений, то для двоичного файла извлекаются допустимые целевые объекты.
Функция использует эти целевые объекты для проверки целевого объекта.
Если двоичный файл не имеет метаданных, описывающих набор допустимых целевых объектов *longjmp* , функция возвращает **значение true**.

Если целевой адрес соответствует сопоставлению без образов, как в JIT-коде, для определения того, разрешен ли переход, используется глобальная политика только для чтения.

## <a name="parameters"></a>Параметры

### <a name="targetaddress-in"></a>TargetAddress [in]

Целевой адрес для перехода.

### <a name="flags-in"></a>Flags [in]

Флаги, описывающие операцию, которая должна быть выполнена с адресом.
Если указать **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), эта функция не прерывает процесс, если целевой объект является недопустимым.

## <a name="returns"></a>Возвращаемое значение

**Значение true** , если целевой объект является допустимым; в противном случае — **значение false**.

## <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел
