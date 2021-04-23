---
description: Метод Configure отправляет сведения о конфигурации, используемые для записи.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Метод Иделайдкконфигуре (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496989"
---
# <a name="idelaydcconfigure-method"></a><span data-ttu-id="87f16-103">Метод Иделайдк:: Configure</span><span class="sxs-lookup"><span data-stu-id="87f16-103">IDelaydC::Configure method</span></span>

<span data-ttu-id="87f16-104">Метод **Configure** отправляет сведения о конфигурации, используемые для записи.</span><span class="sxs-lookup"><span data-stu-id="87f16-104">The **Configure** method submits configuration information used for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="87f16-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87f16-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="87f16-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87f16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f16-107">*хконфигуратионблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87f16-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f16-108">Обработайте с BLOB-объектом, который содержит сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="87f16-108">Handle to the BLOB that contains the configuration information.</span></span>

</dd> <dt>

<span data-ttu-id="87f16-109">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="87f16-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87f16-110">Обработайте с BLOB-объектом ошибок, который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="87f16-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="87f16-111">Сведения о содержимом большого двоичного объекта ошибки см. в подразделе "Примечания" этого раздела.</span><span class="sxs-lookup"><span data-stu-id="87f16-111">For information about the contents of an error BLOB, see the Remarks section in this topic .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f16-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87f16-112">Return value</span></span>

<span data-ttu-id="87f16-113">Если этот метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="87f16-113">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="87f16-114">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="87f16-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="87f16-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="87f16-115">Return code</span></span>                                                                                                      | <span data-ttu-id="87f16-116">Описание</span><span class="sxs-lookup"><span data-stu-id="87f16-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87f16-117"><dt>**НМЕРР \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="87f16-117"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                  | <span data-ttu-id="87f16-118">НПП сообщает, что сеанс отслеживания запущен.</span><span class="sxs-lookup"><span data-stu-id="87f16-118">The NPP reports that the capture session has started.</span></span><br/>                          |
| <dl> <span data-ttu-id="87f16-119"><dt>**\_ \_ фиксированный диск нмерр не является \_ локальным \_**</dt></span><span class="sxs-lookup"><span data-stu-id="87f16-119"><dt>**NMERR\_DISK\_NOT\_LOCAL\_FIXED**</dt></span></span> </dl>    |                                                                                           |
| <dl> <span data-ttu-id="87f16-120"><dt>**НМЕРР \_ \_ не удалось \_ создать \_ память**</dt></span><span class="sxs-lookup"><span data-stu-id="87f16-120"><dt>**NMERR\_COULD\_NOT\_CREATE\_MEMORY**</dt></span></span> </dl> |                                                                                           |
| <dl> <span data-ttu-id="87f16-121"><dt>**НМЕРР \_ недостаточно \_ \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="87f16-121"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>            | <span data-ttu-id="87f16-122">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="87f16-122">No memory was available.</span></span> <span data-ttu-id="87f16-123">Завершите работу Windows, чтобы освободить ресурсы.</span><span class="sxs-lookup"><span data-stu-id="87f16-123">Shut down windows to free up resources.</span></span><br/>               |
| <dl> <span data-ttu-id="87f16-124"><dt>**НМЕРР \_ Недопустимый \_ параметр**</dt></span><span class="sxs-lookup"><span data-stu-id="87f16-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="87f16-125">Большой двоичный объект конфигурации, заданный параметром Хконфигуратион, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="87f16-125">The configuration BLOB specified by the hConfiguration parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87f16-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87f16-126">Remarks</span></span>

<span data-ttu-id="87f16-127">Этот метод необходимо применить для перезапуска НПП, который был запущен, остановлен, но не отключен.</span><span class="sxs-lookup"><span data-stu-id="87f16-127">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="87f16-128">BLOB-объект ошибки, возвращенный *херрорблоб* , содержит записи, которые сетевой монитор не удалось распознать или найти в большом двоичном объекте конфигурации, указанном в *хконфигуратионблоб*.</span><span class="sxs-lookup"><span data-stu-id="87f16-128">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="87f16-129">Возвращенный BLOB-объект ошибки содержит сведения об ошибке, которые приложение может использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="87f16-129">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="87f16-130">Например, если \_ запись BLOB-объекта нмерр \_ \_ \_ не \_ существует, запись, сетевой монитор не удалось найти, включается в возвращенный большой двоичный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="87f16-130">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="87f16-131">Требования</span><span class="sxs-lookup"><span data-stu-id="87f16-131">Requirements</span></span>



| <span data-ttu-id="87f16-132">Требование</span><span class="sxs-lookup"><span data-stu-id="87f16-132">Requirement</span></span> | <span data-ttu-id="87f16-133">Значение</span><span class="sxs-lookup"><span data-stu-id="87f16-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f16-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87f16-134">Minimum supported client</span></span><br/> | <span data-ttu-id="87f16-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87f16-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="87f16-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87f16-136">Minimum supported server</span></span><br/> | <span data-ttu-id="87f16-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87f16-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="87f16-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="87f16-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="87f16-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="87f16-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="87f16-140">DLL</span><span class="sxs-lookup"><span data-stu-id="87f16-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87f16-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87f16-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f16-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87f16-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f16-143">иделайдк</span><span class="sxs-lookup"><span data-stu-id="87f16-143">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="87f16-144">Иделайдк:: Connect</span><span class="sxs-lookup"><span data-stu-id="87f16-144">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="87f16-145">Иделайдк:: Start</span><span class="sxs-lookup"><span data-stu-id="87f16-145">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="87f16-146">Иделайдк:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="87f16-146">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




