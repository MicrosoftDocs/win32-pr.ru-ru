---
title: Метод Ивмдрмсекурити Сетревокатиондата (Вмдрмсдк. h)
description: Метод Сетревокатиондата задает список отзыва сертификатов в локальном хранилище.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- Формат Windows Media, Сетревокатиондата метод
- Сетревокатиондата метод Windows Media Format, интерфейс Ивмдрмсекурити
- Интерфейс Ивмдрмсекурити Windows Media Format, метод Сетревокатиондата
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665307"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a><span data-ttu-id="75a4c-106">Метод Ивмдрмсекурити:: Сетревокатиондата</span><span class="sxs-lookup"><span data-stu-id="75a4c-106">IWMDRMSecurity::SetRevocationData method</span></span>

<span data-ttu-id="75a4c-107">Метод **сетревокатиондата** задает список отзыва сертификатов в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="75a4c-107">The **SetRevocationData** method sets a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="75a4c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75a4c-108">Syntax</span></span>


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="75a4c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="75a4c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75a4c-110">*f \_ гуидревокатионтипе* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="75a4c-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a4c-111">GUID, указывающий тип списка отзыва.</span><span class="sxs-lookup"><span data-stu-id="75a4c-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="75a4c-112">Задайте одну из констант в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="75a4c-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="75a4c-113">Константа GUID</span><span class="sxs-lookup"><span data-stu-id="75a4c-113">GUID constant</span></span>                 | <span data-ttu-id="75a4c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="75a4c-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75a4c-115">\_приложение РЕВОКАТИОНТИПЕ \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="75a4c-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="75a4c-116">Указывает список отзыва сертификатов приложения.</span><span class="sxs-lookup"><span data-stu-id="75a4c-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="75a4c-117">\_устройство WMDRM ревокатионтипе \_</span><span class="sxs-lookup"><span data-stu-id="75a4c-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="75a4c-118">Указывает список отзыва сертификатов устройств.</span><span class="sxs-lookup"><span data-stu-id="75a4c-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="75a4c-119">\_КАРДЕА WMDRM ревокатионтипе \_</span><span class="sxs-lookup"><span data-stu-id="75a4c-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="75a4c-120">Указывает список отзыва сертификатов Windows Media DRM для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="75a4c-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="75a4c-121">*f \_ пбкрл* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="75a4c-121">*f\_pbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a4c-122">Буфер, содержащий список отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="75a4c-122">Buffer containing the certificate revocation list.</span></span>

</dd> <dt>

<span data-ttu-id="75a4c-123">*f \_ кбкрл* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="75a4c-123">*f\_cbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a4c-124">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="75a4c-124">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75a4c-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75a4c-125">Return value</span></span>

<span data-ttu-id="75a4c-126">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="75a4c-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="75a4c-127">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="75a4c-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="75a4c-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="75a4c-128">Return code</span></span>                                                                          | <span data-ttu-id="75a4c-129">Описание</span><span class="sxs-lookup"><span data-stu-id="75a4c-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="75a4c-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="75a4c-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="75a4c-131">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="75a4c-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="75a4c-132">Требования</span><span class="sxs-lookup"><span data-stu-id="75a4c-132">Requirements</span></span>



| <span data-ttu-id="75a4c-133">Требование</span><span class="sxs-lookup"><span data-stu-id="75a4c-133">Requirement</span></span> | <span data-ttu-id="75a4c-134">Значение</span><span class="sxs-lookup"><span data-stu-id="75a4c-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75a4c-135">Header</span><span class="sxs-lookup"><span data-stu-id="75a4c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="75a4c-136"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="75a4c-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="75a4c-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="75a4c-137">Library</span></span><br/> | <dl> <span data-ttu-id="75a4c-138"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75a4c-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75a4c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75a4c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75a4c-140">**жетревокатиондата**</span><span class="sxs-lookup"><span data-stu-id="75a4c-140">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="75a4c-141">**жетревокатиондатаверсион**</span><span class="sxs-lookup"><span data-stu-id="75a4c-141">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="75a4c-142">**Интерфейс Ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="75a4c-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





