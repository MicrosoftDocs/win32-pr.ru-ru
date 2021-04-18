---
title: Свойство Ивмхостинфо MMX (Впккоминтерфацес. h)
description: Определяет, поддерживает ли процессор набор инструкций MMX. | Свойство Ивмхостинфо MMX (Впккоминтерфацес. h)
ms.assetid: 2f556289-c752-4af2-a6d0-abb6e717e609
keywords:
- Виртуальное устройство MMX свойство Virtual PC
- Свойство MMX Virtual PC, интерфейс Ивмхостинфо
- Интерфейс Ивмхостинфо Virtual PC, свойство MMX
topic_type:
- apiref
api_name:
- IVMHostInfo.MMX
- IVMHostInfo.get_MMX
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e224ed6a0f15da9143a884dd1c1dfacc1634fce7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694013"
---
# <a name="ivmhostinfommx-property"></a><span data-ttu-id="a3fa9-107">Свойство Ивмхостинфо:: MMX</span><span class="sxs-lookup"><span data-stu-id="a3fa9-107">IVMHostInfo::MMX property</span></span>

<span data-ttu-id="a3fa9-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a3fa9-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a3fa9-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a3fa9-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a3fa9-110">Определяет, поддерживает ли процессор набор инструкций MMX.</span><span class="sxs-lookup"><span data-stu-id="a3fa9-110">Determines whether the processor supports the MMX instruction set.</span></span>

<span data-ttu-id="a3fa9-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a3fa9-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3fa9-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3fa9-112">Syntax</span></span>


```C++
HRESULT get_MMX(
  [out, retval] VARIANT_BOOL *mmxEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="a3fa9-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a3fa9-113">Property value</span></span>

<span data-ttu-id="a3fa9-114">**Значение true** , если инструкции MMX поддерживаются; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="a3fa9-114">**TRUE** if MMX instructions are supported, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3fa9-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a3fa9-115">Error codes</span></span>



| <span data-ttu-id="a3fa9-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="a3fa9-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a3fa9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a3fa9-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a3fa9-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a3fa9-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a3fa9-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a3fa9-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a3fa9-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="a3fa9-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a3fa9-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a3fa9-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a3fa9-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a3fa9-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a3fa9-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a3fa9-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a3fa9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a3fa9-124">Requirements</span></span>



| <span data-ttu-id="a3fa9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a3fa9-125">Requirement</span></span> | <span data-ttu-id="a3fa9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a3fa9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3fa9-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3fa9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a3fa9-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a3fa9-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a3fa9-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3fa9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a3fa9-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a3fa9-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a3fa9-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a3fa9-131">End of client support</span></span><br/>    | <span data-ttu-id="a3fa9-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3fa9-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a3fa9-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="a3fa9-133">Product</span></span><br/>                  | <span data-ttu-id="a3fa9-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a3fa9-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a3fa9-135">Header</span><span class="sxs-lookup"><span data-stu-id="a3fa9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3fa9-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3fa9-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a3fa9-137">IID</span><span class="sxs-lookup"><span data-stu-id="a3fa9-137">IID</span></span><br/>                      | <span data-ttu-id="a3fa9-138">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="a3fa9-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="a3fa9-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3fa9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3fa9-140">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="a3fa9-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

