---
title: Settings. Volume
description: Свойство Volume указывает или получает текущий том.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Проигрыватель Windows Media Settings. Volume
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
ms.openlocfilehash: e0f5ec4299bf33ed16143eec8570b65c548599e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651842"
---
# <a name="settingsvolume"></a>Settings. Volume

Свойство **Volume** указывает или получает текущий том.

## <a name="syntax"></a>Синтаксис

проигрыватель. Settings. Volume

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** для чтения и записи (**длинное**) в диапазоне от 0 до 100.

## <a name="remarks"></a>Комментарии

Ноль указывает на отсутствие тома и 100 указывает на полный том. Если для этого свойства не указано значение, по умолчанию используется последний параметр тома, установленный для проигрывателя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект параметров**](settings-object.md)
</dt> </dl>

 

 





