---
title: Параметры. том
description: Свойство Volume указывает или получает текущий том.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Параметры проигрыватель Windows Media тома
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c02952426a78323421fd779b253136c1777d509141d51b590b9db40c4d077a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002214"
---
# <a name="settingsvolume"></a>Параметры. том

Свойство **Volume** указывает или получает текущий том.

## <a name="syntax"></a>Синтаксис

проигрыватель. Settings. Volume

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** для чтения и записи (**длинное**) в диапазоне от 0 до 100.

## <a name="remarks"></a>Remarks

Ноль указывает на отсутствие тома и 100 указывает на полный том. Если для этого свойства не указано значение, по умолчанию используется последний параметр тома, установленный для проигрывателя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Параметры Объектами**](settings-object.md)
</dt> </dl>

 

 





