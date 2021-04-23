---
title: Метод Ивмнетворкадаптер Аттачтовиртуалнетворк (Впккоминтерфацес. h)
description: Подключает сетевой интерфейс к указанной виртуальной сети.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- Метод Аттачтовиртуалнетворк Virtual PC
- Метод Аттачтовиртуалнетворк Virtual PC, интерфейс Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, метод Аттачтовиртуалнетворк
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491079"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a><span data-ttu-id="110ee-106">Метод Ивмнетворкадаптер:: Аттачтовиртуалнетворк</span><span class="sxs-lookup"><span data-stu-id="110ee-106">IVMNetworkAdapter::AttachToVirtualNetwork method</span></span>

<span data-ttu-id="110ee-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="110ee-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="110ee-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="110ee-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="110ee-109">Подключает сетевой интерфейс к указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="110ee-109">Attaches the network interface to the specified virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="110ee-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="110ee-110">Syntax</span></span>


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="110ee-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="110ee-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="110ee-112">*virtualNetwork* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="110ee-112">*virtualNetwork* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="110ee-113">Виртуальная сеть, к которой будет подключен этот виртуальный сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="110ee-113">The virtual network to which this virtual NIC will be connected.</span></span> <span data-ttu-id="110ee-114">См. [**ивмвиртуалнетворк**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="110ee-114">See [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="110ee-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="110ee-115">Return value</span></span>

<span data-ttu-id="110ee-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="110ee-116">This method can return one of these values.</span></span>



| <span data-ttu-id="110ee-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="110ee-117">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="110ee-118">Описание</span><span class="sxs-lookup"><span data-stu-id="110ee-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="110ee-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="110ee-119"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                       | <span data-ttu-id="110ee-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="110ee-120">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="110ee-121"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="110ee-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="110ee-122">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="110ee-122">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="110ee-123"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="110ee-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="110ee-124">Параметр не содержит допустимую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="110ee-124">The parameter does not contain a valid virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="110ee-125"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="110ee-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="110ee-126">Отказано в доступе к запрошенной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="110ee-126">Access was denied to the requested virtual network.</span></span><br/>     |
| <dl> <span data-ttu-id="110ee-127"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="110ee-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="110ee-128">Виртуальная машина недопустима или больше не существует.</span><span class="sxs-lookup"><span data-stu-id="110ee-128">The virtual machine is invalid or no longer exists.</span></span><br/>     |
| <dl> <span data-ttu-id="110ee-129"><dt>**Виртуальная машина \_ E \_ Недопустимый \_ \_ идентификатор виртуальной сети \_**</dt></span><span class="sxs-lookup"><span data-stu-id="110ee-129"><dt>**VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID**</dt></span></span> </dl>                                                                        | <span data-ttu-id="110ee-130">Параметр не является существующей виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="110ee-130">The parameter is not an existing virtual network.</span></span><br/>       |
| <dl> <span data-ttu-id="110ee-131"><dt>**отображаемое \_ \_ исключение E**</dt></span><span class="sxs-lookup"><span data-stu-id="110ee-131"><dt>**DISP\_E\_EXCEPTION**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="110ee-132">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="110ee-132">An unexpected error has occurred.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="110ee-133">Требования</span><span class="sxs-lookup"><span data-stu-id="110ee-133">Requirements</span></span>



| <span data-ttu-id="110ee-134">Требование</span><span class="sxs-lookup"><span data-stu-id="110ee-134">Requirement</span></span> | <span data-ttu-id="110ee-135">Значение</span><span class="sxs-lookup"><span data-stu-id="110ee-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="110ee-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="110ee-136">Minimum supported client</span></span><br/> | <span data-ttu-id="110ee-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="110ee-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="110ee-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="110ee-138">Minimum supported server</span></span><br/> | <span data-ttu-id="110ee-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="110ee-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="110ee-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="110ee-140">End of client support</span></span><br/>    | <span data-ttu-id="110ee-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="110ee-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="110ee-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="110ee-142">Product</span></span><br/>                  | <span data-ttu-id="110ee-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="110ee-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="110ee-144">Header</span><span class="sxs-lookup"><span data-stu-id="110ee-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="110ee-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="110ee-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="110ee-146">IID</span><span class="sxs-lookup"><span data-stu-id="110ee-146">IID</span></span><br/>                      | <span data-ttu-id="110ee-147">IID \_ ивмнетворкадаптер определен как e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="110ee-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="110ee-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="110ee-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="110ee-149">**ивмнетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="110ee-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

