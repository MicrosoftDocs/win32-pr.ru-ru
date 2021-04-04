---
title: Свойство Ивмпараллелпортколлектион Count (Впккоминтерфацес. h)
description: Число параллельных портов в этой коллекции.
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмпараллелпортколлектион
- Ивмпараллелпортколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988747"
---
# <a name="ivmparallelportcollectioncount-property"></a><span data-ttu-id="7e3eb-106">Свойство Ивмпараллелпортколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="7e3eb-106">IVMParallelPortCollection::Count property</span></span>

<span data-ttu-id="7e3eb-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7e3eb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7e3eb-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7e3eb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7e3eb-109">Возвращает число параллельных портов в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="7e3eb-109">Retrieves the number of parallel ports in this collection.</span></span>

<span data-ttu-id="7e3eb-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7e3eb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e3eb-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e3eb-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="7e3eb-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7e3eb-112">Property value</span></span>

<span data-ttu-id="7e3eb-113">Число параллельных портов.</span><span class="sxs-lookup"><span data-stu-id="7e3eb-113">The number of parallel ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7e3eb-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7e3eb-114">Error codes</span></span>



| <span data-ttu-id="7e3eb-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="7e3eb-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="7e3eb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7e3eb-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="7e3eb-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7e3eb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="7e3eb-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7e3eb-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="7e3eb-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="7e3eb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="7e3eb-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7e3eb-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="7e3eb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7e3eb-121">Requirements</span></span>



| <span data-ttu-id="7e3eb-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7e3eb-122">Requirement</span></span> | <span data-ttu-id="7e3eb-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7e3eb-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e3eb-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e3eb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7e3eb-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7e3eb-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e3eb-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e3eb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7e3eb-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7e3eb-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7e3eb-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7e3eb-128">End of client support</span></span><br/>    | <span data-ttu-id="7e3eb-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e3eb-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7e3eb-130">Продукт</span><span class="sxs-lookup"><span data-stu-id="7e3eb-130">Product</span></span><br/>                  | <span data-ttu-id="7e3eb-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7e3eb-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7e3eb-132">Header</span><span class="sxs-lookup"><span data-stu-id="7e3eb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e3eb-133"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e3eb-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7e3eb-134">IID</span><span class="sxs-lookup"><span data-stu-id="7e3eb-134">IID</span></span><br/>                      | <span data-ttu-id="7e3eb-135">IID \_ ивмпараллелпортколлектион определен как 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="7e3eb-135">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="7e3eb-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e3eb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e3eb-137">**ивмпараллелпортколлектион**</span><span class="sxs-lookup"><span data-stu-id="7e3eb-137">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

