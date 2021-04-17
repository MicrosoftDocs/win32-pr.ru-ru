---
title: ЕКУАЛИЗЕРСЕТТИНГС. Нормализация
description: Атрибут нормализации указывает или получает значение, указывающее, включена ли нормализация.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- ЕКУАЛИЗЕРСЕТТИНГС. Нормализация проигрывателя Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694781"
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
| true  | Нормализация включена.           |
| false | По умолчанию. Нормализация отключена. |



 

## <a name="remarks"></a>Комментарии

Если нормализация включена, то звуковой сигнал для всего файла цифрового носителя масштабируется до максимального значения. Это позволяет воспроизводить несколько файлов приблизительно на одном томе, не требуя настройки томов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС, элемент**](equalizersettings-element.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. Нормализатионавераже**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. Нормализатионпеак**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





