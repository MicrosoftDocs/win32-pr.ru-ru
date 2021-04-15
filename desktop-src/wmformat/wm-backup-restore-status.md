---
title: Структура WM_BACKUP_RESTORE_STATUS (Вмдрмсдк. h)
description: '\_Структура состояния восстановления резервной копии WM \_ \_ содержит сведения об ожидающей операции резервного копирования или восстановления лицензий.'
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- Формат WM_BACKUP_RESTORE_STATUS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708426"
---
# <a name="wm_backup_restore_status-structure"></a>\_ \_ Структура состояния восстановления резервной копии WM \_

Структура **\_ \_ \_ состояния восстановления резервной копии WM** содержит сведения об ожидающей операции резервного копирования или восстановления лицензий.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**естатус**
</dt> <dd>

Член перечисления [**\_ состояния Msdrm**](msdrm-status.md) , указывающий состояние.

</dd> <dt>

**бстреррор**
</dt> <dd>

Строка, содержащая ошибку.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура получается при вызове метода [**ивмдрмлиценсебаккупресторестатус::-Status**](iwmdrmlicensebackuprestorestatus-getstatus.md) . Он содержит состояние ожидающей операции резервного копирования или восстановления во время вызова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





