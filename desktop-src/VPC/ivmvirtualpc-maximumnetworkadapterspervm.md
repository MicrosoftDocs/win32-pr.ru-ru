---
title: Свойство Максимумнетворкадаптерспервм Ивмвиртуалпк (Впккоминтерфацес. h)
description: Максимальное число сетевых интерфейсов на виртуальную машину.
ms.assetid: 92da4958-5a67-422e-a6bd-68cabf1835ab
keywords:
- Максимумнетворкадаптерспервм свойство Virtual PC
- Максимумнетворкадаптерспервм свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Максимумнетворкадаптерспервм
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumNetworkAdaptersPerVM
- IVMVirtualPC.get_MaximumNetworkAdaptersPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0797775038440c566fa7a3397b05632af839a341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135027"
---
# <a name="ivmvirtualpcmaximumnetworkadapterspervm-property"></a><span data-ttu-id="18daf-106">Свойство Ивмвиртуалпк:: Максимумнетворкадаптерспервм</span><span class="sxs-lookup"><span data-stu-id="18daf-106">IVMVirtualPC::MaximumNetworkAdaptersPerVM property</span></span>

<span data-ttu-id="18daf-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="18daf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="18daf-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="18daf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="18daf-109">Возвращает максимальное число сетевых интерфейсов на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="18daf-109">Retrieves the maximum number of networks interfaces per virtual machine.</span></span>

<span data-ttu-id="18daf-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="18daf-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="18daf-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18daf-111">Syntax</span></span>


```C++
HRESULT get_MaximumNetworkAdaptersPerVM(
  [out, retval] long *maxNetworkAdapters
);
```



## <a name="property-value"></a><span data-ttu-id="18daf-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="18daf-112">Property value</span></span>

<span data-ttu-id="18daf-113">Максимальное число сетевых интерфейсов на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="18daf-113">The maximum number of network interfaces per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="18daf-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="18daf-114">Error codes</span></span>



| <span data-ttu-id="18daf-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="18daf-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="18daf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="18daf-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="18daf-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="18daf-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="18daf-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="18daf-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="18daf-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="18daf-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="18daf-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="18daf-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="18daf-121"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="18daf-121"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="18daf-122">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="18daf-122">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="18daf-123">Требования</span><span class="sxs-lookup"><span data-stu-id="18daf-123">Requirements</span></span>



| <span data-ttu-id="18daf-124">Требование</span><span class="sxs-lookup"><span data-stu-id="18daf-124">Requirement</span></span> | <span data-ttu-id="18daf-125">Значение</span><span class="sxs-lookup"><span data-stu-id="18daf-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="18daf-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18daf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="18daf-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="18daf-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18daf-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18daf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="18daf-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="18daf-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="18daf-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="18daf-130">End of client support</span></span><br/>    | <span data-ttu-id="18daf-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="18daf-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="18daf-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="18daf-132">Product</span></span><br/>                  | <span data-ttu-id="18daf-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="18daf-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="18daf-134">Header</span><span class="sxs-lookup"><span data-stu-id="18daf-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="18daf-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="18daf-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="18daf-136">IID</span><span class="sxs-lookup"><span data-stu-id="18daf-136">IID</span></span><br/>                      | <span data-ttu-id="18daf-137">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="18daf-137">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="18daf-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18daf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18daf-139">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="18daf-139">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

