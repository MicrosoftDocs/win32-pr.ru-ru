---
title: Метод Ивмдрмсекурити Перформсекуритюпдате (Вмдрмсдк. h)
description: Метод Перформсекуритюпдате инициирует обновление безопасности для подсистемы DRM на локальном компьютере.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Формат Windows Media, Перформсекуритюпдате метод
- Перформсекуритюпдате метод Windows Media Format, интерфейс Ивмдрмсекурити
- Интерфейс Ивмдрмсекурити Windows Media Format, метод Перформсекуритюпдате
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704169"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a><span data-ttu-id="4213a-106">Ивмдрмсекурити: метод:P Ерформсекуритюпдате</span><span class="sxs-lookup"><span data-stu-id="4213a-106">IWMDRMSecurity::PerformSecurityUpdate method</span></span>

<span data-ttu-id="4213a-107">Метод **перформсекуритюпдате** инициирует обновление безопасности для подсистемы DRM на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4213a-107">The **PerformSecurityUpdate** method initiates a security update to the DRM subsystem on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4213a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4213a-108">Syntax</span></span>


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="4213a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4213a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4213a-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4213a-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4213a-111">Параметр обновления выражается в одном из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="4213a-111">Update option expressed as one of the following flags.</span></span>



| <span data-ttu-id="4213a-112">Flag</span><span class="sxs-lookup"><span data-stu-id="4213a-112">Flag</span></span>                                          | <span data-ttu-id="4213a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4213a-113">Description</span></span>                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4213a-114">безопасность WMDRM. \_ \_ выполнение \_ индив</span><span class="sxs-lookup"><span data-stu-id="4213a-114">WMDRM\_SECURITY\_PERFORM\_INDIV</span></span>               | <span data-ttu-id="4213a-115">Вызывает индивидуальную установку компонента DRM, только если версия клиента устарела.</span><span class="sxs-lookup"><span data-stu-id="4213a-115">Causes the DRM component to be individualized only if the version of the client is out of date.</span></span> |
| <span data-ttu-id="4213a-116">\_Безопасность WMDRM \_ выполнить \_ Обновление отзыва \_</span><span class="sxs-lookup"><span data-stu-id="4213a-116">WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH</span></span> | <span data-ttu-id="4213a-117">Приводит к обновлению списков отзыва на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="4213a-117">Causes the revocation lists on the client computer to be updated.</span></span>                               |
| <span data-ttu-id="4213a-118">безопасность WMDRM. \_ \_ выполнение \_ принудительного \_ индив</span><span class="sxs-lookup"><span data-stu-id="4213a-118">WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV</span></span>        | <span data-ttu-id="4213a-119">Приводит к тому, что компонент DRM будет индивидуальным, даже если версия клиента не устарела.</span><span class="sxs-lookup"><span data-stu-id="4213a-119">Causes the DRM component to be individualized even if the version of the client is up to date.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4213a-120">*ппункканцелатионкукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4213a-120">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4213a-121">Адрес переменной, которая получает указатель на объект, который можно использовать для отмены этой операции.</span><span class="sxs-lookup"><span data-stu-id="4213a-121">Address of a variable that receives a pointer to an object that can be used to cancel this operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4213a-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4213a-122">Return value</span></span>

<span data-ttu-id="4213a-123">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4213a-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4213a-124">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4213a-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4213a-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4213a-125">Return code</span></span>                                                                          | <span data-ttu-id="4213a-126">Описание</span><span class="sxs-lookup"><span data-stu-id="4213a-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4213a-127"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4213a-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4213a-128">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4213a-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4213a-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4213a-129">Remarks</span></span>

<span data-ttu-id="4213a-130">Этот метод выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="4213a-130">This method executes asynchronously.</span></span> <span data-ttu-id="4213a-131">Он возвращает сразу после вызова, а затем создает события в зависимости от флага, установленного в параметре *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="4213a-131">It returns immediately after being called and then generates events depending on the flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="4213a-132">Для индивидуальной установки (флаг, заданный для \_ безопасности WMDRM \_ выполнение \_ индив или WMDRM \_ Security \_ выполнить \_ Force \_ индив) создается ряд событий **мевмдрминдивидуализатионпрогресс** , за которыми следует событие **мевмдрминдивидуализатионкомплетед** по завершении обработки.</span><span class="sxs-lookup"><span data-stu-id="4213a-132">For individualization (flag set to WMDRM\_SECURITY\_PERFORM\_INDIV or WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV), a series of **MEWMDRMIndividualizationProgress** events is generated followed by an **MEWMDRMIndividualizationCompleted** event when processing is complete.</span></span> <span data-ttu-id="4213a-133">Значение каждого из событий **мевмдрминдивидуализатионпрогресс** , полученных путем вызова **Имфмедиаевент:: GetValue** , является указателем **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="4213a-133">The value of each of the **MEWMDRMIndividualizationProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="4213a-134">Чтобы получить экземпляр интерфейса [**ивмдрминдивидуализатионстатус**](iwmdrmindividualizationstatus.md) , можно вызвать метод **QueryInterface** полученного интерфейса **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="4213a-134">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span>

<span data-ttu-id="4213a-135">Для обновления списков отзыва (для флага, установленного для \_ безопасности WMDRM \_ выполнить \_ \_ Обновление отзыва) создается событие **мевмдрмревокатиондовнлоадкомплетед** после завершения обработки.</span><span class="sxs-lookup"><span data-stu-id="4213a-135">For refreshing the revocation lists (flag set to WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH), an **MEWMDRMREvocationDownloadCompleted** event is generated when processing is complete.</span></span>

> [!Note]  
> <span data-ttu-id="4213a-136">Когда **перформсекуритюпдате** завершает индивидуальную работу, единственными существующими объектами, которые будут отражать новое отдельное состояние, являются те, которые наследуют от **ивмдрмсекурити**.</span><span class="sxs-lookup"><span data-stu-id="4213a-136">When **PerformSecurityUpdate** completes individualization, the only existing objects that will reflect the new individualized state are those that inherit from **IWMDRMSecurity**.</span></span> <span data-ttu-id="4213a-137">Все остальные существующие объекты не будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="4213a-137">All other existing objects will not be updated.</span></span> <span data-ttu-id="4213a-138">Необходимо освободить и повторно создать все другие объекты, чтобы они отражали новое отдельное состояние.</span><span class="sxs-lookup"><span data-stu-id="4213a-138">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

 

<span data-ttu-id="4213a-139">Дополнительные сведения об использовании асинхронных методов расширенных API-интерфейсов клиента DRM Windows Media см. [в разделе Использование модели событий Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="4213a-139">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4213a-140">Требования</span><span class="sxs-lookup"><span data-stu-id="4213a-140">Requirements</span></span>



| <span data-ttu-id="4213a-141">Требование</span><span class="sxs-lookup"><span data-stu-id="4213a-141">Requirement</span></span> | <span data-ttu-id="4213a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="4213a-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4213a-143">Header</span><span class="sxs-lookup"><span data-stu-id="4213a-143">Header</span></span><br/>  | <dl> <span data-ttu-id="4213a-144"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="4213a-144"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="4213a-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4213a-145">Library</span></span><br/> | <dl> <span data-ttu-id="4213a-146"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4213a-146"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4213a-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4213a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4213a-148">**Автоматизированный отзыв и продление компонентов**</span><span class="sxs-lookup"><span data-stu-id="4213a-148">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="4213a-149">**Пример индивидуализации DRM**</span><span class="sxs-lookup"><span data-stu-id="4213a-149">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="4213a-150">**Интерфейс Ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="4213a-150">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="4213a-151">**Выполнение индивидуальной управления цифровыми правами**</span><span class="sxs-lookup"><span data-stu-id="4213a-151">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> </dl>

 

 





