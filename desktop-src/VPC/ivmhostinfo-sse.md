---
title: Свойство SSE Ивмхостинфо (Впккоминтерфацес. h)
description: Определяет, поддерживает ли процессор набор инструкций SSE. | Свойство SSE Ивмхостинфо (Впккоминтерфацес. h)
ms.assetid: 135704db-757a-45b1-884a-5e26ef7d65c7
keywords:
- Виртуальный ПК со свойством SSE
- Свойство SSE Virtual PC, интерфейс Ивмхостинфо
- Интерфейс Ивмхостинфо Virtual PC, свойство SSE
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE
- IVMHostInfo.get_SSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02bef292e7dbcae48b9e2a6a94e7f879212a0dfc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353482"
---
# <a name="ivmhostinfosse-property"></a><span data-ttu-id="47650-107">Свойство Ивмхостинфо:: SSE</span><span class="sxs-lookup"><span data-stu-id="47650-107">IVMHostInfo::SSE property</span></span>

<span data-ttu-id="47650-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="47650-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="47650-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="47650-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="47650-110">Определяет, поддерживает ли процессор набор инструкций SSE.</span><span class="sxs-lookup"><span data-stu-id="47650-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="47650-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="47650-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="47650-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47650-112">Syntax</span></span>


```C++
HRESULT get_SSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="47650-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="47650-113">Property value</span></span>

<span data-ttu-id="47650-114">**Значение true** , если инструкции SSE поддерживаются процессором узла; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="47650-114">**TRUE** if SSE instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="47650-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="47650-115">Error codes</span></span>



| <span data-ttu-id="47650-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="47650-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="47650-117">Значение</span><span class="sxs-lookup"><span data-stu-id="47650-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="47650-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="47650-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="47650-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="47650-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="47650-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="47650-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="47650-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="47650-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="47650-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="47650-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="47650-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="47650-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="47650-124">Требования</span><span class="sxs-lookup"><span data-stu-id="47650-124">Requirements</span></span>



| <span data-ttu-id="47650-125">Требование</span><span class="sxs-lookup"><span data-stu-id="47650-125">Requirement</span></span> | <span data-ttu-id="47650-126">Значение</span><span class="sxs-lookup"><span data-stu-id="47650-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="47650-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47650-127">Minimum supported client</span></span><br/> | <span data-ttu-id="47650-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="47650-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47650-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47650-129">Minimum supported server</span></span><br/> | <span data-ttu-id="47650-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="47650-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="47650-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="47650-131">End of client support</span></span><br/>    | <span data-ttu-id="47650-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="47650-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="47650-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="47650-133">Product</span></span><br/>                  | <span data-ttu-id="47650-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="47650-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="47650-135">Header</span><span class="sxs-lookup"><span data-stu-id="47650-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="47650-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="47650-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="47650-137">IID</span><span class="sxs-lookup"><span data-stu-id="47650-137">IID</span></span><br/>                      | <span data-ttu-id="47650-138">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="47650-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="47650-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47650-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47650-140">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="47650-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

