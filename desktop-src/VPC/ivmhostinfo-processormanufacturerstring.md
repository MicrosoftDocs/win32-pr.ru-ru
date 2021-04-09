---
title: Свойство Процессормануфактурерстринг Ивмхостинфо (Впккоминтерфацес. h)
description: Получает изготовителя хоста процессора.
ms.assetid: b7f4a03a-184c-4996-8102-994bf7f37e50
keywords:
- Процессормануфактурерстринг свойство Virtual PC
- Процессормануфактурерстринг свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Процессормануфактурерстринг
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorManufacturerString
- IVMHostInfo.get_ProcessorManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029e64f0a13d84bea118498726893620e058ac83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071068"
---
# <a name="ivmhostinfoprocessormanufacturerstring-property"></a><span data-ttu-id="f3bca-106">Ивмхостинфо: свойство Роцессормануфактурерстринг:P</span><span class="sxs-lookup"><span data-stu-id="f3bca-106">IVMHostInfo::ProcessorManufacturerString property</span></span>

<span data-ttu-id="f3bca-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f3bca-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f3bca-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f3bca-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f3bca-109">Получает изготовителя хоста процессора.</span><span class="sxs-lookup"><span data-stu-id="f3bca-109">Retrieves the manufacturer of the host processor.</span></span>

<span data-ttu-id="f3bca-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f3bca-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3bca-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3bca-111">Syntax</span></span>


```C++
HRESULT get_ProcessorManufacturerString(
  [out, retval] BSTR *processorManufacturerString
);
```



## <a name="property-value"></a><span data-ttu-id="f3bca-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f3bca-112">Property value</span></span>

<span data-ttu-id="f3bca-113">Производитель.</span><span class="sxs-lookup"><span data-stu-id="f3bca-113">The manufacturer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f3bca-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f3bca-114">Error codes</span></span>



| <span data-ttu-id="f3bca-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="f3bca-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f3bca-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f3bca-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f3bca-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3bca-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f3bca-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f3bca-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f3bca-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="f3bca-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f3bca-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f3bca-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f3bca-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f3bca-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f3bca-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f3bca-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f3bca-123">Требования</span><span class="sxs-lookup"><span data-stu-id="f3bca-123">Requirements</span></span>



| <span data-ttu-id="f3bca-124">Требование</span><span class="sxs-lookup"><span data-stu-id="f3bca-124">Requirement</span></span> | <span data-ttu-id="f3bca-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f3bca-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3bca-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3bca-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f3bca-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f3bca-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3bca-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3bca-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f3bca-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f3bca-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f3bca-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f3bca-130">End of client support</span></span><br/>    | <span data-ttu-id="f3bca-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3bca-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f3bca-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="f3bca-132">Product</span></span><br/>                  | <span data-ttu-id="f3bca-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f3bca-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f3bca-134">Header</span><span class="sxs-lookup"><span data-stu-id="f3bca-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3bca-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3bca-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f3bca-136">IID</span><span class="sxs-lookup"><span data-stu-id="f3bca-136">IID</span></span><br/>                      | <span data-ttu-id="f3bca-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="f3bca-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f3bca-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3bca-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3bca-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="f3bca-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

