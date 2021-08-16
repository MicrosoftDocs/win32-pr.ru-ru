---
description: Методы, используемые для работы с файлами DirectX. x, могут возвращать следующие значения в дополнение к стандартным возвращаемым значениям COM. Не рекомендуется.
ms.assetid: a91168bc-966a-47b5-ba83-fc480593228d
title: Возвращаемые значения (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Return
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 51bc2155a74daf15945a79714355bdace06672c348dfd75679156f812d3d42be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122481"
---
# <a name="return-values-dxfileh"></a>Возвращаемые значения (Дксфиле. h)

Методы, используемые для работы с файлами DirectX. x, могут возвращать следующие значения в дополнение к стандартным возвращаемым значениям COM. Не рекомендуется.

<dl> <dt>

<span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**ДКСФИЛЕ \_ ОК**
</dt> <dd>

Команда успешно выполнена.

</dd> <dt>

<span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**ДКСФИЛИРР \_ бадаллок**
</dt> <dd>

Ошибка выделения памяти.

</dd> <dt>

<span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**ДКСФИЛИРР \_ бадаррайсизе**
</dt> <dd>

Недопустимый размер массива.

</dd> <dt>

<span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**ДКСФИЛИРР \_ бадкачефиле**
</dt> <dd>

Файл кэша, содержащий дату файла. x, недопустим. Файл кэша содержит данные, полученные из сети, кэшированные на жестком диске и получаемые в последующих запросах.

</dd> <dt>

<span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**ДКСФИЛИРР \_ баддатареференце**
</dt> <dd>

Недопустимая ссылка на данные.

</dd> <dt>

<span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**ДКСФИЛИРР \_ бадфиле**
</dt> <dd>

Недопустимый файл.

</dd> <dt>

<span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**ДКСФИЛИРР \_ бадфилекомпрессионтипе**
</dt> <dd>

Недопустимый тип сжатия файла.

</dd> <dt>

<span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**ДКСФИЛИРР \_ бадфилефлоатсизе**
</dt> <dd>

Размер с плавающей запятой недопустим.

</dd> <dt>

<span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**ДКСФИЛИРР \_ бадфилетипе**
</dt> <dd>

Файл не является файлом DirectX. x.

</dd> <dt>

<span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**ДКСФИЛИРР \_ бадфилеверсион**
</dt> <dd>

Недопустимая версия файла.

</dd> <dt>

<span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**ДКСФИЛИРР \_ бадинтринсикс**
</dt> <dd>

Недопустимые встроенные функции.

</dd> <dt>

<span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**ДКСФИЛИРР \_ бадобжект**
</dt> <dd>

Объект недействителен.

</dd> <dt>

<span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**ДКСФИЛИРР \_ бадресаурце**
</dt> <dd>

Недопустимый ресурс.

</dd> <dt>

<span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**ДКСФИЛИРР \_ бадстреамхандле**
</dt> <dd>

Недопустимый обработчик потока.

</dd> <dt>

<span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**ДКСФИЛИРР \_ бадтипе**
</dt> <dd>

Недопустимый тип объекта.

</dd> <dt>

<span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**ДКСФИЛИРР \_ бадвалуе**
</dt> <dd>

Недопустимый параметр.

</dd> <dt>

<span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**ДКСФИЛИРР \_ FILENOTFOUND**
</dt> <dd>

Не удалось найти файл.

</dd> <dt>

<span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**ДКСФИЛИРР \_ интерналеррор**
</dt> <dd>

Произошла внутренняя ошибка.

</dd> <dt>

<span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**ДКСФИЛИРР \_ Интернета**
</dt> <dd>

Не удалось найти подключение к Интернету.

</dd> <dt>

<span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**ДКСФИЛИРР \_ номоредата**
</dt> <dd>

Дополнительные данные недоступны.

</dd> <dt>

<span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**ДКСФИЛИРР \_ номореобжектс**
</dt> <dd>

Все объекты были перечислены.

</dd> <dt>

<span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**ДКСФИЛИРР \_ номорестреамхандлес**
</dt> <dd>

Нет доступных дескрипторов потока.

</dd> <dt>

<span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**ДКСФИЛИРР \_ нотдонэйет**
</dt> <dd>

Операция не завершена.

</dd> <dt>

<span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**ДКСФИЛИРР \_ NotFound**
</dt> <dd>

Не удалось найти объект.

</dd> <dt>

<span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**ДКСФИЛИРР \_ парсиррор**
</dt> <dd>

Не удалось выполнить синтаксический анализ файла.

</dd> <dt>

<span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**ДКСФИЛИРР \_ RESOURCENOTFOUND**
</dt> <dd>

Не удалось найти ресурс.

</dd> <dt>

<span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**\_шаблон дксфилирр**
</dt> <dd>

Нет доступных шаблонов.

</dd> <dt>

<span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**ДКСФИЛИРР \_ урлнотфаунд**
</dt> <dd>

Не удалось найти URL-адрес.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Дксфиле. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Ссылка на X-файл (устаревшая)](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 




