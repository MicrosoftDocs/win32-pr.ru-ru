---
description: Метод Configure отправляет сведения о конфигурации для записи.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'Метод ИЕСП:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662175"
---
# <a name="iespconfigure-method"></a><span data-ttu-id="17948-103">Метод ИЕСП:: Configure</span><span class="sxs-lookup"><span data-stu-id="17948-103">IESP::Configure method</span></span>

<span data-ttu-id="17948-104">Метод **Configure** отправляет сведения о конфигурации для записи.</span><span class="sxs-lookup"><span data-stu-id="17948-104">The **Configure** method submits configuration information for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="17948-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17948-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="17948-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17948-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17948-107">*хконфигуратионблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17948-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17948-108">Обработайте с BLOB-объектом, который настраивает вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="17948-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="17948-109">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="17948-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17948-110">Обработайте с BLOB-объектом ошибок, который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="17948-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="17948-111">Сведения о содержимом большого двоичного объекта ошибки см. в подразделе "Примечания" этого раздела.</span><span class="sxs-lookup"><span data-stu-id="17948-111">For information about the contents of an error BLOB, see the Remarks section in this topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17948-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17948-112">Return value</span></span>

<span data-ttu-id="17948-113">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="17948-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="17948-114">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="17948-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="17948-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="17948-115">Return code</span></span>                                                                                                         | <span data-ttu-id="17948-116">Описание</span><span class="sxs-lookup"><span data-stu-id="17948-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17948-117"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-117"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>                | <span data-ttu-id="17948-118">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="17948-118">The NPP is not connected to the network.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="17948-119"><dt>**НМЕРР \_ не \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>                      | <span data-ttu-id="17948-120">НПП подключается к сети, но не с методом [ИЕСП:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="17948-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="17948-121"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-121"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                     | <span data-ttu-id="17948-122">НПП сообщает, что сеанс отслеживания запущен.</span><span class="sxs-lookup"><span data-stu-id="17948-122">The NPP reports that the capture session has started.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="17948-123"><dt>**НМЕРР \_ Недопустимый \_ триггер**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-123"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="17948-124">Часть триггера BLOB-объекта конфигурации повреждена.</span><span class="sxs-lookup"><span data-stu-id="17948-124">The trigger portion of the configuration BLOB is corrupt.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="17948-125"><dt>**\_запись BLOB-объекта нмерр \_ \_ \_ не \_ существует**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-125"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="17948-126">В большом двоичном объекте конфигурации, указанном параметром *хконфигуратионблоб* , отсутствует запись, необходимая для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="17948-126">The configuration BLOB specified by *hConfigurationBlob* is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="17948-127">Посмотрите на большой двоичный объект Error, возвращенный *херрорблоб* , чтобы определить, какая запись не найдена.</span><span class="sxs-lookup"><span data-stu-id="17948-127">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="17948-128"><dt>**\_Ошибка преобразования BLOB-объекта нмерр \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-128"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="17948-129">Большой двоичный объект поврежден.</span><span class="sxs-lookup"><span data-stu-id="17948-129">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="17948-130"><dt>**\_BLOB-объект нмерр \_ не \_ инициализирован**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-130"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="17948-131">Метод **CreateBlob** не был вызван.</span><span class="sxs-lookup"><span data-stu-id="17948-131">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="17948-132"><dt>**НМЕРР \_ Недопустимый \_ BLOB-объект**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-132"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="17948-133">Объект, на который указывает, не является BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="17948-133">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="17948-134"><dt>**\_ \_ Недопустимая строка большого двоичного объекта нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-134"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="17948-135">Строка не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="17948-135">The string is not null-terminated.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="17948-136"><dt>**\_BLOB-объект верхнего уровня нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-136"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="17948-137">Неправильный номер версии большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="17948-137">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="17948-138"><dt>**НМЕРР \_ недостаточно \_ \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-138"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="17948-139">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="17948-139">No memory was available.</span></span> <span data-ttu-id="17948-140">Завершите работу Windows, чтобы освободить ресурсы.</span><span class="sxs-lookup"><span data-stu-id="17948-140">Shut down windows to free up resources.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="17948-141"><dt>**\_время ожидания нмерр**</dt></span><span class="sxs-lookup"><span data-stu-id="17948-141"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="17948-142">Истекло время ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="17948-142">The request has timed out.</span></span><br/>                                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="17948-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17948-143">Remarks</span></span>

<span data-ttu-id="17948-144">Этот метод необходимо применить для перезапуска НПП, который был запущен и остановлен, но не был отключен.</span><span class="sxs-lookup"><span data-stu-id="17948-144">You must apply this method to restart an NPP that has been started and stopped, but not disconnected.</span></span>

<span data-ttu-id="17948-145">BLOB-объект ошибки, возвращенный параметром *херрорблоб* , содержит записи, которые сетевой монитор не удалось распознать или найти в большом двоичном объекте конфигурации, указанном в *хконфигуратионблоб*.</span><span class="sxs-lookup"><span data-stu-id="17948-145">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="17948-146">Возвращенный BLOB-объект ошибки содержит сведения об ошибке, которые приложение может использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="17948-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="17948-147">Например, если \_ запись BLOB-объекта нмерр \_ \_ \_ не \_ существует, запись, сетевой монитор не удалось найти, включается в возвращенный большой двоичный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="17948-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="17948-148">Требования</span><span class="sxs-lookup"><span data-stu-id="17948-148">Requirements</span></span>



| <span data-ttu-id="17948-149">Требование</span><span class="sxs-lookup"><span data-stu-id="17948-149">Requirement</span></span> | <span data-ttu-id="17948-150">Значение</span><span class="sxs-lookup"><span data-stu-id="17948-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17948-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17948-151">Minimum supported client</span></span><br/> | <span data-ttu-id="17948-152">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="17948-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="17948-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17948-153">Minimum supported server</span></span><br/> | <span data-ttu-id="17948-154">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="17948-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="17948-155">Заголовок</span><span class="sxs-lookup"><span data-stu-id="17948-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="17948-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="17948-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="17948-157">DLL</span><span class="sxs-lookup"><span data-stu-id="17948-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17948-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17948-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

 




