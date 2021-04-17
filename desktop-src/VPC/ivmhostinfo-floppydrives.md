---
title: Свойство Флоппидривес Ивмхостинфо (Впккоминтерфацес. h)
description: Возвращает буквы дисков, связанные с дисководами гибких дисков узла.
ms.assetid: 9a8ab4b5-6ee8-463f-809b-b88cd28d9373
keywords:
- Флоппидривес свойство Virtual PC
- Флоппидривес свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство Флоппидривес
topic_type:
- apiref
api_name:
- IVMHostInfo.FloppyDrives
- IVMHostInfo.get_FloppyDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c31e3ece942f31fc6245c9f23a2995eb7b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415732"
---
# <a name="ivmhostinfofloppydrives-property"></a><span data-ttu-id="3c3b0-106">Свойство Ивмхостинфо:: Флоппидривес</span><span class="sxs-lookup"><span data-stu-id="3c3b0-106">IVMHostInfo::FloppyDrives property</span></span>

<span data-ttu-id="3c3b0-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3c3b0-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3c3b0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3c3b0-109">Возвращает буквы дисков, связанные с дисководами гибких дисков узла.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-109">Retrieves the drive letters associated with host floppy drives.</span></span>

<span data-ttu-id="3c3b0-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3b0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c3b0-111">Syntax</span></span>


```C++
HRESULT get_FloppyDrives(
  [out, retval] VARIANT *floppyDrives
);
```



## <a name="property-value"></a><span data-ttu-id="3c3b0-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3c3b0-112">Property value</span></span>

<span data-ttu-id="3c3b0-113">Массив букв диска.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-113">An array of drive letters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c3b0-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3c3b0-114">Error codes</span></span>



| <span data-ttu-id="3c3b0-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="3c3b0-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3c3b0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3c3b0-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3c3b0-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c3b0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3c3b0-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3c3b0-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="3c3b0-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3c3b0-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3c3b0-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3c3b0-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3c3b0-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3c3b0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3c3b0-123">Requirements</span></span>



| <span data-ttu-id="3c3b0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3c3b0-124">Requirement</span></span> | <span data-ttu-id="3c3b0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3c3b0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3b0-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c3b0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3c3b0-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3c3b0-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c3b0-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c3b0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3c3b0-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3c3b0-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3c3b0-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3c3b0-130">End of client support</span></span><br/>    | <span data-ttu-id="3c3b0-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3c3b0-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3c3b0-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="3c3b0-132">Product</span></span><br/>                  | <span data-ttu-id="3c3b0-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3c3b0-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3c3b0-134">Header</span><span class="sxs-lookup"><span data-stu-id="3c3b0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c3b0-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c3b0-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3c3b0-136">IID</span><span class="sxs-lookup"><span data-stu-id="3c3b0-136">IID</span></span><br/>                      | <span data-ttu-id="3c3b0-137">IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="3c3b0-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3c3b0-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c3b0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3b0-139">**ивмхостинфо**</span><span class="sxs-lookup"><span data-stu-id="3c3b0-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

