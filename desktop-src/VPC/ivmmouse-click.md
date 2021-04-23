---
title: Метод Ивммаусе Click (Впккоминтерфацес. h)
description: Имитирует нажатие кнопки мыши.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Щелкните метод виртуальный ПК.
- Щелкните метод Virtual PC, интерфейс Ивммаусе
- Интерфейс Ивммаусе Virtual PC, метод Click
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ea1b861db0a92ad92e689770182d225778aee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492891"
---
# <a name="ivmmouseclick-method"></a><span data-ttu-id="b6c75-106">Метод Ивммаусе:: Click</span><span class="sxs-lookup"><span data-stu-id="b6c75-106">IVMMouse::Click method</span></span>

<span data-ttu-id="b6c75-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b6c75-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b6c75-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b6c75-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b6c75-109">Имитирует нажатие кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="b6c75-109">Simulates a mouse button click.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c75-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6c75-110">Syntax</span></span>


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="b6c75-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6c75-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c75-112">*буттониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6c75-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c75-113">Индекс нажатой кнопки.</span><span class="sxs-lookup"><span data-stu-id="b6c75-113">The index of the button being clicked.</span></span> <span data-ttu-id="b6c75-114">Список значений см. в разделе [**вммаусебуттон**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="b6c75-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c75-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6c75-115">Return value</span></span>

<span data-ttu-id="b6c75-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="b6c75-116">This method can return one of these values.</span></span>



| <span data-ttu-id="b6c75-117">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b6c75-117">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="b6c75-118">Описание</span><span class="sxs-lookup"><span data-stu-id="b6c75-118">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6c75-119"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b6c75-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="b6c75-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b6c75-120">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="b6c75-121"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b6c75-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="b6c75-122">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b6c75-122">The parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="b6c75-123"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b6c75-123"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="b6c75-124">Виртуальная машина, к которой подключено это устройство с мышью, в данный момент не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6c75-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="b6c75-125"><dt>**Виртуальная машина \_ Электронная \_ мышь \_ не \_ активна**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="b6c75-125"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="b6c75-126">Не удалось выполнить операцию, так как устройство мыши не включено или сейчас не активно на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b6c75-126">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="b6c75-127"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b6c75-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="b6c75-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b6c75-128">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="b6c75-129">Требования</span><span class="sxs-lookup"><span data-stu-id="b6c75-129">Requirements</span></span>



| <span data-ttu-id="b6c75-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b6c75-130">Requirement</span></span> | <span data-ttu-id="b6c75-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b6c75-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c75-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6c75-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c75-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b6c75-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b6c75-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6c75-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c75-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b6c75-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b6c75-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b6c75-136">End of client support</span></span><br/>    | <span data-ttu-id="b6c75-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b6c75-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b6c75-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="b6c75-138">Product</span></span><br/>                  | <span data-ttu-id="b6c75-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b6c75-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b6c75-140">Header</span><span class="sxs-lookup"><span data-stu-id="b6c75-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6c75-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c75-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b6c75-142">IID</span><span class="sxs-lookup"><span data-stu-id="b6c75-142">IID</span></span><br/>                      | <span data-ttu-id="b6c75-143">IID \_ ивммаусе определен как ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="b6c75-143">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="b6c75-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6c75-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c75-145">**ивммаусе**</span><span class="sxs-lookup"><span data-stu-id="b6c75-145">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

