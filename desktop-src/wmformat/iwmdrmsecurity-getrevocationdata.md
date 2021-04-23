---
title: Метод Ивмдрмсекурити Жетревокатиондата (Вмдрмсдк. h)
description: Метод Жетревокатиондата извлекает список отзыва сертификатов из локального хранилища.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Формат Windows Media, Жетревокатиондата метод
- Жетревокатиондата метод Windows Media Format, интерфейс Ивмдрмсекурити
- Интерфейс Ивмдрмсекурити Windows Media Format, метод Жетревокатиондата
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665309"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a><span data-ttu-id="b0654-106">Метод Ивмдрмсекурити:: Жетревокатиондата</span><span class="sxs-lookup"><span data-stu-id="b0654-106">IWMDRMSecurity::GetRevocationData method</span></span>

<span data-ttu-id="b0654-107">Метод **жетревокатиондата** извлекает список отзыва сертификатов из локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="b0654-107">The **GetRevocationData** method retrieves a certificate revocation list from the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0654-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0654-108">Syntax</span></span>


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="b0654-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0654-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0654-110">*f \_ гуидревокатионтипе* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="b0654-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0654-111">Идентификатор GUID, определяющий тип получаемого списка отзыва.</span><span class="sxs-lookup"><span data-stu-id="b0654-111">GUID identifying the type of revocation list to retrieve.</span></span> <span data-ttu-id="b0654-112">Используйте одну из констант в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b0654-112">Use one of the constants in the following table.</span></span>



| <span data-ttu-id="b0654-113">Константа GUID</span><span class="sxs-lookup"><span data-stu-id="b0654-113">GUID constant</span></span>                 | <span data-ttu-id="b0654-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b0654-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b0654-115">\_приложение РЕВОКАТИОНТИПЕ \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="b0654-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="b0654-116">Указывает список отзыва сертификатов приложения.</span><span class="sxs-lookup"><span data-stu-id="b0654-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="b0654-117">\_устройство WMDRM ревокатионтипе \_</span><span class="sxs-lookup"><span data-stu-id="b0654-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="b0654-118">Указывает список отзыва сертификатов устройств.</span><span class="sxs-lookup"><span data-stu-id="b0654-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="b0654-119">\_КАРДЕА WMDRM ревокатионтипе \_</span><span class="sxs-lookup"><span data-stu-id="b0654-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="b0654-120">Указывает список отзыва сертификатов Windows Media DRM для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="b0654-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b0654-121">*f \_ пбкрл* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b0654-121">*f\_pbCRL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0654-122">Буфер, который получает список отзыва.</span><span class="sxs-lookup"><span data-stu-id="b0654-122">Buffer that receives the revocation list.</span></span> <span data-ttu-id="b0654-123">Задайте **значение NULL** , чтобы получить требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="b0654-123">Set to **NULL** to get the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="b0654-124">*f \_ пкбкрл* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b0654-124">*f\_pcbCRL* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0654-125">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="b0654-125">Size of the buffer in bytes.</span></span> <span data-ttu-id="b0654-126">Если *f \_ Пбкрл* имеет **значение NULL**, для этого параметра задается требуемый размер буфера в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b0654-126">If *f\_pbCRL* is **NULL**, this value is set to the required buffer size on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0654-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0654-127">Return value</span></span>

<span data-ttu-id="b0654-128">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b0654-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b0654-129">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b0654-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b0654-130">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b0654-130">Return code</span></span>                                                                          | <span data-ttu-id="b0654-131">Описание</span><span class="sxs-lookup"><span data-stu-id="b0654-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b0654-132"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b0654-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b0654-133">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="b0654-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b0654-134">Требования</span><span class="sxs-lookup"><span data-stu-id="b0654-134">Requirements</span></span>



| <span data-ttu-id="b0654-135">Требование</span><span class="sxs-lookup"><span data-stu-id="b0654-135">Requirement</span></span> | <span data-ttu-id="b0654-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b0654-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0654-137">Header</span><span class="sxs-lookup"><span data-stu-id="b0654-137">Header</span></span><br/>  | <dl> <span data-ttu-id="b0654-138"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0654-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0654-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0654-139">Library</span></span><br/> | <dl> <span data-ttu-id="b0654-140"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0654-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0654-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0654-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0654-142">**Автоматизированный отзыв и продление компонентов**</span><span class="sxs-lookup"><span data-stu-id="b0654-142">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="b0654-143">**жетревокатиондатаверсион**</span><span class="sxs-lookup"><span data-stu-id="b0654-143">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="b0654-144">**Интерфейс Ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="b0654-144">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="b0654-145">**сетревокатиондата**</span><span class="sxs-lookup"><span data-stu-id="b0654-145">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





