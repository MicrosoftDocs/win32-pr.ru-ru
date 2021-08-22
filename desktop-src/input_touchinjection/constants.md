---
title: Константы внедрения касаний
description: В этом разделе приведены справочные сведения по константам внедрения касаний.
ms.assetid: 52941DF1-88AF-452B-BF3E-838ADBDBC9B2
topic_type:
- apiref
api_name:
- MAX_TOUCH_COUNT
- TOUCH_FEEDBACK_DEFAULT
- TOUCH_FEEDBACK_INDIRECT
- TOUCH_FEEDBACK_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: d86af0d67c48218e8cb3f5909b647ff59d8b0cdddddef24057e02521a7f253ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451744"
---
# <a name="touch-injection-constants"></a>Константы внедрения касаний

В этом разделе приведены справочные сведения по константам [внедрения касаний](touch-injection-portal.md) .

| Константа/значение | Описание |
|---|---|
| **MAX_TOUCH_COUNT** 256                            | Указывает максимальное число одновременных контактов.<br/> |
| **TOUCH_FEEDBACK_DEFAULT** 0x1    | Указывает визуализации сенсорного ввода по умолчанию.<br/>                |
| **TOUCH_FEEDBACK_INDIRECT** 0x2 | Указывает непрямые сенсорные визуализации.<br/>               |
| **TOUCH_FEEDBACK_NONE** 0x3             | Указывает отсутствие сенсорных визуализаций.<br/>                     |

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента | Windows 8 \[ только классические приложения\]                                           |
| Минимальная версия сервера | Windows Server 2012 \[ только классические приложения\]                                 |
| Header                   | Winuser. h |

## <a name="see-also"></a>См. также раздел

[Справочник по внедрению касаний](touch-injection-reference.md)
