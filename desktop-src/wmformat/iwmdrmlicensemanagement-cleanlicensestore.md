---
title: Метод Ивмдрмлиценсеманажемент Клеанлиценсесторе (Вмдрмсдк. h)
description: Метод Клеанлиценсесторе удаляет непригодные для использования лицензии из временного хранилища лицензий и дефрагментации локального хранилища лицензий для повышения производительности.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Формат Windows Media, Клеанлиценсесторе метод
- Клеанлиценсесторе метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Клеанлиценсесторе
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717824"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a><span data-ttu-id="849bc-106">Метод Ивмдрмлиценсеманажемент:: Клеанлиценсесторе</span><span class="sxs-lookup"><span data-stu-id="849bc-106">IWMDRMLicenseManagement::CleanLicenseStore method</span></span>

<span data-ttu-id="849bc-107">Метод **клеанлиценсесторе** удаляет непригодные для использования лицензии из временного хранилища лицензий и дефрагментации локального хранилища лицензий для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="849bc-107">The **CleanLicenseStore** method removes unusable licenses from the temporary license store and defragments the local license store to improve performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="849bc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="849bc-108">Syntax</span></span>


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="849bc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="849bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="849bc-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="849bc-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="849bc-111">Флаги, указывающие параметры очистки хранилища лицензий для использования.</span><span class="sxs-lookup"><span data-stu-id="849bc-111">Flags specifying the license store cleaning options to use.</span></span> <span data-ttu-id="849bc-112">Задайте одну из констант в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="849bc-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="849bc-113">Константа</span><span class="sxs-lookup"><span data-stu-id="849bc-113">Constant</span></span>                            | <span data-ttu-id="849bc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="849bc-114">Description</span></span>                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="849bc-115">\_Синхронизация WMDRM \_ Clean \_ Store \_</span><span class="sxs-lookup"><span data-stu-id="849bc-115">WMDRM\_CLEAN\_LICENSE\_STORE\_SYNC</span></span>  | <span data-ttu-id="849bc-116">Операция очистки будет выполнена синхронно.</span><span class="sxs-lookup"><span data-stu-id="849bc-116">The clean operation will be performed synchronously.</span></span> <span data-ttu-id="849bc-117">Этот метод не будет возвращать значение до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="849bc-117">This method will not return until the operation is complete.</span></span>                                                              |
| <span data-ttu-id="849bc-118">\_ \_ хранилище лицензий очистки \_ WMDRM \_ Async</span><span class="sxs-lookup"><span data-stu-id="849bc-118">WMDRM\_CLEAN\_LICENSE\_STORE\_ASYNC</span></span> | <span data-ttu-id="849bc-119">Операция очистки будет выполнена асинхронно.</span><span class="sxs-lookup"><span data-stu-id="849bc-119">The clean operation will be performed asynchronously.</span></span> <span data-ttu-id="849bc-120">Этот метод будет возвращать немедленно.</span><span class="sxs-lookup"><span data-stu-id="849bc-120">This method will return immediately.</span></span> <span data-ttu-id="849bc-121">После завершения операции будет отправлено событие мультимедиа Мелиценсестореклеанед.</span><span class="sxs-lookup"><span data-stu-id="849bc-121">When the operation is complete, the media event MELicenseStoreCleaned will be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="849bc-122">*ппункканцелатионкукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="849bc-122">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="849bc-123">Указатель, получающий указатель на интерфейс **IUnknown** объекта, определяющий этот асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="849bc-123">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="849bc-124">Этот указатель интерфейса можно использовать для отмены асинхронного вызова путем вызова метода [**ивмдрмевентженератор:: канцеласинкоператион**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="849bc-124">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="849bc-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="849bc-125">Return value</span></span>

<span data-ttu-id="849bc-126">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="849bc-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="849bc-127">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="849bc-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="849bc-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="849bc-128">Return code</span></span>                                                                                            | <span data-ttu-id="849bc-129">Описание</span><span class="sxs-lookup"><span data-stu-id="849bc-129">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="849bc-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="849bc-130"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="849bc-131">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="849bc-131">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="849bc-132"><dt>**DRM \_ E \_ лиценсенотфаунд**</dt></span><span class="sxs-lookup"><span data-stu-id="849bc-132"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="849bc-133">На клиентском компьютере нет временного хранилища лицензий.</span><span class="sxs-lookup"><span data-stu-id="849bc-133">There is no temporary license store on the client computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="849bc-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="849bc-134">Remarks</span></span>

<span data-ttu-id="849bc-135">Этот метод выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="849bc-135">This method executes asynchronously.</span></span> <span data-ttu-id="849bc-136">Он возвращает сразу после вызова, а затем создает событие **мевмдрмлиценсестореклеанед** после завершения обработки.</span><span class="sxs-lookup"><span data-stu-id="849bc-136">It returns immediately after being called and then generates an **MEWMDRMLicenseStoreCleaned** event when processing is complete.</span></span>

<span data-ttu-id="849bc-137">Дополнительные сведения об использовании асинхронных методов расширенных API-интерфейсов клиента DRM Windows Media см. [в разделе Использование модели событий Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="849bc-137">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="849bc-138">Требования</span><span class="sxs-lookup"><span data-stu-id="849bc-138">Requirements</span></span>



| <span data-ttu-id="849bc-139">Требование</span><span class="sxs-lookup"><span data-stu-id="849bc-139">Requirement</span></span> | <span data-ttu-id="849bc-140">Значение</span><span class="sxs-lookup"><span data-stu-id="849bc-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="849bc-141">Header</span><span class="sxs-lookup"><span data-stu-id="849bc-141">Header</span></span><br/>  | <dl> <span data-ttu-id="849bc-142"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="849bc-142"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="849bc-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="849bc-143">Library</span></span><br/> | <dl> <span data-ttu-id="849bc-144"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="849bc-144"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="849bc-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="849bc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="849bc-146">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="849bc-146">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





