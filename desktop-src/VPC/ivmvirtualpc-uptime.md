---
title: Свойство Ивмвиртуалпк "время работы" (Впккоминтерфацес. h)
description: Возвращает количество секунд, в течение которых приложение Windows Virtual PC было запущено.
ms.assetid: 3007a961-2e8c-4674-aab6-4424d0d73eca
keywords:
- Свойство "время работоспособности" Virtual PC
- Свойство "время работы" Virtual PC, интерфейс Ивмвиртуалпк
- Виртуальный ПК интерфейса Ивмвиртуалпк, свойство времени работы
topic_type:
- apiref
api_name:
- IVMVirtualPC.UpTime
- IVMVirtualPC.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab07128380a097677e0ad8acca5208e5cef11da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803730"
---
# <a name="ivmvirtualpcuptime-property"></a><span data-ttu-id="f6797-106">Свойство Ивмвиртуалпк:: время работы</span><span class="sxs-lookup"><span data-stu-id="f6797-106">IVMVirtualPC::UpTime property</span></span>

<span data-ttu-id="f6797-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f6797-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f6797-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f6797-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f6797-109">Возвращает количество секунд, в течение которых приложение Windows Virtual PC было запущено.</span><span class="sxs-lookup"><span data-stu-id="f6797-109">Retrieves the number of seconds the Windows Virtual PC application has been running.</span></span>

<span data-ttu-id="f6797-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f6797-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6797-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6797-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="f6797-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f6797-112">Property value</span></span>

<span data-ttu-id="f6797-113">Количество секунд, в течение которых было запущено приложение Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="f6797-113">The number of seconds that the Windows Virtual PC application has been running.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f6797-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f6797-114">Error codes</span></span>



| <span data-ttu-id="f6797-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="f6797-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="f6797-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f6797-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6797-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6797-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="f6797-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f6797-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f6797-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="f6797-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="f6797-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f6797-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="f6797-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f6797-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="f6797-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f6797-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="f6797-123"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="f6797-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="f6797-124">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="f6797-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f6797-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f6797-125">Requirements</span></span>



| <span data-ttu-id="f6797-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f6797-126">Requirement</span></span> | <span data-ttu-id="f6797-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f6797-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6797-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6797-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f6797-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f6797-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6797-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6797-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f6797-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6797-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f6797-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f6797-132">End of client support</span></span><br/>    | <span data-ttu-id="f6797-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6797-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f6797-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="f6797-134">Product</span></span><br/>                  | <span data-ttu-id="f6797-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f6797-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f6797-136">Header</span><span class="sxs-lookup"><span data-stu-id="f6797-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6797-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6797-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f6797-138">IID</span><span class="sxs-lookup"><span data-stu-id="f6797-138">IID</span></span><br/>                      | <span data-ttu-id="f6797-139">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="f6797-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f6797-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6797-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6797-141">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="f6797-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

