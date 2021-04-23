---
title: Метод Ивмдрмлиценсекуери Сетактионалловедкуерипарамс (Вмдрмсдк. h)
description: Метод Сетактионалловедкуерипарамс задает сведения о конкретной среде для более точных результатов запроса при использовании метода Куеряктионалловед.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- Формат Windows Media, Сетактионалловедкуерипарамс метод
- Сетактионалловедкуерипарамс метод Windows Media Format, интерфейс Ивмдрмлиценсекуери
- Интерфейс Ивмдрмлиценсекуери Windows Media Format, метод Сетактионалловедкуерипарамс
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675052"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a><span data-ttu-id="b4032-106">Метод Ивмдрмлиценсекуери:: Сетактионалловедкуерипарамс</span><span class="sxs-lookup"><span data-stu-id="b4032-106">IWMDRMLicenseQuery::SetActionAllowedQueryParams method</span></span>

<span data-ttu-id="b4032-107">Метод **сетактионалловедкуерипарамс** задает сведения о конкретной среде для более точных результатов запроса при использовании метода [**куеряктионалловед**](iwmdrmlicensequery-queryactionallowed.md) .</span><span class="sxs-lookup"><span data-stu-id="b4032-107">The **SetActionAllowedQueryParams** method sets environment-specific information for more accurate query results when using the [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4032-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4032-108">Syntax</span></span>


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a><span data-ttu-id="b4032-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4032-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4032-110">*фисмф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4032-110">*fIsMF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4032-111">Указывает, будет ли содержимое визуализировано с помощью объектов пакета SDK Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b4032-111">Specifies whether the content will be rendered by using the objects of the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="b4032-112">**Значение false** указывает, что отрисовка осуществляется объектами пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="b4032-112">**FALSE** indicates rendering by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="b4032-113">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b4032-113">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b4032-114">*дваппсеклевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4032-114">*dwAppSecLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4032-115">Уровень безопасности приложения запроса.</span><span class="sxs-lookup"><span data-stu-id="b4032-115">Security level of the querying application.</span></span> <span data-ttu-id="b4032-116">Это значение важно только в том случае, если будут использоваться объекты пакета SDK Windows Media Format, в этом случае *фисмф* должно быть установлено в **значение false**.</span><span class="sxs-lookup"><span data-stu-id="b4032-116">This value is only important if the objects of the Windows Media Format SDK will be used, in which case *fIsMF* should be set to **FALSE**.</span></span> <span data-ttu-id="b4032-117">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b4032-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b4032-118">*фхассериалнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4032-118">*fHasSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4032-119">Указывает, имеет ли целевое устройство для операции копирования серийный номер.</span><span class="sxs-lookup"><span data-stu-id="b4032-119">Specifies whether the target device for a copy operation has a serial number.</span></span> <span data-ttu-id="b4032-120">Этот параметр является необязательным и применяется только к запросам операций копирования.</span><span class="sxs-lookup"><span data-stu-id="b4032-120">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> <dt>

<span data-ttu-id="b4032-121">*бстрдевицецерт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4032-121">*bstrDeviceCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4032-122">Сертификат устройства целевого устройства при использовании Windows Media DRM для переносных устройств.</span><span class="sxs-lookup"><span data-stu-id="b4032-122">Device certificate of the target device when using Windows Media DRM for Portable Devices.</span></span> <span data-ttu-id="b4032-123">Этот параметр является необязательным и применяется только к запросам операций копирования.</span><span class="sxs-lookup"><span data-stu-id="b4032-123">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4032-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4032-124">Return value</span></span>

<span data-ttu-id="b4032-125">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b4032-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b4032-126">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b4032-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b4032-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b4032-127">Return code</span></span>                                                                          | <span data-ttu-id="b4032-128">Описание</span><span class="sxs-lookup"><span data-stu-id="b4032-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b4032-129"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b4032-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b4032-130">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="b4032-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4032-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4032-131">Remarks</span></span>

<span data-ttu-id="b4032-132">Нет.</span><span class="sxs-lookup"><span data-stu-id="b4032-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4032-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b4032-133">Requirements</span></span>



| <span data-ttu-id="b4032-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b4032-134">Requirement</span></span> | <span data-ttu-id="b4032-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b4032-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4032-136">Header</span><span class="sxs-lookup"><span data-stu-id="b4032-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b4032-137"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4032-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4032-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4032-138">Library</span></span><br/> | <dl> <span data-ttu-id="b4032-139"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4032-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4032-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4032-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4032-141">**Интерфейс Ивмдрмлиценсекуери**</span><span class="sxs-lookup"><span data-stu-id="b4032-141">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="b4032-142">**Запрос подробных сведений о правах**</span><span class="sxs-lookup"><span data-stu-id="b4032-142">**Querying for Detailed Rights Information**</span></span>](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





