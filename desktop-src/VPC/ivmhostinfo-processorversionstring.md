---
title: Свойство Процессорверсионстринг Ивмхостинфо (Впккоминтерфацес. h)
description: Возвращает версию процессора узла.
ms.assetid: 6cbf0295-7975-4b3c-903f-3deded218184
keywords:
- Процессорверсионстринг свойство Virtual PC
- Процессорверсионстринг свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Процессорверсионстринг
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorVersionString
- IVMHostInfo.get_ProcessorVersionString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0af54c99df18b2c650c31c8ee01d1cca9e37942
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533737"
---
# <a name="ivmhostinfoprocessorversionstring-property"></a><span data-ttu-id="13ea3-106">Ивмхостинфо: свойство Роцессорверсионстринг:P</span><span class="sxs-lookup"><span data-stu-id="13ea3-106">IVMHostInfo::ProcessorVersionString property</span></span>

<span data-ttu-id="13ea3-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="13ea3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="13ea3-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="13ea3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="13ea3-109">Возвращает версию процессора узла.</span><span class="sxs-lookup"><span data-stu-id="13ea3-109">Retrieves the version of the host processor.</span></span>

<span data-ttu-id="13ea3-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="13ea3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ea3-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13ea3-111">Syntax</span></span>


```C++
HRESULT get_ProcessorVersionString(
  [out, retval] BSTR *processorVersionString
);
```



## <a name="property-value"></a><span data-ttu-id="13ea3-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="13ea3-112">Property value</span></span>

<span data-ttu-id="13ea3-113">Версия процессора.</span><span class="sxs-lookup"><span data-stu-id="13ea3-113">The processor version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13ea3-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="13ea3-114">Error codes</span></span>



| <span data-ttu-id="13ea3-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="13ea3-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="13ea3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="13ea3-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="13ea3-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="13ea3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="13ea3-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="13ea3-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="13ea3-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="13ea3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="13ea3-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="13ea3-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="13ea3-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="13ea3-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="13ea3-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="13ea3-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="13ea3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="13ea3-123">Requirements</span></span>



| <span data-ttu-id="13ea3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="13ea3-124">Requirement</span></span> | <span data-ttu-id="13ea3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="13ea3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="13ea3-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13ea3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="13ea3-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="13ea3-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13ea3-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13ea3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="13ea3-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="13ea3-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="13ea3-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="13ea3-130">End of client support</span></span><br/>    | <span data-ttu-id="13ea3-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="13ea3-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="13ea3-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="13ea3-132">Product</span></span><br/>                  | <span data-ttu-id="13ea3-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="13ea3-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="13ea3-134">Header</span><span class="sxs-lookup"><span data-stu-id="13ea3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="13ea3-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="13ea3-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="13ea3-136">IID</span><span class="sxs-lookup"><span data-stu-id="13ea3-136">IID</span></span><br/>                      | <span data-ttu-id="13ea3-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="13ea3-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="13ea3-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13ea3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ea3-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="13ea3-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

