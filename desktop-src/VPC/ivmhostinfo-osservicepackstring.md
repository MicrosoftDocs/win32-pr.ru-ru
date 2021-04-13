---
title: Свойство Оссервицепаккстринг Ивмхостинфо (Впккоминтерфацес. h)
description: Извлекает сведения о пакете обновления операционной системы, работающей на размещающем компьютере.
ms.assetid: e5fe51f8-9bcf-49bd-bec6-2538b3e8edfa
keywords:
- Оссервицепаккстринг свойство Virtual PC
- Оссервицепаккстринг свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Оссервицепаккстринг
topic_type:
- apiref
api_name:
- IVMHostInfo.OSServicePackString
- IVMHostInfo.get_OSServicePackString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a046499b72333b4acf8daffbd66dbab44107e0b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340325"
---
# <a name="ivmhostinfoosservicepackstring-property"></a><span data-ttu-id="51a2c-106">Свойство Ивмхостинфо:: Оссервицепаккстринг</span><span class="sxs-lookup"><span data-stu-id="51a2c-106">IVMHostInfo::OSServicePackString property</span></span>

<span data-ttu-id="51a2c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="51a2c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="51a2c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="51a2c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="51a2c-109">Извлекает сведения о пакете обновления операционной системы, работающей на размещающем компьютере.</span><span class="sxs-lookup"><span data-stu-id="51a2c-109">Retrieves the service pack information of the operating system running on the host machine.</span></span>

<span data-ttu-id="51a2c-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="51a2c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="51a2c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51a2c-111">Syntax</span></span>


```C++
HRESULT get_OSServicePackString(
  [out, retval] BSTR *OSServicePack
);
```



## <a name="property-value"></a><span data-ttu-id="51a2c-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="51a2c-112">Property value</span></span>

<span data-ttu-id="51a2c-113">Версия пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="51a2c-113">The service pack version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="51a2c-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="51a2c-114">Error codes</span></span>



| <span data-ttu-id="51a2c-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="51a2c-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="51a2c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="51a2c-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="51a2c-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="51a2c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="51a2c-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="51a2c-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="51a2c-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="51a2c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="51a2c-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="51a2c-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="51a2c-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="51a2c-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="51a2c-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="51a2c-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="51a2c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="51a2c-123">Requirements</span></span>



| <span data-ttu-id="51a2c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="51a2c-124">Requirement</span></span> | <span data-ttu-id="51a2c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="51a2c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51a2c-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51a2c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="51a2c-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="51a2c-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51a2c-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51a2c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="51a2c-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="51a2c-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="51a2c-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="51a2c-130">End of client support</span></span><br/>    | <span data-ttu-id="51a2c-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51a2c-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="51a2c-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="51a2c-132">Product</span></span><br/>                  | <span data-ttu-id="51a2c-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="51a2c-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="51a2c-134">Header</span><span class="sxs-lookup"><span data-stu-id="51a2c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="51a2c-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="51a2c-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="51a2c-136">IID</span><span class="sxs-lookup"><span data-stu-id="51a2c-136">IID</span></span><br/>                      | <span data-ttu-id="51a2c-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="51a2c-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="51a2c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51a2c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51a2c-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="51a2c-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

