---
description: Отправляет данные конфигурации для отслеживания данных.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'Метод ИРТК:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650516"
---
# <a name="irtcconfigure-method"></a><span data-ttu-id="db90d-103">Метод ИРТК:: Configure</span><span class="sxs-lookup"><span data-stu-id="db90d-103">IRTC::Configure method</span></span>

<span data-ttu-id="db90d-104">Метод [**Configure**](configure.md) отправляет данные конфигурации для отслеживания данных.</span><span class="sxs-lookup"><span data-stu-id="db90d-104">The [**Configure**](configure.md) method submits configuration data for a data capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="db90d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db90d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="db90d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db90d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db90d-107">*хконфигуратионблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db90d-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db90d-108">Маркер для большого двоичного объекта, настроенного вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="db90d-108">A handle to the BLOB that is configured by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="db90d-109">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db90d-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db90d-110">Маркер для большого двоичного объекта ошибок, который содержит дополнительные данные об ошибке.</span><span class="sxs-lookup"><span data-stu-id="db90d-110">A handle to an error BLOB that contains additional error data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db90d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db90d-111">Return value</span></span>

<span data-ttu-id="db90d-112">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="db90d-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="db90d-113">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="db90d-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="db90d-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="db90d-114">Return code</span></span>                                                                                                         | <span data-ttu-id="db90d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="db90d-115">Description</span></span>                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db90d-116"><dt>**\_BLOB-объект нмерр \_ не \_ инициализирован**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-116"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="db90d-117">Метод **CreateBlob** не был вызван.</span><span class="sxs-lookup"><span data-stu-id="db90d-117">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                 |
| <dl> <span data-ttu-id="db90d-118"><dt>**НМЕРР \_ Недопустимый \_ BLOB-объект**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-118"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="db90d-119">Объект, на который указывает, не является BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="db90d-119">The object pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="db90d-120"><dt>**\_BLOB-объект верхнего уровня нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-120"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="db90d-121">Неправильный номер версии большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="db90d-121">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="db90d-122"><dt>**\_запись BLOB-объекта нмерр \_ \_ уже \_ существует**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-122"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="db90d-123">Дублирование большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="db90d-123">Duplicate BLOB.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="db90d-124"><dt>**\_запись BLOB-объекта нмерр \_ \_ \_ не \_ существует**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-124"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="db90d-125">Большой двоичный объект конфигурации, заданный параметром *хконфигуратионблоб* , не имеет записи, необходимой для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="db90d-125">The configuration BLOB specified by *hConfigurationBlob* lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="db90d-126">Просмотрите большой двоичный объект ошибки, возвращенный *херрорблоб* , чтобы определить, какая запись не найдена.</span><span class="sxs-lookup"><span data-stu-id="db90d-126">View the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="db90d-127"><dt>**\_спецификатор неоднозначных нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-127"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="db90d-128">Отсутствуют данные о владельце или категории большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="db90d-128">The BLOB Owner or Category data is missing.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="db90d-129"><dt>**\_ \_ \_ не найден владелец BLOB-объекта нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-129"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="db90d-130">Раздел владельца большого двоичного объекта не найден.</span><span class="sxs-lookup"><span data-stu-id="db90d-130">The BLOB Owner section was not found.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="db90d-131"><dt>**\_Категория BLOB-объектов нмерр \_ \_ не \_ найдена**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-131"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="db90d-132">Раздел категории BLOB-объектов не найден.</span><span class="sxs-lookup"><span data-stu-id="db90d-132">The BLOB Category section was not found.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="db90d-133"><dt>**НМЕРР \_ неизвестная \_ Категория**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-133"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="db90d-134">Раздел категории BLOB-объектов был найден, но не распознан.</span><span class="sxs-lookup"><span data-stu-id="db90d-134">The BLOB Category section was found, but not understood.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="db90d-135"><dt>**НМЕРР \_ неизвестный \_ тег**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-135"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="db90d-136">Раздел тега BLOB-объекта найден, но не распознан.</span><span class="sxs-lookup"><span data-stu-id="db90d-136">The BLOB Tag section was found, but not understood.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="db90d-137"><dt>**\_Ошибка преобразования BLOB-объекта нмерр \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-137"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="db90d-138">Большой двоичный объект поврежден.</span><span class="sxs-lookup"><span data-stu-id="db90d-138">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="db90d-139"><dt>**НМЕРР \_ Недопустимый \_ триггер**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-139"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="db90d-140">Повреждена часть триггера большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="db90d-140">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="db90d-141"><dt>**\_ \_ Недопустимая строка большого двоичного объекта нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-141"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="db90d-142">Строка не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="db90d-142">The string is not null-terminated.</span></span><br/>                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="db90d-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db90d-143">Remarks</span></span>

<span data-ttu-id="db90d-144">Этот метод необходимо применить для перезапуска НПП, который был запущен, остановлен, но не отключен.</span><span class="sxs-lookup"><span data-stu-id="db90d-144">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="db90d-145">BLOB-объект ошибки, возвращенный *херрорблоб* , содержит записи, которые сетевой монитор не удалось распознать или найти в большом двоичном объекте конфигурации, указанном в *хконфигуратионблоб*.</span><span class="sxs-lookup"><span data-stu-id="db90d-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="db90d-146">Возвращенный BLOB-объект ошибки содержит данные об ошибке, которые приложение может использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="db90d-146">The returned error BLOB contains error data that the application can use for troubleshooting.</span></span> <span data-ttu-id="db90d-147">Например, если \_ запись BLOB-объекта нмерр \_ \_ \_ не \_ существует, запись, сетевой монитор не удается найти, включается в возвращенный большой двоичный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="db90d-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor cannot find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="db90d-148">Требования</span><span class="sxs-lookup"><span data-stu-id="db90d-148">Requirements</span></span>



| <span data-ttu-id="db90d-149">Требование</span><span class="sxs-lookup"><span data-stu-id="db90d-149">Requirement</span></span> | <span data-ttu-id="db90d-150">Значение</span><span class="sxs-lookup"><span data-stu-id="db90d-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db90d-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db90d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="db90d-152">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db90d-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="db90d-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db90d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="db90d-154">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db90d-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="db90d-155">Заголовок</span><span class="sxs-lookup"><span data-stu-id="db90d-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="db90d-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="db90d-157">DLL</span><span class="sxs-lookup"><span data-stu-id="db90d-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db90d-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db90d-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db90d-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db90d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db90d-160">иртк</span><span class="sxs-lookup"><span data-stu-id="db90d-160">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="db90d-161">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="db90d-161">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="db90d-162">сетевой монитор большие двоичные объекты</span><span class="sxs-lookup"><span data-stu-id="db90d-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




