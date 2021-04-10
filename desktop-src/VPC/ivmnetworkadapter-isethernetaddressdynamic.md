---
title: Свойство Исесернетаддрессдинамик Ивмнетворкадаптер (Впккоминтерфацес. h)
description: Определяет, создается ли адрес Ethernet динамически.
ms.assetid: 7bd87868-f1d1-48e5-9e1b-04d2126f9dad
keywords:
- Исесернетаддрессдинамик свойство Virtual PC
- Исесернетаддрессдинамик свойство Virtual PC, интерфейс Ивмнетворкадаптер
- Ивмнетворкадаптер интерфейс Virtual PC, свойство Исесернетаддрессдинамик
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.IsEthernetAddressDynamic
- IVMNetworkAdapter.get_IsEthernetAddressDynamic
- IVMNetworkAdapter.put_IsEthernetAddressDynamic
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b16074243094d410e8d39538b024120daa1871e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071064"
---
# <a name="ivmnetworkadapterisethernetaddressdynamic-property"></a><span data-ttu-id="717ac-106">Свойство Ивмнетворкадаптер:: Исесернетаддрессдинамик</span><span class="sxs-lookup"><span data-stu-id="717ac-106">IVMNetworkAdapter::IsEthernetAddressDynamic property</span></span>

<span data-ttu-id="717ac-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="717ac-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="717ac-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="717ac-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="717ac-109">Определяет, создается ли адрес Ethernet динамически.</span><span class="sxs-lookup"><span data-stu-id="717ac-109">Determines whether the Ethernet address is dynamically generated.</span></span>

<span data-ttu-id="717ac-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="717ac-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="717ac-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="717ac-111">Syntax</span></span>


```C++
HRESULT put_IsEthernetAddressDynamic(
  [in]          VARIANT_BOOL isDynamic
);

HRESULT get_IsEthernetAddressDynamic(
  [out, retval] VARIANT_BOOL *isDynamic
);
```



## <a name="property-value"></a><span data-ttu-id="717ac-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="717ac-112">Property value</span></span>

<span data-ttu-id="717ac-113">Задайте значение \_ true, если адрес Ethernet должен быть динамически создан, и вариант \_ false, если адрес Ethernet является статическим.</span><span class="sxs-lookup"><span data-stu-id="717ac-113">Set to VARIANT\_TRUE if the Ethernet address should be dynamically generated and VARIANT\_FALSE if the Ethernet address is static.</span></span>

## <a name="error-codes"></a><span data-ttu-id="717ac-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="717ac-114">Error codes</span></span>



| <span data-ttu-id="717ac-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="717ac-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="717ac-116">Значение</span><span class="sxs-lookup"><span data-stu-id="717ac-116">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="717ac-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="717ac-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="717ac-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="717ac-118">The operation was successful.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="717ac-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="717ac-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="717ac-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="717ac-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="717ac-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="717ac-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="717ac-122">Виртуальная машина не найдена.</span><span class="sxs-lookup"><span data-stu-id="717ac-122">The virtual machine was not found.</span></span> <span data-ttu-id="717ac-123">Это может произойти, если компьютер был удален после создания объекта [**ивмнетворкадаптер**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="717ac-123">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/> |
| <dl> <span data-ttu-id="717ac-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="717ac-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="717ac-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="717ac-125">An unexpected error has occurred.</span></span><br/>                                                                                                                         |



## <a name="remarks"></a><span data-ttu-id="717ac-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="717ac-126">Remarks</span></span>

<span data-ttu-id="717ac-127">Для большинства виртуальных сетевых интерфейсов этому свойству должно быть присвоено значение **true** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="717ac-127">This property should be set to **TRUE** (default) for most virtual network interfaces.</span></span> <span data-ttu-id="717ac-128">Если для программного обеспечения в гостевой системе требуется статический Ethernet-адрес, это свойство должно иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="717ac-128">If software in the guest requires a static Ethernet address, this property should be set to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="717ac-129">Требования</span><span class="sxs-lookup"><span data-stu-id="717ac-129">Requirements</span></span>



| <span data-ttu-id="717ac-130">Требование</span><span class="sxs-lookup"><span data-stu-id="717ac-130">Requirement</span></span> | <span data-ttu-id="717ac-131">Значение</span><span class="sxs-lookup"><span data-stu-id="717ac-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="717ac-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="717ac-132">Minimum supported client</span></span><br/> | <span data-ttu-id="717ac-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="717ac-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="717ac-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="717ac-134">Minimum supported server</span></span><br/> | <span data-ttu-id="717ac-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="717ac-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="717ac-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="717ac-136">End of client support</span></span><br/>    | <span data-ttu-id="717ac-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="717ac-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="717ac-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="717ac-138">Product</span></span><br/>                  | <span data-ttu-id="717ac-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="717ac-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="717ac-140">Header</span><span class="sxs-lookup"><span data-stu-id="717ac-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="717ac-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="717ac-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="717ac-142">IID</span><span class="sxs-lookup"><span data-stu-id="717ac-142">IID</span></span><br/>                      | <span data-ttu-id="717ac-143">IID \_ ивмнетворкадаптер определен как e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="717ac-143">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="717ac-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="717ac-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="717ac-145">**ивмнетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="717ac-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

