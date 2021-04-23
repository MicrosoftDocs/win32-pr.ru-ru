---
title: Свойство Рдппипенаме Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Возвращает имя именованного канала RDP-подключения, используемого для видео и ввода.
ms.assetid: 0c2d0f23-40cd-4a86-96dd-546fb3570871
keywords:
- Рдппипенаме свойство Virtual PC
- Рдппипенаме свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Рдппипенаме
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RdpPipeName
- IVMVirtualMachine.get_RdpPipeName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86e49463c5e443a07d1fa86736047435eaf60a06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071059"
---
# <a name="ivmvirtualmachinerdppipename-property"></a><span data-ttu-id="2f2a0-106">Свойство Ивмвиртуалмачине:: Рдппипенаме</span><span class="sxs-lookup"><span data-stu-id="2f2a0-106">IVMVirtualMachine::RdpPipeName property</span></span>

<span data-ttu-id="2f2a0-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f2a0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2f2a0-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2f2a0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2f2a0-109">Возвращает имя именованного канала RDP-подключения, используемого для видео и ввода.</span><span class="sxs-lookup"><span data-stu-id="2f2a0-109">Retrieves the name of the RDP connection named pipe used for video and input.</span></span>

<span data-ttu-id="2f2a0-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2f2a0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2a0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f2a0-111">Syntax</span></span>


```C++
HRESULT get_RdpPipeName(
  [out, retval] BSTR *RdpPipeName
);
```



## <a name="property-value"></a><span data-ttu-id="2f2a0-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2f2a0-112">Property value</span></span>

<span data-ttu-id="2f2a0-113">Имя именованного канала RDP-подключения, используемого для видео и ввода.</span><span class="sxs-lookup"><span data-stu-id="2f2a0-113">Name of the RDP connection named pipe used for video and input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2f2a0-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2f2a0-114">Error codes</span></span>

<span data-ttu-id="2f2a0-115">Если метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2f2a0-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f2a0-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f2a0-116">Otherwise, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="2f2a0-117">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="2f2a0-117">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="2f2a0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2f2a0-118">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="2f2a0-119"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2f2a0-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="2f2a0-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2f2a0-120">The operation was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="2f2a0-121"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="2f2a0-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="2f2a0-122">Параметр Рдппипенаме имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2f2a0-122">The RdpPipeName parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="2f2a0-123"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="2f2a0-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="2f2a0-124">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="2f2a0-124">The virtual machine is not running.</span></span><br/>    |
| <dl> <span data-ttu-id="2f2a0-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2f2a0-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="2f2a0-126">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2f2a0-126">An unknown error occurred.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="2f2a0-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2f2a0-127">Requirements</span></span>



| <span data-ttu-id="2f2a0-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2f2a0-128">Requirement</span></span> | <span data-ttu-id="2f2a0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2f2a0-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2a0-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f2a0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2f2a0-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2f2a0-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f2a0-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f2a0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2f2a0-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2f2a0-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2f2a0-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2f2a0-134">End of client support</span></span><br/>    | <span data-ttu-id="2f2a0-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f2a0-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2f2a0-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="2f2a0-136">Product</span></span><br/>                  | <span data-ttu-id="2f2a0-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2f2a0-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2f2a0-138">Header</span><span class="sxs-lookup"><span data-stu-id="2f2a0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f2a0-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f2a0-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2f2a0-140">IID</span><span class="sxs-lookup"><span data-stu-id="2f2a0-140">IID</span></span><br/>                      | <span data-ttu-id="2f2a0-141">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="2f2a0-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2f2a0-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f2a0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2a0-143">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="2f2a0-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

