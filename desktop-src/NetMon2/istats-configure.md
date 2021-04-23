---
description: Метод Configure отправляет сведения о конфигурации записи.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: 'Метод Истатс:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9f2dddea3132ce81a57f16737c0f90c6277d4efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272063"
---
# <a name="istatsconfigure-method"></a><span data-ttu-id="945d6-103">Метод Истатс:: Configure</span><span class="sxs-lookup"><span data-stu-id="945d6-103">IStats::Configure method</span></span>

<span data-ttu-id="945d6-104">Метод **Configure** отправляет сведения о конфигурации записи.</span><span class="sxs-lookup"><span data-stu-id="945d6-104">The **Configure** method submits capture configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="945d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="945d6-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="945d6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="945d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="945d6-107">*хконфигуратионблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="945d6-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="945d6-108">Обработайте с BLOB-объектом, который настраивает вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="945d6-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="945d6-109">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="945d6-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="945d6-110">Обработайте с BLOB-объектом ошибок, который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="945d6-110">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="945d6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="945d6-111">Return value</span></span>

<span data-ttu-id="945d6-112">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="945d6-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="945d6-113">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="945d6-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="945d6-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="945d6-114">Return code</span></span>                                                                                                         | <span data-ttu-id="945d6-115">Описание</span><span class="sxs-lookup"><span data-stu-id="945d6-115">Description</span></span>                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="945d6-116"><dt>**\_ \_ Недопустимая строка большого двоичного объекта нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-116"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="945d6-117">Строка не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="945d6-117">The string is not null-terminated.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="945d6-118"><dt>**\_BLOB-объект нмерр \_ не \_ инициализирован**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-118"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="945d6-119">Метод **CreateBlob** не был вызван.</span><span class="sxs-lookup"><span data-stu-id="945d6-119">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="945d6-120"><dt>**НМЕРР \_ Недопустимый \_ BLOB-объект**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-120"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="945d6-121">Объект, на который указывает, не является BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="945d6-121">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="945d6-122"><dt>**\_BLOB-объект верхнего уровня нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-122"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="945d6-123">Неправильный номер версии большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="945d6-123">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="945d6-124"><dt>**\_запись BLOB-объекта нмерр \_ \_ уже \_ существует**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-124"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="945d6-125">Запись BLOB-объекта уже существует.</span><span class="sxs-lookup"><span data-stu-id="945d6-125">A BLOB entry already exists.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="945d6-126"><dt>**\_запись BLOB-объекта нмерр \_ \_ \_ не \_ существует**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-126"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="945d6-127">Большой двоичный объект конфигурации, заданный параметром *хконфигуратионблоб* , не имеет записи, необходимой для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="945d6-127">The configuration BLOB specified by the *hConfigurationBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="945d6-128">Проверьте большой двоичный объект ошибки, возвращенный параметром *херрорблоб* , чтобы определить, какая запись не была найдена.</span><span class="sxs-lookup"><span data-stu-id="945d6-128">Look at the error BLOB returned by the *hErrorBlob* parameter to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="945d6-129"><dt>**\_спецификатор неоднозначных нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-129"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="945d6-130">BLOB-объект не имеет сведений о владельце или категории.</span><span class="sxs-lookup"><span data-stu-id="945d6-130">The BLOB lacks owner or category information.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="945d6-131"><dt>**\_ \_ \_ не найден владелец BLOB-объекта нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-131"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="945d6-132">Раздел владельца большого двоичного объекта не найден.</span><span class="sxs-lookup"><span data-stu-id="945d6-132">The Owner section of the BLOB was not found.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="945d6-133"><dt>**\_Категория BLOB-объектов нмерр \_ \_ не \_ найдена**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-133"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="945d6-134">Раздел категории большого двоичного объекта не найден.</span><span class="sxs-lookup"><span data-stu-id="945d6-134">The Category section of the BLOB was not found.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="945d6-135"><dt>**НМЕРР \_ неизвестная \_ Категория**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-135"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="945d6-136">Сведения о категории найдены, но не распознаны.</span><span class="sxs-lookup"><span data-stu-id="945d6-136">Category information was found but not understood.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="945d6-137"><dt>**НМЕРР \_ неизвестный \_ тег**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-137"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="945d6-138">Информация о теге найдена, но не распознана.</span><span class="sxs-lookup"><span data-stu-id="945d6-138">Tag information was found but not understood.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="945d6-139"><dt>**\_Ошибка преобразования BLOB-объекта нмерр \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-139"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="945d6-140">Большой двоичный объект поврежден.</span><span class="sxs-lookup"><span data-stu-id="945d6-140">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="945d6-141"><dt>**НМЕРР \_ Недопустимый \_ триггер**</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-141"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="945d6-142">Повреждена часть триггера большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="945d6-142">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="945d6-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="945d6-143">Remarks</span></span>

<span data-ttu-id="945d6-144">Этот метод необходимо применить для перезапуска НПП, который был запущен, остановлен, но не отключен.</span><span class="sxs-lookup"><span data-stu-id="945d6-144">You must apply this method to restart an NPP that has been started, stopped but not disconnected.</span></span>

<span data-ttu-id="945d6-145">BLOB-объект ошибки, возвращенный *херрорблоб* , содержит записи, которые сетевой монитор не удалось распознать или найти в большом двоичном объекте конфигурации, указанном в параметре *хконфигуратионблоб* .</span><span class="sxs-lookup"><span data-stu-id="945d6-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in the *hConfigurationBlob* parameter.</span></span> <span data-ttu-id="945d6-146">Возвращенный BLOB-объект ошибки содержит сведения об ошибке, которые приложение может использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="945d6-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="945d6-147">Например, если \_ запись BLOB-объекта нмерр \_ \_ \_ не \_ существует, запись, сетевой монитор не удалось найти, включается в возвращенный большой двоичный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="945d6-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="945d6-148">Требования</span><span class="sxs-lookup"><span data-stu-id="945d6-148">Requirements</span></span>



| <span data-ttu-id="945d6-149">Требование</span><span class="sxs-lookup"><span data-stu-id="945d6-149">Requirement</span></span> | <span data-ttu-id="945d6-150">Значение</span><span class="sxs-lookup"><span data-stu-id="945d6-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="945d6-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="945d6-151">Minimum supported client</span></span><br/> | <span data-ttu-id="945d6-152">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="945d6-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="945d6-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="945d6-153">Minimum supported server</span></span><br/> | <span data-ttu-id="945d6-154">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="945d6-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="945d6-155">Заголовок</span><span class="sxs-lookup"><span data-stu-id="945d6-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="945d6-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="945d6-157">DLL</span><span class="sxs-lookup"><span data-stu-id="945d6-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="945d6-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="945d6-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="945d6-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945d6-160">истатс</span><span class="sxs-lookup"><span data-stu-id="945d6-160">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="945d6-161">ИСТАТС:: Connect</span><span class="sxs-lookup"><span data-stu-id="945d6-161">ISTATS::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="945d6-162">сетевой монитор большие двоичные объекты</span><span class="sxs-lookup"><span data-stu-id="945d6-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




