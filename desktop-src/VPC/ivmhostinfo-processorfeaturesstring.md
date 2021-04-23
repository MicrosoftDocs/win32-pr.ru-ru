---
title: Свойство Процессорфеатуресстринг Ивмхостинфо (Впккоминтерфацес. h)
description: Возвращает список возможностей, поддерживаемых процессором узла.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- Процессорфеатуресстринг свойство Virtual PC
- Процессорфеатуресстринг свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Процессорфеатуресстринг
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672455"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a><span data-ttu-id="92548-106">Ивмхостинфо: свойство Роцессорфеатуресстринг:P</span><span class="sxs-lookup"><span data-stu-id="92548-106">IVMHostInfo::ProcessorFeaturesString property</span></span>

<span data-ttu-id="92548-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="92548-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="92548-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="92548-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="92548-109">Возвращает список возможностей, поддерживаемых процессором узла.</span><span class="sxs-lookup"><span data-stu-id="92548-109">Retrieves the list features supported by the host processor.</span></span>

<span data-ttu-id="92548-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="92548-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="92548-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92548-111">Syntax</span></span>


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a><span data-ttu-id="92548-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="92548-112">Property value</span></span>

<span data-ttu-id="92548-113">Разделенный запятыми список функций.</span><span class="sxs-lookup"><span data-stu-id="92548-113">A comma-delimited list of features.</span></span> <span data-ttu-id="92548-114">Примером может быть "MMX, SSE, SSE2, x86-64".</span><span class="sxs-lookup"><span data-stu-id="92548-114">An example would be "MMX,SSE,SSE2,x86-64".</span></span>



| <span data-ttu-id="92548-115">Значение</span><span class="sxs-lookup"><span data-stu-id="92548-115">Value</span></span>                                                                                 | <span data-ttu-id="92548-116">Значение</span><span class="sxs-lookup"><span data-stu-id="92548-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="92548-117"><dt>"AMD-V"</dt></span><span class="sxs-lookup"><span data-stu-id="92548-117"><dt>"AMD-V"</dt></span></span> </dl>    | <span data-ttu-id="92548-118">Поддерживает расширения виртуализации AMD.</span><span class="sxs-lookup"><span data-stu-id="92548-118">Supports the AMD Virtualization extensions.</span></span><br/>              |
| <dl> <span data-ttu-id="92548-119"><dt>"Intel VT"</dt></span><span class="sxs-lookup"><span data-stu-id="92548-119"><dt>"Intel VT"</dt></span></span> </dl> | <span data-ttu-id="92548-120">Поддерживает расширения технологии виртуализации Intel.</span><span class="sxs-lookup"><span data-stu-id="92548-120">Supports the Intel Virtualization Technology extensions.</span></span><br/> |
| <dl> <span data-ttu-id="92548-121"><dt>"ХАВД"</dt></span><span class="sxs-lookup"><span data-stu-id="92548-121"><dt>"HAVD"</dt></span></span> </dl>     | <span data-ttu-id="92548-122">Аппаратная виртуализация отключена.</span><span class="sxs-lookup"><span data-stu-id="92548-122">Hardware Assisted Virtualization is disabled.</span></span><br/>            |
| <dl> <span data-ttu-id="92548-123"><dt>ИМЕЕТЕ</dt></span><span class="sxs-lookup"><span data-stu-id="92548-123"><dt>"HAVE"</dt></span></span> </dl>     | <span data-ttu-id="92548-124">Виртуализация с поддержкой оборудования включена.</span><span class="sxs-lookup"><span data-stu-id="92548-124">Hardware Assisted Virtualization is enabled.</span></span><br/>             |
| <dl> <span data-ttu-id="92548-125"><dt>ТЕХНОЛОГИЕЙ</dt></span><span class="sxs-lookup"><span data-stu-id="92548-125"><dt>"MMX"</dt></span></span> </dl>      | <span data-ttu-id="92548-126">Поддерживает расширения MMX.</span><span class="sxs-lookup"><span data-stu-id="92548-126">Supports the MMX extensions.</span></span><br/>                             |
| <dl> <span data-ttu-id="92548-127"><dt>ИСПОЛЬЗУЕМЫЙ</dt></span><span class="sxs-lookup"><span data-stu-id="92548-127"><dt>"SSE"</dt></span></span> </dl>      | <span data-ttu-id="92548-128">Поддерживает расширения Streaming SIMD.</span><span class="sxs-lookup"><span data-stu-id="92548-128">Supports the Streaming SIMD Extensions.</span></span><br/>                  |
| <dl> <span data-ttu-id="92548-129"><dt>ПОДДЕРЖИВАЮЩ</dt></span><span class="sxs-lookup"><span data-stu-id="92548-129"><dt>"SSE2"</dt></span></span> </dl>     | <span data-ttu-id="92548-130">Поддерживает расширения Streaming SIMD Extensions 2.</span><span class="sxs-lookup"><span data-stu-id="92548-130">Supports the Streaming SIMD Extensions 2.</span></span><br/>                |
| <dl> <span data-ttu-id="92548-131"><dt>SSE3</dt></span><span class="sxs-lookup"><span data-stu-id="92548-131"><dt>"SSE3"</dt></span></span> </dl>     | <span data-ttu-id="92548-132">Поддерживает потоковые SIMD расширения 3.</span><span class="sxs-lookup"><span data-stu-id="92548-132">Supports the Streaming SIMD Extensions 3.</span></span><br/>                |
| <dl> <span data-ttu-id="92548-133"><dt>"ТКСТЕ"</dt></span><span class="sxs-lookup"><span data-stu-id="92548-133"><dt>"TXTE"</dt></span></span> </dl>     | <span data-ttu-id="92548-134">Поддерживает расширения технологии доверенного выполнения.</span><span class="sxs-lookup"><span data-stu-id="92548-134">Supports the Trusted Execution Technology extensions.</span></span><br/>    |
| <dl> <span data-ttu-id="92548-135"><dt>"x86-64"</dt></span><span class="sxs-lookup"><span data-stu-id="92548-135"><dt>"x86-64"</dt></span></span> </dl>   | <span data-ttu-id="92548-136">Поддерживает расширения x86-64.</span><span class="sxs-lookup"><span data-stu-id="92548-136">Supports x86-64 extensions.</span></span><br/>                              |



 

## <a name="error-codes"></a><span data-ttu-id="92548-137">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="92548-137">Error codes</span></span>



| <span data-ttu-id="92548-138">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="92548-138">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="92548-139">Значение</span><span class="sxs-lookup"><span data-stu-id="92548-139">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="92548-140"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="92548-140"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="92548-141">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="92548-141">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="92548-142"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="92548-142"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="92548-143">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="92548-143">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="92548-144"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="92548-144"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="92548-145">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="92548-145">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="92548-146">Требования</span><span class="sxs-lookup"><span data-stu-id="92548-146">Requirements</span></span>



| <span data-ttu-id="92548-147">Требование</span><span class="sxs-lookup"><span data-stu-id="92548-147">Requirement</span></span> | <span data-ttu-id="92548-148">Значение</span><span class="sxs-lookup"><span data-stu-id="92548-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="92548-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92548-149">Minimum supported client</span></span><br/> | <span data-ttu-id="92548-150">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="92548-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="92548-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92548-151">Minimum supported server</span></span><br/> | <span data-ttu-id="92548-152">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="92548-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="92548-153">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="92548-153">End of client support</span></span><br/>    | <span data-ttu-id="92548-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="92548-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="92548-155">Продукт</span><span class="sxs-lookup"><span data-stu-id="92548-155">Product</span></span><br/>                  | <span data-ttu-id="92548-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="92548-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="92548-157">Header</span><span class="sxs-lookup"><span data-stu-id="92548-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="92548-158"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="92548-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="92548-159">IID</span><span class="sxs-lookup"><span data-stu-id="92548-159">IID</span></span><br/>                      | <span data-ttu-id="92548-160">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="92548-160">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="92548-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92548-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92548-162">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="92548-162">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

