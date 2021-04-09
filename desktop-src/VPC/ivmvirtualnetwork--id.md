---
title: Метод _ID Ивмвиртуалнетворк (Впккоминтерфацес. h)
description: Извлекает внутренний идентификатор виртуальной сети.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- _ID метод Virtual PC
- _ID метод Virtual PC, интерфейс Ивмвиртуалнетворк
- Ивмвиртуалнетворк интерфейс Virtual PC, метод _ID
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b79c4d6f4dfa778fee156b1bfa09ab39b8bedf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071923"
---
# <a name="ivmvirtualnetwork_id-method"></a><span data-ttu-id="2d13d-106">Метод Ивмвиртуалнетворк:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="2d13d-106">IVMVirtualNetwork::\_ID method</span></span>

<span data-ttu-id="2d13d-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2d13d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2d13d-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2d13d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2d13d-109">Извлекает внутренний идентификатор виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d13d-109">Retrieves the internal identifier of the virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d13d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d13d-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a><span data-ttu-id="2d13d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d13d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d13d-112">*virtualNetworkID* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2d13d-112">*virtualNetworkID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d13d-113">Идентификатор виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2d13d-113">The virtual network identifier.</span></span> <span data-ttu-id="2d13d-114">Идентификатор виртуальной сети (NAT) общей сети — 01010101010101010101010101010101.</span><span class="sxs-lookup"><span data-stu-id="2d13d-114">The identifier for the Shared Networking (NAT) virtual network is 01010101010101010101010101010101.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d13d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d13d-115">Return value</span></span>

<span data-ttu-id="2d13d-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2d13d-116">This method can return one of these values.</span></span>



| <span data-ttu-id="2d13d-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="2d13d-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="2d13d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="2d13d-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2d13d-119"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2d13d-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2d13d-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2d13d-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="2d13d-121"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="2d13d-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2d13d-122">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2d13d-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="2d13d-123"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2d13d-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2d13d-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2d13d-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2d13d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d13d-125">Remarks</span></span>

<span data-ttu-id="2d13d-126">Это свойство не может использоваться в языках скриптов.</span><span class="sxs-lookup"><span data-stu-id="2d13d-126">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d13d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2d13d-127">Requirements</span></span>



| <span data-ttu-id="2d13d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2d13d-128">Requirement</span></span> | <span data-ttu-id="2d13d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2d13d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d13d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d13d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2d13d-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2d13d-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d13d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d13d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2d13d-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2d13d-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2d13d-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2d13d-134">End of client support</span></span><br/>    | <span data-ttu-id="2d13d-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d13d-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2d13d-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="2d13d-136">Product</span></span><br/>                  | <span data-ttu-id="2d13d-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2d13d-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2d13d-138">Header</span><span class="sxs-lookup"><span data-stu-id="2d13d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d13d-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d13d-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2d13d-140">IID</span><span class="sxs-lookup"><span data-stu-id="2d13d-140">IID</span></span><br/>                      | <span data-ttu-id="2d13d-141">IID \_ ивмвиртуалнетворк определен как 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="2d13d-141">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2d13d-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d13d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d13d-143">**ивмвиртуалнетворк**</span><span class="sxs-lookup"><span data-stu-id="2d13d-143">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

