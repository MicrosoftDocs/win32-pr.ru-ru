---
title: Свойство высоты Ивмдисплай (Впккоминтерфацес. h)
description: Высота дисплея виртуальной машины (в пикселях).
ms.assetid: 4fbb7c2b-6d5f-4af6-b8cc-3a7546b15cbd
keywords:
- Свойство высоты Virtual PC
- Свойство высоты Virtual PC, интерфейс Ивмдисплай
- Ивмдисплай интерфейс Virtual PC, свойство Height
topic_type:
- apiref
api_name:
- IVMDisplay.Height
- IVMDisplay.get_Height
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6ff5746c817dcc81b353f80e2daa345b5587fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071696"
---
# <a name="ivmdisplayheight-property"></a><span data-ttu-id="c0153-106">Свойство Ивмдисплай:: Height</span><span class="sxs-lookup"><span data-stu-id="c0153-106">IVMDisplay::Height property</span></span>

<span data-ttu-id="c0153-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c0153-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c0153-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c0153-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c0153-109">Извлекает высоту дисплея виртуальной машины в пикселях.</span><span class="sxs-lookup"><span data-stu-id="c0153-109">Retrieves the height of the virtual machine's display, in pixels.</span></span>

<span data-ttu-id="c0153-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c0153-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0153-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0153-111">Syntax</span></span>


```C++
HRESULT get_Height(
  [out, retval] long *displayPixelHeight
);
```



## <a name="property-value"></a><span data-ttu-id="c0153-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c0153-112">Property value</span></span>

<span data-ttu-id="c0153-113">Высота (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="c0153-113">The height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0153-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c0153-114">Error codes</span></span>



| <span data-ttu-id="c0153-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="c0153-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="c0153-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c0153-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0153-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c0153-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="c0153-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c0153-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c0153-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c0153-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="c0153-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c0153-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c0153-121"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="c0153-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="c0153-122">Для этой операции должна быть запущена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="c0153-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="c0153-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c0153-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="c0153-124">Виртуальная машина является недопустимой или не запущена в данный момент.</span><span class="sxs-lookup"><span data-stu-id="c0153-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="c0153-125"><dt>Виртуальная машина \_ \_Нет \_ отображаемых</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="c0153-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="c0153-126">Не удалось выбрать допустимый дисплей для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0153-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="c0153-127"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c0153-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="c0153-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c0153-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="c0153-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c0153-129">Requirements</span></span>



| <span data-ttu-id="c0153-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c0153-130">Requirement</span></span> | <span data-ttu-id="c0153-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c0153-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0153-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0153-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c0153-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c0153-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0153-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0153-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c0153-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0153-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c0153-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c0153-136">End of client support</span></span><br/>    | <span data-ttu-id="c0153-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0153-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c0153-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="c0153-138">Product</span></span><br/>                  | <span data-ttu-id="c0153-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c0153-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c0153-140">Header</span><span class="sxs-lookup"><span data-stu-id="c0153-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0153-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0153-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c0153-142">IID</span><span class="sxs-lookup"><span data-stu-id="c0153-142">IID</span></span><br/>                      | <span data-ttu-id="c0153-143">IID \_ ивмдисплай определен как 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="c0153-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c0153-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0153-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0153-145">**ивмдисплай**</span><span class="sxs-lookup"><span data-stu-id="c0153-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

