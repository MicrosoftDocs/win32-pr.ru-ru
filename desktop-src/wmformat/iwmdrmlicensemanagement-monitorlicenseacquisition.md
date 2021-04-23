---
title: Метод Ивмдрмлиценсеманажемент Мониторлиценсеаккуиситион (Вмдрмсдк. h)
description: Метод Мониторлиценсеаккуиситион инициирует мониторинг процесса получения лицензии.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Формат Windows Media, Мониторлиценсеаккуиситион метод
- Мониторлиценсеаккуиситион метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Мониторлиценсеаккуиситион
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25171d36a9d360f7c8eb77211c580c4f7676618f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105714084"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a><span data-ttu-id="8098e-106">Метод Ивмдрмлиценсеманажемент:: Мониторлиценсеаккуиситион</span><span class="sxs-lookup"><span data-stu-id="8098e-106">IWMDRMLicenseManagement::MonitorLicenseAcquisition method</span></span>

<span data-ttu-id="8098e-107">Метод **мониторлиценсеаккуиситион** инициирует мониторинг процесса получения лицензии.</span><span class="sxs-lookup"><span data-stu-id="8098e-107">The **MonitorLicenseAcquisition** method initiates monitoring for a license acquisition process.</span></span>

## <a name="syntax"></a><span data-ttu-id="8098e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8098e-108">Syntax</span></span>


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="8098e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8098e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8098e-110">*бстркид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8098e-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8098e-111">Идентификатор ключа (ребенок) получаемой лицензии.</span><span class="sxs-lookup"><span data-stu-id="8098e-111">Key ID (KID) of the license being acquired.</span></span>

</dd> <dt>

<span data-ttu-id="8098e-112">*бстрхеадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8098e-112">*bstrHeader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8098e-113">Заголовок содержимого, который использовался при вызове метода [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="8098e-113">Content header that was used in the call to the [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="8098e-114">*бстрактионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8098e-114">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8098e-115">Строка, содержащая действия, запрошенные при вызове метода **AcquireLicense** .</span><span class="sxs-lookup"><span data-stu-id="8098e-115">String containing the actions requested in the call to the **AcquireLicense** method.</span></span>

</dd> <dt>

<span data-ttu-id="8098e-116">*ппункканцелатионкукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8098e-116">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8098e-117">Указатель, получающий указатель на интерфейс **IUnknown** объекта, определяющий этот асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="8098e-117">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="8098e-118">Этот указатель интерфейса можно использовать для отмены асинхронного вызова путем вызова метода [**ивмдрмевентженератор:: канцеласинкоператион**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="8098e-118">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8098e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8098e-119">Return value</span></span>

<span data-ttu-id="8098e-120">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8098e-120">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8098e-121">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8098e-121">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8098e-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8098e-122">Return code</span></span>                                                                          | <span data-ttu-id="8098e-123">Описание</span><span class="sxs-lookup"><span data-stu-id="8098e-123">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8098e-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8098e-124"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8098e-125">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="8098e-125">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8098e-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8098e-126">Remarks</span></span>

<span data-ttu-id="8098e-127">Нет.</span><span class="sxs-lookup"><span data-stu-id="8098e-127">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="8098e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8098e-128">Requirements</span></span>



| <span data-ttu-id="8098e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8098e-129">Requirement</span></span> | <span data-ttu-id="8098e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8098e-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8098e-131">Header</span><span class="sxs-lookup"><span data-stu-id="8098e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8098e-132"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="8098e-132"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8098e-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8098e-133">Library</span></span><br/> | <dl> <span data-ttu-id="8098e-134"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8098e-134"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8098e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8098e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8098e-136">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="8098e-136">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





