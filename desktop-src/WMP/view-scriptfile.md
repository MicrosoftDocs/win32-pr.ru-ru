---
title: VIEW. scriptFile
description: Атрибут scriptFile указывает имена файлов сопутствующих файлов JScript.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- Просмотреть. scriptFile проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648905"
---
# <a name="viewscriptfile"></a>VIEW. scriptFile

Атрибут **scriptFile** указывает имена файлов сопутствующих файлов JScript.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** только для записи и не имеет значения по умолчанию. Имена файлов нескольких файлов JScript разделяются точкой с запятой. Не должны присутствовать начальные и следующие пробелы и точки с запятой.

## <a name="remarks"></a>Комментарии

Код в указанных файлах может использоваться любым обработчиком событий в представлении. Код, используемый обработчиками событий в нескольких представлениях, может быть помещен в файл с тем же именем, что и файл определения обложки, но с расширением. js, а не с расширением WMS. Этот файл загружается автоматически, и его не нужно указывать в файле определения обложки.

## <a name="examples"></a>Примеры


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**VIEW, элемент**](view-element.md)
</dt> </dl>

 

 





