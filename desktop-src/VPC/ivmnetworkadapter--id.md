---
title: Метод _ID Ивмнетворкадаптер (Впккоминтерфацес. h)
description: Извлекает внутренний идентификатор этого сетевого интерфейса.
ms.assetid: 3e71c2cd-1a75-44d9-9a6d-04e6344dfec3
keywords:
- _ID метод Virtual PC
- _ID метод Virtual PC, интерфейс Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, метод _ID
topic_type:
- apiref
api_name:
- IVMNetworkAdapter._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9df514d24f9826b58964b4c51c9a76a9ba982e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988780"
---
# <a name="ivmnetworkadapter_id-method"></a><span data-ttu-id="1e721-106">Метод Ивмнетворкадаптер:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="1e721-106">IVMNetworkAdapter::\_ID method</span></span>

<span data-ttu-id="1e721-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1e721-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1e721-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1e721-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1e721-109">Извлекает внутренний идентификатор этого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1e721-109">Retrieves the internal identifier of this network interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e721-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e721-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *identifier
);
```



## <a name="parameters"></a><span data-ttu-id="1e721-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e721-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e721-112">*идентификатор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e721-112">*identifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e721-113">Внутренний идентификатор.</span><span class="sxs-lookup"><span data-stu-id="1e721-113">The internal identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e721-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e721-114">Return value</span></span>

<span data-ttu-id="1e721-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="1e721-115">This method can return one of these values.</span></span>



| <span data-ttu-id="1e721-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="1e721-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="1e721-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1e721-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="1e721-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1e721-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1e721-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1e721-119">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="1e721-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="1e721-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1e721-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1e721-121">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="1e721-122"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e721-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="1e721-123">Не удается найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="1e721-123">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="1e721-124"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1e721-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1e721-125">В операции произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1e721-125">The operation had an unknown error.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="1e721-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e721-126">Remarks</span></span>

<span data-ttu-id="1e721-127">Этот метод не может использоваться в языках сценариев.</span><span class="sxs-lookup"><span data-stu-id="1e721-127">This method is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e721-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1e721-128">Requirements</span></span>



| <span data-ttu-id="1e721-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1e721-129">Requirement</span></span> | <span data-ttu-id="1e721-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1e721-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e721-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e721-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1e721-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1e721-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e721-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e721-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1e721-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1e721-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1e721-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1e721-135">End of client support</span></span><br/>    | <span data-ttu-id="1e721-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e721-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1e721-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="1e721-137">Product</span></span><br/>                  | <span data-ttu-id="1e721-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e721-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1e721-139">Header</span><span class="sxs-lookup"><span data-stu-id="1e721-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e721-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e721-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1e721-141">IID</span><span class="sxs-lookup"><span data-stu-id="1e721-141">IID</span></span><br/>                      | <span data-ttu-id="1e721-142">IID \_ ивмнетворкадаптер определен как e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="1e721-142">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1e721-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e721-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e721-144">**ивмнетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="1e721-144">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

