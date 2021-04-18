---
title: Метод Ивмдрмсекурити Жетревокатиондатаверсион (Вмдрмсдк. h)
description: Метод Жетревокатиондатаверсион извлекает номер версии списка отзыва сертификатов в локальном хранилище.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Формат Windows Media, Жетревокатиондатаверсион метод
- Жетревокатиондатаверсион метод Windows Media Format, интерфейс Ивмдрмсекурити
- Интерфейс Ивмдрмсекурити Windows Media Format, метод Жетревокатиондатаверсион
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665308"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a><span data-ttu-id="3e544-106">Метод Ивмдрмсекурити:: Жетревокатиондатаверсион</span><span class="sxs-lookup"><span data-stu-id="3e544-106">IWMDRMSecurity::GetRevocationDataVersion method</span></span>

<span data-ttu-id="3e544-107">Метод **жетревокатиондатаверсион** извлекает номер версии списка отзыва сертификатов в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="3e544-107">The **GetRevocationDataVersion** method retrieves the version number of a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e544-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e544-108">Syntax</span></span>


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a><span data-ttu-id="3e544-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e544-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e544-110">*f \_ гуидревокатионтипе* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3e544-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e544-111">GUID, указывающий тип списка отзыва.</span><span class="sxs-lookup"><span data-stu-id="3e544-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="3e544-112">Задайте одну из констант в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3e544-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="3e544-113">Константа GUID</span><span class="sxs-lookup"><span data-stu-id="3e544-113">GUID constant</span></span>                 | <span data-ttu-id="3e544-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3e544-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3e544-115">\_приложение РЕВОКАТИОНТИПЕ \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="3e544-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="3e544-116">Указывает список отзыва сертификатов приложения.</span><span class="sxs-lookup"><span data-stu-id="3e544-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="3e544-117">\_устройство WMDRM ревокатионтипе \_</span><span class="sxs-lookup"><span data-stu-id="3e544-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="3e544-118">Указывает список отзыва сертификатов устройств.</span><span class="sxs-lookup"><span data-stu-id="3e544-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="3e544-119">\_КАРДЕА WMDRM ревокатионтипе \_</span><span class="sxs-lookup"><span data-stu-id="3e544-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="3e544-120">Указывает список отзыва сертификатов Windows Media DRM для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="3e544-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3e544-121">*f \_ пдвкрлверсион* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3e544-121">*f\_pdwCRLVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e544-122">Переменная, которая получает номер версии.</span><span class="sxs-lookup"><span data-stu-id="3e544-122">Variable that receives the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e544-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e544-123">Return value</span></span>

<span data-ttu-id="3e544-124">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3e544-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3e544-125">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3e544-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3e544-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3e544-126">Return code</span></span>                                                                          | <span data-ttu-id="3e544-127">Описание</span><span class="sxs-lookup"><span data-stu-id="3e544-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3e544-128"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3e544-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3e544-129">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="3e544-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3e544-130">Требования</span><span class="sxs-lookup"><span data-stu-id="3e544-130">Requirements</span></span>



| <span data-ttu-id="3e544-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3e544-131">Requirement</span></span> | <span data-ttu-id="3e544-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3e544-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e544-133">Header</span><span class="sxs-lookup"><span data-stu-id="3e544-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3e544-134"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e544-134"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e544-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3e544-135">Library</span></span><br/> | <dl> <span data-ttu-id="3e544-136"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e544-136"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e544-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e544-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e544-138">**Автоматизированный отзыв и продление компонентов**</span><span class="sxs-lookup"><span data-stu-id="3e544-138">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="3e544-139">**жетревокатиондата**</span><span class="sxs-lookup"><span data-stu-id="3e544-139">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="3e544-140">**Интерфейс Ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="3e544-140">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="3e544-141">**сетревокатиондата**</span><span class="sxs-lookup"><span data-stu-id="3e544-141">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





