---
title: Метод Ивмдрмлиценсеманажемент Ресторелиценсес (Вмдрмсдк. h)
description: Метод Ресторелиценсес восстанавливает лицензии из резервной копии лицензий, созданной путем вызова метода Баккуплиценсес.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Формат Windows Media, Ресторелиценсес метод
- Ресторелиценсес метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Ресторелиценсес
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717901"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a><span data-ttu-id="5c403-106">Метод Ивмдрмлиценсеманажемент:: Ресторелиценсес</span><span class="sxs-lookup"><span data-stu-id="5c403-106">IWMDRMLicenseManagement::RestoreLicenses method</span></span>

<span data-ttu-id="5c403-107">Метод **ресторелиценсес** восстанавливает лицензии из резервной копии лицензий, созданной путем вызова метода [**баккуплиценсес**](iwmdrmlicensemanagement-backuplicenses.md) .</span><span class="sxs-lookup"><span data-stu-id="5c403-107">The **RestoreLicenses** method restores licenses from a license backup that was created by calling the [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c403-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c403-108">Syntax</span></span>


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="5c403-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c403-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c403-110">*бстрбаккупдиректори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c403-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c403-111">UNC-путь к расположению, из которого будут восстановлены лицензии.</span><span class="sxs-lookup"><span data-stu-id="5c403-111">UNC path of the location from which the licenses will be restored.</span></span>

</dd> <dt>

<span data-ttu-id="5c403-112">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c403-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c403-113">Флаги, указывающие используемые параметры восстановления.</span><span class="sxs-lookup"><span data-stu-id="5c403-113">Flags specifying the restore options to use.</span></span> <span data-ttu-id="5c403-114">В настоящее время поддерживается только флаг \_ \_ индивидуализируйте для восстановления WMDRM, который настраивает метод для выполнения индивидуализации в процессе восстановления, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="5c403-114">The only flag currently supported is WMDRM\_RESTORE\_INDIVIDUALIZE, which configures the method to perform individualization as part of the restoration, if required.</span></span>

</dd> <dt>

<span data-ttu-id="5c403-115">*ппункканцелатионкукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5c403-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c403-116">Указатель, получающий указатель на интерфейс **IUnknown** объекта, определяющий этот асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="5c403-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="5c403-117">Этот указатель интерфейса можно использовать для отмены асинхронного вызова путем вызова метода [**ивмдрмевентженератор:: канцеласинкоператион**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="5c403-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c403-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c403-118">Return value</span></span>

<span data-ttu-id="5c403-119">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5c403-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5c403-120">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5c403-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5c403-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5c403-121">Return code</span></span>                                                                          | <span data-ttu-id="5c403-122">Описание</span><span class="sxs-lookup"><span data-stu-id="5c403-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5c403-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5c403-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5c403-124">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="5c403-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c403-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c403-125">Remarks</span></span>

<span data-ttu-id="5c403-126">Этот метод выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="5c403-126">This method executes asynchronously.</span></span> <span data-ttu-id="5c403-127">Он возвращает сразу после вызова, а затем создает ряд событий **мевмдрмлиценсересторепрогресс** , за которыми следует событие **мевмдрмлиценсересторекомплетед** после завершения обработки.</span><span class="sxs-lookup"><span data-stu-id="5c403-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseRestoreProgress** events followed by an **MEWMDRMLicenseRestoreCompleted** event when processing is complete.</span></span> <span data-ttu-id="5c403-128">Значение каждого из событий **мевмдрмлиценсересторепрогресс** , полученных путем вызова **Имфмедиаевент:: GetValue** , является указателем **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="5c403-128">The value of each of the **MEWMDRMLicenseRestoreProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="5c403-129">Чтобы получить экземпляр интерфейса [**ивмдрмлиценсебаккупресторестатус**](iwmdrmlicensebackuprestorestatus.md) , можно вызвать метод **QueryInterface** полученного интерфейса **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="5c403-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="5c403-130">Дополнительные сведения об использовании асинхронных методов расширенных API-интерфейсов клиента DRM Windows Media см. [в разделе Использование модели событий Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="5c403-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="5c403-131">Резервное копирование может выполняться с локального компьютера или с другого компьютера.</span><span class="sxs-lookup"><span data-stu-id="5c403-131">The backup can be from the local machine or from a different machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c403-132">Требования</span><span class="sxs-lookup"><span data-stu-id="5c403-132">Requirements</span></span>



| <span data-ttu-id="5c403-133">Требование</span><span class="sxs-lookup"><span data-stu-id="5c403-133">Requirement</span></span> | <span data-ttu-id="5c403-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5c403-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c403-135">Header</span><span class="sxs-lookup"><span data-stu-id="5c403-135">Header</span></span><br/>  | <dl> <span data-ttu-id="5c403-136"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c403-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c403-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5c403-137">Library</span></span><br/> | <dl> <span data-ttu-id="5c403-138"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c403-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c403-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c403-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c403-140">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="5c403-140">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





