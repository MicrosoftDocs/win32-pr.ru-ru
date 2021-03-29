---
title: Метод Ивмдрмпровидер CreateObject (Вмдрмсдк. h)
description: Метод CreateObject извлекает указатель на указанный интерфейс, создавая реализующий объект при необходимости.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Формат метода CreateObject Windows Media Format
- Метод CreateObject формат Windows Media Format, интерфейс Ивмдрмпровидер
- Интерфейс Ивмдрмпровидер интерфейса Windows Media Format, метод CreateObject
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648013"
---
# <a name="iwmdrmprovidercreateobject-method"></a><span data-ttu-id="cd906-106">Метод Ивмдрмпровидер:: CreateObject</span><span class="sxs-lookup"><span data-stu-id="cd906-106">IWMDRMProvider::CreateObject method</span></span>

<span data-ttu-id="cd906-107">Метод **CreateObject** извлекает указатель на указанный интерфейс, создавая реализующий объект при необходимости.</span><span class="sxs-lookup"><span data-stu-id="cd906-107">The **CreateObject** method retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd906-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd906-108">Syntax</span></span>


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="cd906-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd906-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd906-110">*riid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd906-110">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd906-111">Идентификатор создаваемого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cd906-111">Identifier of the interface to be created.</span></span> <span data-ttu-id="cd906-112">Задайте одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cd906-112">Set to one of the following values.</span></span>

-   <span data-ttu-id="cd906-113">IID \_ ивмдрмлиценсеманажемент</span><span class="sxs-lookup"><span data-stu-id="cd906-113">IID\_IWMDRMLicenseManagement</span></span>
-   <span data-ttu-id="cd906-114">IID \_ ивмдрмлиценсекуери</span><span class="sxs-lookup"><span data-stu-id="cd906-114">IID\_IWMDRMLicenseQuery</span></span>
-   <span data-ttu-id="cd906-115">IID \_ ивмдрмнетрецеивер</span><span class="sxs-lookup"><span data-stu-id="cd906-115">IID\_IWMDRMNetReceiver</span></span>
-   <span data-ttu-id="cd906-116">IID \_ ивмдрмнеттрансмиттер</span><span class="sxs-lookup"><span data-stu-id="cd906-116">IID\_IWMDRMNetTransmitter</span></span>
-   <span data-ttu-id="cd906-117">IID \_ ивмдрмсекурити</span><span class="sxs-lookup"><span data-stu-id="cd906-117">IID\_IWMDRMSecurity</span></span>

</dd> <dt>

<span data-ttu-id="cd906-118">*ппвобжект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cd906-118">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd906-119">Адрес указателя, получающего адрес запрошенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cd906-119">Address of a pointer that receives the address of the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd906-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd906-120">Return value</span></span>

<span data-ttu-id="cd906-121">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cd906-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cd906-122">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cd906-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cd906-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cd906-123">Return code</span></span>                                                                          | <span data-ttu-id="cd906-124">Описание</span><span class="sxs-lookup"><span data-stu-id="cd906-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cd906-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cd906-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cd906-126">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="cd906-126">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cd906-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd906-127">Remarks</span></span>

<span data-ttu-id="cd906-128">Нет.</span><span class="sxs-lookup"><span data-stu-id="cd906-128">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd906-129">Требования</span><span class="sxs-lookup"><span data-stu-id="cd906-129">Requirements</span></span>



| <span data-ttu-id="cd906-130">Требование</span><span class="sxs-lookup"><span data-stu-id="cd906-130">Requirement</span></span> | <span data-ttu-id="cd906-131">Значение</span><span class="sxs-lookup"><span data-stu-id="cd906-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd906-132">Header</span><span class="sxs-lookup"><span data-stu-id="cd906-132">Header</span></span><br/>  | <dl> <span data-ttu-id="cd906-133"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd906-133"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd906-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd906-134">Library</span></span><br/> | <dl> <span data-ttu-id="cd906-135"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd906-135"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd906-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd906-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd906-137">**Интерфейс Ивмдрмпровидер**</span><span class="sxs-lookup"><span data-stu-id="cd906-137">**IWMDRMProvider Interface**</span></span>](iwmdrmprovider.md)
</dt> <dt>

[<span data-ttu-id="cd906-138">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="cd906-138">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="cd906-139">**Интерфейс Ивмдрмлиценсекуери**</span><span class="sxs-lookup"><span data-stu-id="cd906-139">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="cd906-140">**Интерфейс Ивмдрмнетрецеивер**</span><span class="sxs-lookup"><span data-stu-id="cd906-140">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="cd906-141">**Интерфейс Ивмдрмнеттрансмиттер**</span><span class="sxs-lookup"><span data-stu-id="cd906-141">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> <dt>

[<span data-ttu-id="cd906-142">**Интерфейс Ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="cd906-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





