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
ms.openlocfilehash: 7d465b9759d958cba06bf0b950bc67772fbb84a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821197"
---
# <a name="return-values-dxfileh"></a><span data-ttu-id="5fe94-104">Возвращаемые значения (Дксфиле. h)</span><span class="sxs-lookup"><span data-stu-id="5fe94-104">Return Values (DXFile.h)</span></span>

<span data-ttu-id="5fe94-105">Методы, используемые для работы с файлами DirectX. x, могут возвращать следующие значения в дополнение к стандартным возвращаемым значениям COM.</span><span class="sxs-lookup"><span data-stu-id="5fe94-105">The methods used to work with DirectX .x files can return the following values in addition to the standard COM return values.</span></span> <span data-ttu-id="5fe94-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5fe94-106">Deprecated.</span></span>

<dl> <dt>

<span data-ttu-id="5fe94-107"><span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**ДКСФИЛЕ \_ ОК**</span><span class="sxs-lookup"><span data-stu-id="5fe94-107"><span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-108">Команда успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="5fe94-108">Command completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-109"><span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**ДКСФИЛИРР \_ бадаллок**</span><span class="sxs-lookup"><span data-stu-id="5fe94-109"><span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**DXFILEERR\_BADALLOC**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-110">Ошибка выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="5fe94-110">Memory allocation failed.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-111"><span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**ДКСФИЛИРР \_ бадаррайсизе**</span><span class="sxs-lookup"><span data-stu-id="5fe94-111"><span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**DXFILEERR\_BADARRAYSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-112">Недопустимый размер массива.</span><span class="sxs-lookup"><span data-stu-id="5fe94-112">Array size is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-113"><span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**ДКСФИЛИРР \_ бадкачефиле**</span><span class="sxs-lookup"><span data-stu-id="5fe94-113"><span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**DXFILEERR\_BADCACHEFILE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-114">Файл кэша, содержащий дату файла. x, недопустим.</span><span class="sxs-lookup"><span data-stu-id="5fe94-114">The cache file containing the .x file date is invalid.</span></span> <span data-ttu-id="5fe94-115">Файл кэша содержит данные, полученные из сети, кэшированные на жестком диске и получаемые в последующих запросах.</span><span class="sxs-lookup"><span data-stu-id="5fe94-115">A cache file contains data retrieved from the network, cached on the hard disk, and retrieved in subsequent requests.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-116"><span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**ДКСФИЛИРР \_ баддатареференце**</span><span class="sxs-lookup"><span data-stu-id="5fe94-116"><span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**DXFILEERR\_BADDataReference**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-117">Недопустимая ссылка на данные.</span><span class="sxs-lookup"><span data-stu-id="5fe94-117">Data reference is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-118"><span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**ДКСФИЛИРР \_ бадфиле**</span><span class="sxs-lookup"><span data-stu-id="5fe94-118"><span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**DXFILEERR\_BADFILE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-119">Недопустимый файл.</span><span class="sxs-lookup"><span data-stu-id="5fe94-119">File is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-120"><span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**ДКСФИЛИРР \_ бадфилекомпрессионтипе**</span><span class="sxs-lookup"><span data-stu-id="5fe94-120"><span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**DXFILEERR\_BADFILECOMPRESSIONTYPE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-121">Недопустимый тип сжатия файла.</span><span class="sxs-lookup"><span data-stu-id="5fe94-121">File compression type is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-122"><span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**ДКСФИЛИРР \_ бадфилефлоатсизе**</span><span class="sxs-lookup"><span data-stu-id="5fe94-122"><span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**DXFILEERR\_BADFILEFLOATSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-123">Размер с плавающей запятой недопустим.</span><span class="sxs-lookup"><span data-stu-id="5fe94-123">Floating-point size is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-124"><span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**ДКСФИЛИРР \_ бадфилетипе**</span><span class="sxs-lookup"><span data-stu-id="5fe94-124"><span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**DXFILEERR\_BADFILETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-125">Файл не является файлом DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="5fe94-125">File is not a DirectX .x file.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-126"><span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**ДКСФИЛИРР \_ бадфилеверсион**</span><span class="sxs-lookup"><span data-stu-id="5fe94-126"><span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**DXFILEERR\_BADFILEVERSION**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-127">Недопустимая версия файла.</span><span class="sxs-lookup"><span data-stu-id="5fe94-127">File version is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-128"><span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**ДКСФИЛИРР \_ бадинтринсикс**</span><span class="sxs-lookup"><span data-stu-id="5fe94-128"><span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**DXFILEERR\_BADINTRINSICS**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-129">Недопустимые встроенные функции.</span><span class="sxs-lookup"><span data-stu-id="5fe94-129">Intrinsics are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-130"><span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**ДКСФИЛИРР \_ бадобжект**</span><span class="sxs-lookup"><span data-stu-id="5fe94-130"><span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**DXFILEERR\_BADOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-131">Объект недействителен.</span><span class="sxs-lookup"><span data-stu-id="5fe94-131">Object is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-132"><span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**ДКСФИЛИРР \_ бадресаурце**</span><span class="sxs-lookup"><span data-stu-id="5fe94-132"><span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**DXFILEERR\_BADRESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-133">Недопустимый ресурс.</span><span class="sxs-lookup"><span data-stu-id="5fe94-133">Resource is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-134"><span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**ДКСФИЛИРР \_ бадстреамхандле**</span><span class="sxs-lookup"><span data-stu-id="5fe94-134"><span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**DXFILEERR\_BADSTREAMHANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-135">Недопустимый обработчик потока.</span><span class="sxs-lookup"><span data-stu-id="5fe94-135">Stream handle is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-136"><span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**ДКСФИЛИРР \_ бадтипе**</span><span class="sxs-lookup"><span data-stu-id="5fe94-136"><span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**DXFILEERR\_BADTYPE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-137">Недопустимый тип объекта.</span><span class="sxs-lookup"><span data-stu-id="5fe94-137">Object type is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-138"><span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**ДКСФИЛИРР \_ бадвалуе**</span><span class="sxs-lookup"><span data-stu-id="5fe94-138"><span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**DXFILEERR\_BADVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-139">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="5fe94-139">Parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-140"><span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**ДКСФИЛИРР \_ FILENOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="5fe94-140"><span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**DXFILEERR\_FILENOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-141">Не удалось найти файл.</span><span class="sxs-lookup"><span data-stu-id="5fe94-141">File could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-142"><span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**ДКСФИЛИРР \_ интерналеррор**</span><span class="sxs-lookup"><span data-stu-id="5fe94-142"><span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**DXFILEERR\_INTERNALERROR**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-143">Произошла внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="5fe94-143">Internal error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-144"><span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**ДКСФИЛИРР \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="5fe94-144"><span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR\_NOINTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-145">Не удалось найти подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="5fe94-145">Internet connection not found.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-146"><span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**ДКСФИЛИРР \_ номоредата**</span><span class="sxs-lookup"><span data-stu-id="5fe94-146"><span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**DXFILEERR\_NOMOREDATA**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-147">Дополнительные данные недоступны.</span><span class="sxs-lookup"><span data-stu-id="5fe94-147">No further data is available.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-148"><span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**ДКСФИЛИРР \_ номореобжектс**</span><span class="sxs-lookup"><span data-stu-id="5fe94-148"><span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**DXFILEERR\_NOMOREOBJECTS**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-149">Все объекты были перечислены.</span><span class="sxs-lookup"><span data-stu-id="5fe94-149">All objects have been enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-150"><span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**ДКСФИЛИРР \_ номорестреамхандлес**</span><span class="sxs-lookup"><span data-stu-id="5fe94-150"><span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**DXFILEERR\_NOMORESTREAMHANDLES**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-151">Нет доступных дескрипторов потока.</span><span class="sxs-lookup"><span data-stu-id="5fe94-151">No stream handles are available.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-152"><span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**ДКСФИЛИРР \_ нотдонэйет**</span><span class="sxs-lookup"><span data-stu-id="5fe94-152"><span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**DXFILEERR\_NOTDONEYET**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-153">Операция не завершена.</span><span class="sxs-lookup"><span data-stu-id="5fe94-153">Operation has not completed.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-154"><span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**ДКСФИЛИРР \_ NotFound**</span><span class="sxs-lookup"><span data-stu-id="5fe94-154"><span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**DXFILEERR\_NOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-155">Не удалось найти объект.</span><span class="sxs-lookup"><span data-stu-id="5fe94-155">Object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-156"><span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**ДКСФИЛИРР \_ парсиррор**</span><span class="sxs-lookup"><span data-stu-id="5fe94-156"><span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR\_PARSEERROR**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-157">Не удалось выполнить синтаксический анализ файла.</span><span class="sxs-lookup"><span data-stu-id="5fe94-157">File could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-158"><span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**ДКСФИЛИРР \_ RESOURCENOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="5fe94-158"><span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**DXFILEERR\_RESOURCENOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-159">Не удалось найти ресурс.</span><span class="sxs-lookup"><span data-stu-id="5fe94-159">Resource could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-160"><span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**\_шаблон дксфилирр**</span><span class="sxs-lookup"><span data-stu-id="5fe94-160"><span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**DXFILEERR\_NOTEMPLATE**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-161">Нет доступных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="5fe94-161">No template available.</span></span>

</dd> <dt>

<span data-ttu-id="5fe94-162"><span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**ДКСФИЛИРР \_ урлнотфаунд**</span><span class="sxs-lookup"><span data-stu-id="5fe94-162"><span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**DXFILEERR\_URLNOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="5fe94-163">Не удалось найти URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5fe94-163">URL could not be found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fe94-164">Требования</span><span class="sxs-lookup"><span data-stu-id="5fe94-164">Requirements</span></span>



| <span data-ttu-id="5fe94-165">Требование</span><span class="sxs-lookup"><span data-stu-id="5fe94-165">Requirement</span></span> | <span data-ttu-id="5fe94-166">Значение</span><span class="sxs-lookup"><span data-stu-id="5fe94-166">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe94-167">Header</span><span class="sxs-lookup"><span data-stu-id="5fe94-167">Header</span></span><br/> | <dl> <span data-ttu-id="5fe94-168"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fe94-168"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fe94-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fe94-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe94-170">Ссылка на X-файл (устаревшая)</span><span class="sxs-lookup"><span data-stu-id="5fe94-170">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 




