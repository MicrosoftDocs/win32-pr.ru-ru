---
title: Имсрдпдривеколлектион Рескандривес, метод
description: Обновляет список объектов в коллекции. | Имсрдпдривеколлектион Рескандривес, метод
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рескандривес
- Службы удаленных рабочих столов метода Рескандривес, интерфейс Имсрдпдривеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдривеколлектион, метод Рескандривес
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684840"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a><span data-ttu-id="771c1-107">Метод Имсрдпдривеколлектион:: Рескандривес</span><span class="sxs-lookup"><span data-stu-id="771c1-107">IMsRdpDriveCollection::RescanDrives method</span></span>

<span data-ttu-id="771c1-108">Обновляет список объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="771c1-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="771c1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="771c1-109">Syntax</span></span>


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="771c1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="771c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="771c1-111">*вбулдинредир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="771c1-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771c1-112">Состояние перенаправления по умолчанию, которое будет применяться к вновь обнаруженным устройствам или дискам.</span><span class="sxs-lookup"><span data-stu-id="771c1-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="771c1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="771c1-113">Return value</span></span>

<span data-ttu-id="771c1-114">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="771c1-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="771c1-115">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="771c1-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="771c1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="771c1-116">Requirements</span></span>



| <span data-ttu-id="771c1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="771c1-117">Requirement</span></span> | <span data-ttu-id="771c1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="771c1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="771c1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="771c1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="771c1-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="771c1-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="771c1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="771c1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="771c1-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="771c1-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="771c1-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="771c1-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="771c1-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="771c1-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="771c1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="771c1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="771c1-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="771c1-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="771c1-127">IID</span><span class="sxs-lookup"><span data-stu-id="771c1-127">IID</span></span><br/>                      | <span data-ttu-id="771c1-128">IID \_ имсрдпдривеколлектион определен как 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="771c1-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="771c1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="771c1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771c1-130">**имсрдпдривеколлектион**</span><span class="sxs-lookup"><span data-stu-id="771c1-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





