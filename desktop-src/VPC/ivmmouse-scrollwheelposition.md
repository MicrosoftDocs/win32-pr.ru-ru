---
title: Свойство Скроллвхилпоситион Ивммаусе (Впккоминтерфацес. h)
description: Настраивает z-координату мыши (только относительную).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- Скроллвхилпоситион свойство Virtual PC
- Скроллвхилпоситион свойство Virtual PC, интерфейс Ивммаусе
- Ивммаусе интерфейс Virtual PC, свойство Скроллвхилпоситион
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803742"
---
# <a name="ivmmousescrollwheelposition-property"></a><span data-ttu-id="2c436-106">Свойство Ивммаусе:: Скроллвхилпоситион</span><span class="sxs-lookup"><span data-stu-id="2c436-106">IVMMouse::ScrollWheelPosition property</span></span>

<span data-ttu-id="2c436-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2c436-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2c436-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2c436-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2c436-109">Настраивает z-координату мыши (только относительную).</span><span class="sxs-lookup"><span data-stu-id="2c436-109">Adjusts the z-coordinate of the mouse (relative only).</span></span>

<span data-ttu-id="2c436-110">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="2c436-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c436-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c436-111">Syntax</span></span>


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a><span data-ttu-id="2c436-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2c436-112">Property value</span></span>

<span data-ttu-id="2c436-113">Координата z, указывающая количество пикселей, на которое мышь перемещается вдоль оси z.</span><span class="sxs-lookup"><span data-stu-id="2c436-113">The z-coordinate indicating the number of pixels the mouse is to be moved along the z-axis.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2c436-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2c436-114">Error codes</span></span>



| <span data-ttu-id="2c436-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="2c436-115">Name/value</span></span>                                                                                                                                                                     | <span data-ttu-id="2c436-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2c436-116">Meaning</span></span>                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c436-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2c436-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                        | <span data-ttu-id="2c436-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2c436-118">The operation was successful.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="2c436-119"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="2c436-119"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>             | <span data-ttu-id="2c436-120">Виртуальная машина, к которой подключено это устройство с мышью, в данный момент не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c436-120">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>         |
| <dl> <span data-ttu-id="2c436-121"><dt>Виртуальная машина \_ Электронная \_ мышь \_ не \_ активна</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="2c436-121"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>           | <span data-ttu-id="2c436-122">Устройство мыши не включено или сейчас не активно на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2c436-122">The mouse device has not been powered up, or is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="2c436-123"><dt>Виртуальная машина \_ E \_ использование \_ абсолютных \_ координат</dt> <dt>0xA0040801</dt></span><span class="sxs-lookup"><span data-stu-id="2c436-123"><dt>VM\_E\_USING\_ABSOLUTE\_COORDINATES</dt> <dt>0xA0040801</dt></span></span> </dl> | <span data-ttu-id="2c436-124">Положение колесика прокрутки не может быть задано, когда мышь использует абсолютные координаты.</span><span class="sxs-lookup"><span data-stu-id="2c436-124">The scroll wheel position cannot be set when the mouse device is using absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="2c436-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2c436-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                  | <span data-ttu-id="2c436-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2c436-126">An unexpected error has occurred.</span></span><br/>                                                            |



## <a name="requirements"></a><span data-ttu-id="2c436-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2c436-127">Requirements</span></span>



| <span data-ttu-id="2c436-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2c436-128">Requirement</span></span> | <span data-ttu-id="2c436-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2c436-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c436-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c436-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c436-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2c436-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c436-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c436-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c436-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2c436-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2c436-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2c436-134">End of client support</span></span><br/>    | <span data-ttu-id="2c436-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c436-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2c436-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="2c436-136">Product</span></span><br/>                  | <span data-ttu-id="2c436-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2c436-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2c436-138">Header</span><span class="sxs-lookup"><span data-stu-id="2c436-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c436-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c436-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2c436-140">IID</span><span class="sxs-lookup"><span data-stu-id="2c436-140">IID</span></span><br/>                      | <span data-ttu-id="2c436-141">IID \_ ивммаусе определен как ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="2c436-141">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="2c436-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c436-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c436-143">**ивммаусе**</span><span class="sxs-lookup"><span data-stu-id="2c436-143">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

