---
title: ЕКУАЛИЗЕРСЕТТИНГС. Нормализация
description: Атрибут нормализации указывает или получает значение, указывающее, включена ли нормализация.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- проигрыватель Windows Media екуализерсеттингс. нормализация
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f2befdd62f0508822d5547cb3b894b93ea095f52db4cf9bbdb4a444d99251c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578174"
---
# <a name="equalizersettingsnormalization"></a>ЕКУАЛИЗЕРСЕТТИНГС. Нормализация

Атрибут **нормализации** указывает или получает значение, указывающее, включена ли нормализация.

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **логическим значением** для чтения и записи.



| Значение | Описание                         |
|-------|-------------------------------------|
| Да  | Нормализация включена.           |
| false | По умолчанию. Нормализация отключена. |



 

## <a name="remarks"></a>Remarks

Если нормализация включена, то звуковой сигнал для всего файла цифрового носителя масштабируется до максимального значения. Это позволяет воспроизводить несколько файлов приблизительно на одном томе, не требуя настройки томов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС, элемент**](equalizersettings-element.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. Нормализатионавераже**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. Нормализатионпеак**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





