---
title: Метод Ивмдрмсекурити Жетконтентенаблерсфорревокатионс (Вмдрмсдк. h)
description: Метод Жетконтентенаблерсфорревокатионс получает интерфейсы включения содержимого, которые обеспечивают возобновление компонентов на основе отозванных сертификатов.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Формат Windows Media, Жетконтентенаблерсфорревокатионс метод
- Жетконтентенаблерсфорревокатионс метод Windows Media Format, интерфейс Ивмдрмсекурити
- Интерфейс Ивмдрмсекурити Windows Media Format, метод Жетконтентенаблерсфорревокатионс
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648674"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a><span data-ttu-id="fd538-106">Метод Ивмдрмсекурити:: Жетконтентенаблерсфорревокатионс</span><span class="sxs-lookup"><span data-stu-id="fd538-106">IWMDRMSecurity::GetContentEnablersForRevocations method</span></span>

<span data-ttu-id="fd538-107">Метод **жетконтентенаблерсфорревокатионс** получает интерфейсы включения содержимого, которые обеспечивают возобновление компонентов на основе отозванных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="fd538-107">The **GetContentEnablersForRevocations** method retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd538-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd538-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="fd538-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd538-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd538-110">*ргпбцертс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd538-110">*rgpbCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd538-111">Массив сертификатов для получения содержимого созидателями.</span><span class="sxs-lookup"><span data-stu-id="fd538-111">Array of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="fd538-112">Число элементов в массиве должно быть задано параметром *кцертс*.</span><span class="sxs-lookup"><span data-stu-id="fd538-112">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="fd538-113">*ргпдвцертсизес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd538-113">*rgpdwCertSizes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd538-114">Массив, содержащий размеры сертификатов в массиве *ргпбцертс* .</span><span class="sxs-lookup"><span data-stu-id="fd538-114">Array containing the sizes of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="fd538-115">Число элементов в массиве должно быть задано параметром *кцертс*.</span><span class="sxs-lookup"><span data-stu-id="fd538-115">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="fd538-116">*ргпгуидцертс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd538-116">*rgpguidCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd538-117">Массив, содержащий типы сертификатов в массиве *ргпбцертс* .</span><span class="sxs-lookup"><span data-stu-id="fd538-117">Array containing the types of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="fd538-118">Число элементов в массиве должно быть задано параметром *кцертс*.</span><span class="sxs-lookup"><span data-stu-id="fd538-118">The number of elements in the array must be specified by *cCerts*.</span></span> <span data-ttu-id="fd538-119">Для каждого элемента массива используйте одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fd538-119">For each element of the array, use one of the following values.</span></span>



| <span data-ttu-id="fd538-120">Константа GUID</span><span class="sxs-lookup"><span data-stu-id="fd538-120">GUID constant</span></span>                 | <span data-ttu-id="fd538-121">Описание</span><span class="sxs-lookup"><span data-stu-id="fd538-121">Description</span></span>                                                    |
|-------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="fd538-122">\_приложение РЕВОКАТИОНТИПЕ \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="fd538-122">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="fd538-123">Указывает сертификат приложения.</span><span class="sxs-lookup"><span data-stu-id="fd538-123">Specifies an application certificate.</span></span>                          |
| <span data-ttu-id="fd538-124">\_устройство WMDRM ревокатионтипе \_</span><span class="sxs-lookup"><span data-stu-id="fd538-124">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="fd538-125">Указывает сертификат устройства.</span><span class="sxs-lookup"><span data-stu-id="fd538-125">Specifies a device certificate.</span></span>                                |
| <span data-ttu-id="fd538-126">\_КАРДЕА WMDRM ревокатионтипе \_</span><span class="sxs-lookup"><span data-stu-id="fd538-126">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="fd538-127">Указывает сертификат Windows Media DRM для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="fd538-127">Specifies a Windows Media DRM for Network Devices certificate.</span></span> |



 

</dd> <dt>

<span data-ttu-id="fd538-128">*кцертс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd538-128">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd538-129">Число сертификатов для получения содержимого созидателями.</span><span class="sxs-lookup"><span data-stu-id="fd538-129">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="fd538-130">Это число элементов в массиве *ргпбцертс* , массиве *ргпдвцертсизес* и массиве *ргпгуидцертс* .</span><span class="sxs-lookup"><span data-stu-id="fd538-130">This is the number of elements in the *rgpbCerts* array, the *rgpdwCertSizes* array, and the *rgpguidCerts* array.</span></span>

</dd> <dt>

<span data-ttu-id="fd538-131">*хресулсинт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd538-131">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd538-132">Возвращенное значение, полученное из операции, которая завершилась сбоем из-за отозванного сертификата.</span><span class="sxs-lookup"><span data-stu-id="fd538-132">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="fd538-133">Если вы не вызываете в ответ на вызов метода со сбоем, задайте для параметра значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fd538-133">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="fd538-134">*пргконтентенаблерс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fd538-134">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd538-135">Массив, который получает адреса только что созданных интерфейсов **имфконтентенаблер** .</span><span class="sxs-lookup"><span data-stu-id="fd538-135">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="fd538-136">Задайте значение **null** , чтобы получить количество созидателями содержимого в параметре *пкконтентенаблерс* .</span><span class="sxs-lookup"><span data-stu-id="fd538-136">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fd538-137">*пкконтентенаблерс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fd538-137">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd538-138">Число элементов в массиве *пргконтентенаблерс* .</span><span class="sxs-lookup"><span data-stu-id="fd538-138">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="fd538-139">Если *пргконтентенаблерс* имеет **значение NULL**, это значение устанавливается равным числу необходимых созидателями содержимого на выходе.</span><span class="sxs-lookup"><span data-stu-id="fd538-139">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd538-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd538-140">Return value</span></span>

<span data-ttu-id="fd538-141">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fd538-141">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fd538-142">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fd538-142">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fd538-143">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fd538-143">Return code</span></span>                                                                          | <span data-ttu-id="fd538-144">Описание</span><span class="sxs-lookup"><span data-stu-id="fd538-144">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fd538-145"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fd538-145"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fd538-146">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="fd538-146">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd538-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd538-147">Remarks</span></span>

<span data-ttu-id="fd538-148">Если вы используете интерфейс **имфконтентенаблер** для обновления отозванных компонентов, необходимо уточнить процесс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="fd538-148">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="fd538-149">Это уточнение необходимо, так как процесс обновления отправляет данные с клиентского компьютера на веб-сайт корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="fd538-149">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="fd538-150">При вызове **имфконтентенаблер:: аутоматиценабле** программа включения содержимого запускает браузер по умолчанию с адресом службы обновления на веб-сайте Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="fd538-150">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="fd538-151">Уникальный идентификатор, идентифицирующий отозванный компонент, передается в службу обновления.</span><span class="sxs-lookup"><span data-stu-id="fd538-151">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="fd538-152">Затем служба перенаправляет браузер на веб-страницу, с которой пользователь может загрузить и установить новую версию отозванного компонента.</span><span class="sxs-lookup"><span data-stu-id="fd538-152">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd538-153">Требования</span><span class="sxs-lookup"><span data-stu-id="fd538-153">Requirements</span></span>



| <span data-ttu-id="fd538-154">Требование</span><span class="sxs-lookup"><span data-stu-id="fd538-154">Requirement</span></span> | <span data-ttu-id="fd538-155">Значение</span><span class="sxs-lookup"><span data-stu-id="fd538-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd538-156">Header</span><span class="sxs-lookup"><span data-stu-id="fd538-156">Header</span></span><br/>  | <dl> <span data-ttu-id="fd538-157"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd538-157"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd538-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd538-158">Library</span></span><br/> | <dl> <span data-ttu-id="fd538-159"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd538-159"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd538-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd538-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd538-161">**Автоматизированный отзыв и продление компонентов**</span><span class="sxs-lookup"><span data-stu-id="fd538-161">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="fd538-162">**Интерфейс Ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="fd538-162">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





