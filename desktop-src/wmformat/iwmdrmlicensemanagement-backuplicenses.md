---
title: Метод Ивмдрмлиценсеманажемент Баккуплиценсес (Вмдрмсдк. h)
description: Метод Баккуплиценсес создает резервную копию лицензий в локальном хранилище лицензий.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Формат Windows Media, Баккуплиценсес метод
- Баккуплиценсес метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Баккуплиценсес
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717899"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a><span data-ttu-id="73c2b-106">Метод Ивмдрмлиценсеманажемент:: Баккуплиценсес</span><span class="sxs-lookup"><span data-stu-id="73c2b-106">IWMDRMLicenseManagement::BackupLicenses method</span></span>

<span data-ttu-id="73c2b-107">Метод **баккуплиценсес** создает резервную копию лицензий в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="73c2b-107">The **BackupLicenses** method creates a backup of the licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c2b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73c2b-108">Syntax</span></span>


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="73c2b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="73c2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73c2b-110">*бстрбаккупдиректори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73c2b-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c2b-111">UNC-путь к расположению, в которое будут создаваться резервные копии лицензий.</span><span class="sxs-lookup"><span data-stu-id="73c2b-111">UNC path of the location to which the licenses will be backed up.</span></span>

</dd> <dt>

<span data-ttu-id="73c2b-112">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73c2b-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c2b-113">Флаги, указывающие используемые параметры резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="73c2b-113">Flags specifying the backup options to use.</span></span> <span data-ttu-id="73c2b-114">Единственным поддерживаемым флагом является \_ \_ Перезапись WMDRM Backup, которая настраивает метод для перезаписи существующих файлов резервных копий в каталоге.</span><span class="sxs-lookup"><span data-stu-id="73c2b-114">The only flag currently supported is WMDRM\_BACKUP\_OVERWRITE, which configures the method to overwrite any existing backup files in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="73c2b-115">*ппункканцелатионкукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="73c2b-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73c2b-116">Указатель, получающий указатель на интерфейс **IUnknown** объекта, определяющий этот асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="73c2b-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="73c2b-117">Этот указатель интерфейса можно использовать для отмены асинхронного вызова путем вызова метода [**ивмдрмевентженератор:: канцеласинкоператион**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="73c2b-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73c2b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73c2b-118">Return value</span></span>

<span data-ttu-id="73c2b-119">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="73c2b-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="73c2b-120">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="73c2b-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="73c2b-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="73c2b-121">Return code</span></span>                                                                          | <span data-ttu-id="73c2b-122">Описание</span><span class="sxs-lookup"><span data-stu-id="73c2b-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="73c2b-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="73c2b-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="73c2b-124">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="73c2b-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73c2b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73c2b-125">Remarks</span></span>

<span data-ttu-id="73c2b-126">Этот метод выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="73c2b-126">This method executes asynchronously.</span></span> <span data-ttu-id="73c2b-127">Он возвращает сразу после вызова, а затем создает ряд событий **мевмдрмлиценсебаккуппрогресс** , за которыми следует событие **мевмдрмлиценсебаккупкомплетед** после завершения обработки.</span><span class="sxs-lookup"><span data-stu-id="73c2b-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseBackupProgress** events followed by an **MEWMDRMLicenseBackupCompleted** event when processing is complete.</span></span> <span data-ttu-id="73c2b-128">Значение каждого из событий **мевмдрмлиценсебаккуппрогресс** , полученных путем вызова **Имфмедиаевент:: GetValue** , является указателем **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="73c2b-128">The value of each of the **MEWMDRMLicenseBackupProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="73c2b-129">Чтобы получить экземпляр интерфейса [**ивмдрмлиценсебаккупресторестатус**](iwmdrmlicensebackuprestorestatus.md) , можно вызвать метод **QueryInterface** полученного интерфейса **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="73c2b-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="73c2b-130">Дополнительные сведения об использовании асинхронных методов расширенных API-интерфейсов клиента DRM Windows Media см. [в разделе Использование модели событий Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="73c2b-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="73c2b-131">Не все лицензии разрешено архивировать.</span><span class="sxs-lookup"><span data-stu-id="73c2b-131">Not all licenses are permitted to be backed up.</span></span> <span data-ttu-id="73c2b-132">Этот метод создает резервные копии только тех лицензий, которые допускают ее.</span><span class="sxs-lookup"><span data-stu-id="73c2b-132">This method only backs up licenses that allow it.</span></span>

## <a name="requirements"></a><span data-ttu-id="73c2b-133">Требования</span><span class="sxs-lookup"><span data-stu-id="73c2b-133">Requirements</span></span>



| <span data-ttu-id="73c2b-134">Требование</span><span class="sxs-lookup"><span data-stu-id="73c2b-134">Requirement</span></span> | <span data-ttu-id="73c2b-135">Значение</span><span class="sxs-lookup"><span data-stu-id="73c2b-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73c2b-136">Header</span><span class="sxs-lookup"><span data-stu-id="73c2b-136">Header</span></span><br/>  | <dl> <span data-ttu-id="73c2b-137"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c2b-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="73c2b-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73c2b-138">Library</span></span><br/> | <dl> <span data-ttu-id="73c2b-139"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73c2b-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73c2b-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73c2b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c2b-141">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="73c2b-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





