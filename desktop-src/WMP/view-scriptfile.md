---
title: VIEW. scriptFile
description: атрибут scriptFile указывает имена файлов сопутствующих JScript файлов.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- просмотреть. scriptFile проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f22b0fb5f0815c8977a363c033d26c0d68f725e0cdcd546bc2f2c1a7b723c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615334"
---
# <a name="viewscriptfile"></a>VIEW. scriptFile

атрибут **scriptFile** указывает имена файлов сопутствующих JScript файлов.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** только для записи и не имеет значения по умолчанию. имена файлов нескольких JScript разделяются точкой с запятой. Не должны присутствовать начальные и следующие пробелы и точки с запятой.

## <a name="remarks"></a>Remarks

Код в указанных файлах может использоваться любым обработчиком событий в представлении. Код, используемый обработчиками событий в нескольких представлениях, может быть помещен в файл с тем же именем, что и файл определения обложки, но с расширением .js, а не с расширением WMS. Этот файл загружается автоматически, и его не нужно указывать в файле определения обложки.

## <a name="examples"></a>Примеры


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**VIEW, элемент**](view-element.md)
</dt> </dl>

 

 





