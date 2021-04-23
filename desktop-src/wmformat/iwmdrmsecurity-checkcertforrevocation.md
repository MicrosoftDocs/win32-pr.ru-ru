---
title: Метод Ивмдрмсекурити Чеккцертфорревокатион (Вмдрмсдк. h)
description: Метод Чеккцертфорревокатион определяет, был ли отозван сертификат.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Формат Windows Media, Чеккцертфорревокатион метод
- Чеккцертфорревокатион метод Windows Media Format, интерфейс Ивмдрмсекурити
- Интерфейс Ивмдрмсекурити Windows Media Format, метод Чеккцертфорревокатион
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648012"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a><span data-ttu-id="6c5f8-106">Метод Ивмдрмсекурити:: Чеккцертфорревокатион</span><span class="sxs-lookup"><span data-stu-id="6c5f8-106">IWMDRMSecurity::CheckCertForRevocation method</span></span>

<span data-ttu-id="6c5f8-107">Метод **чеккцертфорревокатион** определяет, был ли отозван сертификат.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-107">The **CheckCertForRevocation** method determines whether a certificate has been revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c5f8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c5f8-108">Syntax</span></span>


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a><span data-ttu-id="6c5f8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c5f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c5f8-110">*ргуидревокатионлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c5f8-110">*rguidRevocationList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5f8-111">Идентификатор GUID, определяющий используемый список отзыва.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-111">GUID identifying the revocation list to use.</span></span> <span data-ttu-id="6c5f8-112">Задайте одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="6c5f8-113">Константа GUID</span><span class="sxs-lookup"><span data-stu-id="6c5f8-113">GUID constant</span></span>                 | <span data-ttu-id="6c5f8-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6c5f8-114">Description</span></span>                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5f8-115">\_приложение РЕВОКАТИОНТИПЕ \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="6c5f8-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="6c5f8-116">Указывает список отзыва сертификатов приложения.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-116">Specifies the application certificate revocation list.</span></span>                                     |
| <span data-ttu-id="6c5f8-117">\_устройство WMDRM ревокатионтипе \_</span><span class="sxs-lookup"><span data-stu-id="6c5f8-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="6c5f8-118">Указывает список отзыва сертификатов устройств.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-118">Specifies the device certificate revocation list.</span></span>                                          |
| <span data-ttu-id="6c5f8-119">\_КАРДЕА WMDRM ревокатионтипе \_</span><span class="sxs-lookup"><span data-stu-id="6c5f8-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="6c5f8-120">Указывает список отзыва сертификатов Windows Media DRM для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-120">Specifies the Microsoft Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6c5f8-121">*пбцерт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c5f8-121">*pbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5f8-122">Буфер, содержащий сертификат для поиска.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-122">Buffer containing the certificate to look up.</span></span>

</dd> <dt>

<span data-ttu-id="6c5f8-123">*кбцерт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c5f8-123">*cbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5f8-124">Размер буфера *пбцерт* в байтах.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-124">Size of the buffer *pbCert*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6c5f8-125">*фревокед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6c5f8-125">*fRevoked* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5f8-126">В поле выходные данные указывает, имеется ли сертификат в списке отзыва.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-126">On output, indicates whether the certificate is present in the revocation list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c5f8-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c5f8-127">Return value</span></span>

<span data-ttu-id="6c5f8-128">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6c5f8-129">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6c5f8-130">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6c5f8-130">Return code</span></span>                                                                          | <span data-ttu-id="6c5f8-131">Описание</span><span class="sxs-lookup"><span data-stu-id="6c5f8-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6c5f8-132"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5f8-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6c5f8-133">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="6c5f8-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6c5f8-134">Требования</span><span class="sxs-lookup"><span data-stu-id="6c5f8-134">Requirements</span></span>



| <span data-ttu-id="6c5f8-135">Требование</span><span class="sxs-lookup"><span data-stu-id="6c5f8-135">Requirement</span></span> | <span data-ttu-id="6c5f8-136">Значение</span><span class="sxs-lookup"><span data-stu-id="6c5f8-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5f8-137">Header</span><span class="sxs-lookup"><span data-stu-id="6c5f8-137">Header</span></span><br/>  | <dl> <span data-ttu-id="6c5f8-138"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c5f8-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c5f8-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6c5f8-139">Library</span></span><br/> | <dl> <span data-ttu-id="6c5f8-140"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c5f8-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5f8-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c5f8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5f8-142">**Интерфейс Ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="6c5f8-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





