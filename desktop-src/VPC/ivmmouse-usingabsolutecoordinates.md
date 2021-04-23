---
title: Свойство Усингабсолутекурдинатес Ивммаусе (Впккоминтерфацес. h)
description: Возвращает, представляют ли координаты мыши абсолютные или относительные координаты.
ms.assetid: 668278f8-28ae-4128-9653-4985bddbe184
keywords:
- Усингабсолутекурдинатес свойство Virtual PC
- Усингабсолутекурдинатес свойство Virtual PC, интерфейс Ивммаусе
- Ивммаусе интерфейс Virtual PC, свойство Усингабсолутекурдинатес
topic_type:
- apiref
api_name:
- IVMMouse.UsingAbsoluteCoordinates
- IVMMouse.get_UsingAbsoluteCoordinates
- IVMMouse.put_UsingAbsoluteCoordinates
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc216466ab8ef0483d3c1a229f6a493d4ba913dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535099"
---
# <a name="ivmmouseusingabsolutecoordinates-property"></a><span data-ttu-id="b03ba-106">Свойство Ивммаусе:: Усингабсолутекурдинатес</span><span class="sxs-lookup"><span data-stu-id="b03ba-106">IVMMouse::UsingAbsoluteCoordinates property</span></span>

<span data-ttu-id="b03ba-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b03ba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b03ba-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b03ba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b03ba-109">Возвращает, представляют ли координаты мыши абсолютные или относительные координаты.</span><span class="sxs-lookup"><span data-stu-id="b03ba-109">Retrieves whether mouse coordinates represent absolute or relative coordinates.</span></span>

<span data-ttu-id="b03ba-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b03ba-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b03ba-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b03ba-111">Syntax</span></span>


```C++
HRESULT put_UsingAbsoluteCoordinates(
  [in]          VARIANT_BOOL usingAbsoluteCoordinates
);

HRESULT get_UsingAbsoluteCoordinates(
  [out, retval] VARIANT_BOOL *usingAbsoluteCoordinates
);
```



## <a name="property-value"></a><span data-ttu-id="b03ba-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b03ba-112">Property value</span></span>

<span data-ttu-id="b03ba-113">**Вариант \_ Значение TRUE** , чтобы настроить устройство мыши для использования абсолютных координат, **вариант \_ false** — для использования относительных координат.</span><span class="sxs-lookup"><span data-stu-id="b03ba-113">**VARIANT\_TRUE** to set the mouse device to use absolute coordinates, **VARIANT\_FALSE** to use relative coordinates.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b03ba-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b03ba-114">Error codes</span></span>



| <span data-ttu-id="b03ba-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="b03ba-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="b03ba-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b03ba-116">Meaning</span></span>                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b03ba-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b03ba-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="b03ba-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b03ba-118">The operation was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="b03ba-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="b03ba-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="b03ba-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b03ba-120">The parameter is **NULL**.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b03ba-121"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b03ba-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="b03ba-122">Виртуальная машина, к которой подключено это устройство с мышью, в данный момент не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b03ba-122">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                       |
| <dl> <span data-ttu-id="b03ba-123"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="b03ba-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="b03ba-124">Компоненты интеграции не установлены.</span><span class="sxs-lookup"><span data-stu-id="b03ba-124">Integration components are not installed.</span></span> <span data-ttu-id="b03ba-125">Компоненты интеграции необходимы для использования абсолютных координат.</span><span class="sxs-lookup"><span data-stu-id="b03ba-125">Integration components are required to use absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="b03ba-126"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b03ba-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="b03ba-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b03ba-127">An unexpected error has occurred.</span></span><br/>                                                                          |



## <a name="remarks"></a><span data-ttu-id="b03ba-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b03ba-128">Remarks</span></span>

<span data-ttu-id="b03ba-129">Это свойство является локальным только для этого объекта и по умолчанию будет иметь **вариант \_ false** для нового объекта [**ивммаусе**](ivmmouse.md) .</span><span class="sxs-lookup"><span data-stu-id="b03ba-129">This property is local only to this object and will default to **VARIANT\_FALSE** for a new [**IVMMouse**](ivmmouse.md) object.</span></span> <span data-ttu-id="b03ba-130">Обратите внимание, что для использования абсолютных координат необходимо установить компоненты интеграции.</span><span class="sxs-lookup"><span data-stu-id="b03ba-130">Note that integration components must be installed in order to use absolute coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="b03ba-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b03ba-131">Requirements</span></span>



| <span data-ttu-id="b03ba-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b03ba-132">Requirement</span></span> | <span data-ttu-id="b03ba-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b03ba-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b03ba-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b03ba-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b03ba-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b03ba-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b03ba-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b03ba-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b03ba-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b03ba-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b03ba-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b03ba-138">End of client support</span></span><br/>    | <span data-ttu-id="b03ba-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b03ba-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b03ba-140">Продукт</span><span class="sxs-lookup"><span data-stu-id="b03ba-140">Product</span></span><br/>                  | <span data-ttu-id="b03ba-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b03ba-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b03ba-142">Header</span><span class="sxs-lookup"><span data-stu-id="b03ba-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b03ba-143"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b03ba-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b03ba-144">IID</span><span class="sxs-lookup"><span data-stu-id="b03ba-144">IID</span></span><br/>                      | <span data-ttu-id="b03ba-145">IID \_ ивммаусе определен как ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="b03ba-145">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="b03ba-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b03ba-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b03ba-147">**ивммаусе**</span><span class="sxs-lookup"><span data-stu-id="b03ba-147">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

