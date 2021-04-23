---
title: Свойство Вертикалпоситион Ивммаусе (Впккоминтерфацес. h)
description: Абсолютная координата y мыши.
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- Вертикалпоситион свойство Virtual PC
- Вертикалпоситион свойство Virtual PC, интерфейс Ивммаусе
- Ивммаусе интерфейс Virtual PC, свойство Вертикалпоситион
topic_type:
- apiref
api_name:
- IVMMouse.VerticalPosition
- IVMMouse.get_VerticalPosition
- IVMMouse.put_VerticalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64712f557a3fcd59181e8ce65d835b630da68e48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989305"
---
# <a name="ivmmouseverticalposition-property"></a><span data-ttu-id="e05d3-106">Свойство Ивммаусе:: Вертикалпоситион</span><span class="sxs-lookup"><span data-stu-id="e05d3-106">IVMMouse::VerticalPosition property</span></span>

<span data-ttu-id="e05d3-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e05d3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e05d3-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e05d3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e05d3-109">Получает абсолютную координату y указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="e05d3-109">Retrieves the absolute y-coordinate of the mouse.</span></span>

<span data-ttu-id="e05d3-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e05d3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e05d3-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e05d3-111">Syntax</span></span>


```C++
HRESULT put_VerticalPosition(
  [in]          long position
);

HRESULT get_VerticalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a><span data-ttu-id="e05d3-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e05d3-112">Property value</span></span>

<span data-ttu-id="e05d3-113">Координата y, указывающая новое положение мыши.</span><span class="sxs-lookup"><span data-stu-id="e05d3-113">The y-coordinate indicating the new position of the mouse.</span></span> <span data-ttu-id="e05d3-114">При использовании абсолютных координат это значение указывает новую координату y мыши.</span><span class="sxs-lookup"><span data-stu-id="e05d3-114">When using absolute coordinates, this value specifies the new y-coordinate of the mouse.</span></span> <span data-ttu-id="e05d3-115">При использовании относительных координат это значение указывает количество пикселей, в которое указатель мыши должен перемещаться по оси y.</span><span class="sxs-lookup"><span data-stu-id="e05d3-115">When using relative coordinates, this value specifies the number of pixels the mouse should be moved in the y direction.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e05d3-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e05d3-116">Error codes</span></span>



| <span data-ttu-id="e05d3-117">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="e05d3-117">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="e05d3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e05d3-118">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e05d3-119"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e05d3-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="e05d3-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e05d3-120">The operation was successful.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="e05d3-121"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="e05d3-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="e05d3-122">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e05d3-122">The parameter is **NULL**.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="e05d3-123"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="e05d3-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="e05d3-124">Виртуальная машина, к которой подключено это устройство с мышью, в данный момент не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e05d3-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="e05d3-125"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="e05d3-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="e05d3-126">Необходимо установить компоненты интеграции, чтобы получить положение мыши, или задать положение мыши при использовании абсолютных координат.</span><span class="sxs-lookup"><span data-stu-id="e05d3-126">Integration components must be installed to retrieve the mouse position, or to set the mouse position when using absolute coordinates.</span></span><br/>       |
| <dl> <span data-ttu-id="e05d3-127"><dt>Виртуальная машина \_ E \_ использование \_ относительных \_ координат</dt> <dt>0xA0040802</dt></span><span class="sxs-lookup"><span data-stu-id="e05d3-127"><dt>VM\_E\_USING\_RELATIVE\_COORDINATES</dt> <dt>0xA0040802</dt></span></span> </dl>   | <span data-ttu-id="e05d3-128">Устройство мыши в настоящее время настроено для использования относительных координат мыши.</span><span class="sxs-lookup"><span data-stu-id="e05d3-128">The mouse device is currently set to use relative mouse coordinates.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="e05d3-129"><dt>Виртуальная машина \_ Электронная \_ мышь \_ не \_ активна</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="e05d3-129"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>             | <span data-ttu-id="e05d3-130">Абсолютные координаты не могут быть получены, если устройство мыши не включено или если оно в настоящее время не активно на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e05d3-130">The absolute coordinates cannot be retrieved if the mouse device is not powered up, or if it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="e05d3-131"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e05d3-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="e05d3-132">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e05d3-132">An unexpected error has occurred.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="e05d3-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e05d3-133">Remarks</span></span>

<span data-ttu-id="e05d3-134">Это свойство не может быть получено при использовании относительных координат.</span><span class="sxs-lookup"><span data-stu-id="e05d3-134">This property cannot be retrieved when using relative coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="e05d3-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e05d3-135">Requirements</span></span>



| <span data-ttu-id="e05d3-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e05d3-136">Requirement</span></span> | <span data-ttu-id="e05d3-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e05d3-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e05d3-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e05d3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e05d3-139">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e05d3-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e05d3-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e05d3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e05d3-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e05d3-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e05d3-142">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e05d3-142">End of client support</span></span><br/>    | <span data-ttu-id="e05d3-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e05d3-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e05d3-144">Продукт</span><span class="sxs-lookup"><span data-stu-id="e05d3-144">Product</span></span><br/>                  | <span data-ttu-id="e05d3-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e05d3-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e05d3-146">Header</span><span class="sxs-lookup"><span data-stu-id="e05d3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e05d3-147"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e05d3-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e05d3-148">IID</span><span class="sxs-lookup"><span data-stu-id="e05d3-148">IID</span></span><br/>                      | <span data-ttu-id="e05d3-149">IID \_ ивммаусе определен как ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="e05d3-149">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="e05d3-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e05d3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e05d3-151">**ивммаусе**</span><span class="sxs-lookup"><span data-stu-id="e05d3-151">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

