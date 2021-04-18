---
title: Ивмдрмдевице Жетдевицецертификате, метод
description: Метод Жетдевицецертификате извлекает сертификат устройства.
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- Метод Жетдевицецертификате Windows Media диспетчер устройств
- Метод Жетдевицецертификате Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Жетдевицецертификате
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ceecca32f2455d73ca1dce76a4f8a17613a1ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694422"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a><span data-ttu-id="eb4fc-106">Метод Ивмдрмдевице:: Жетдевицецертификате</span><span class="sxs-lookup"><span data-stu-id="eb4fc-106">IWMDRMDevice::GetDeviceCertificate method</span></span>

<span data-ttu-id="eb4fc-107">Метод **жетдевицецертификате** извлекает сертификат устройства.</span><span class="sxs-lookup"><span data-stu-id="eb4fc-107">The **GetDeviceCertificate** method retrieves the device certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4fc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb4fc-108">Syntax</span></span>


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a><span data-ttu-id="eb4fc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb4fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb4fc-110">*пбстрдевцерт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eb4fc-110">*pbstrDevCert* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4fc-111">Указатель на **строку BSTR** , содержащую полученный сертификат устройства.</span><span class="sxs-lookup"><span data-stu-id="eb4fc-111">Pointer to a **BSTR** containing the retrieved device certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb4fc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb4fc-112">Return value</span></span>

<span data-ttu-id="eb4fc-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="eb4fc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="eb4fc-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="eb4fc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="eb4fc-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="eb4fc-115">Return code</span></span>                                                                          | <span data-ttu-id="eb4fc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="eb4fc-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="eb4fc-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4fc-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="eb4fc-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="eb4fc-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="eb4fc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="eb4fc-119">Requirements</span></span>



| <span data-ttu-id="eb4fc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="eb4fc-120">Requirement</span></span> | <span data-ttu-id="eb4fc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="eb4fc-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4fc-122">Header</span><span class="sxs-lookup"><span data-stu-id="eb4fc-122">Header</span></span><br/>  | <dl> <span data-ttu-id="eb4fc-123"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb4fc-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="eb4fc-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eb4fc-124">Library</span></span><br/> | <dl> <span data-ttu-id="eb4fc-125"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb4fc-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb4fc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb4fc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb4fc-127">**Интерфейс Ивмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="eb4fc-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





