---
title: Свойство Видеомоде Ивмдисплай (Впккоминтерфацес. h)
description: Извлекает текущий режим видео.
ms.assetid: e5a090c2-f7e6-4b85-8729-64d2ff68fcf3
keywords:
- Видеомоде свойство Virtual PC
- Видеомоде свойство Virtual PC, интерфейс Ивмдисплай
- Ивмдисплай интерфейс Virtual PC, свойство Видеомоде
topic_type:
- apiref
api_name:
- IVMDisplay.VideoMode
- IVMDisplay.get_VideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164a658766cb8973a7c1ac403756ee888abab1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988608"
---
# <a name="ivmdisplayvideomode-property"></a><span data-ttu-id="3a0bf-106">Свойство Ивмдисплай:: Видеомоде</span><span class="sxs-lookup"><span data-stu-id="3a0bf-106">IVMDisplay::VideoMode property</span></span>

<span data-ttu-id="3a0bf-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3a0bf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3a0bf-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3a0bf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3a0bf-109">Извлекает текущий режим видео.</span><span class="sxs-lookup"><span data-stu-id="3a0bf-109">Retrieves the current video mode.</span></span>

<span data-ttu-id="3a0bf-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3a0bf-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0bf-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a0bf-111">Syntax</span></span>


```C++
HRESULT get_VideoMode(
  [out, retval] VMDisplayVideoMode *videoMode
);
```



## <a name="property-value"></a><span data-ttu-id="3a0bf-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3a0bf-112">Property value</span></span>

<span data-ttu-id="3a0bf-113">Текущий режим видео операционной системы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="3a0bf-113">The current video mode of the guest operating system.</span></span> <span data-ttu-id="3a0bf-114">Список значений см. в разделе [**вмдисплайвидеомоде**](vmdisplayvideomode.md).</span><span class="sxs-lookup"><span data-stu-id="3a0bf-114">For a list of values, see [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="3a0bf-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3a0bf-115">Error codes</span></span>



| <span data-ttu-id="3a0bf-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="3a0bf-116">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="3a0bf-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3a0bf-117">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3a0bf-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3a0bf-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="3a0bf-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3a0bf-119">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="3a0bf-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="3a0bf-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="3a0bf-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3a0bf-121">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3a0bf-122"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="3a0bf-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="3a0bf-123">Для этой операции должна быть запущена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="3a0bf-123">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="3a0bf-124"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3a0bf-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="3a0bf-125">Виртуальная машина является недопустимой или не запущена в данный момент.</span><span class="sxs-lookup"><span data-stu-id="3a0bf-125">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="3a0bf-126"><dt>Виртуальная машина \_ \_Нет \_ отображаемых</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="3a0bf-126"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="3a0bf-127">Не удалось выбрать допустимый дисплей для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3a0bf-127">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="3a0bf-128"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3a0bf-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="3a0bf-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3a0bf-129">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="3a0bf-130">Требования</span><span class="sxs-lookup"><span data-stu-id="3a0bf-130">Requirements</span></span>



| <span data-ttu-id="3a0bf-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3a0bf-131">Requirement</span></span> | <span data-ttu-id="3a0bf-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3a0bf-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0bf-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a0bf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3a0bf-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3a0bf-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a0bf-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a0bf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3a0bf-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3a0bf-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3a0bf-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3a0bf-137">End of client support</span></span><br/>    | <span data-ttu-id="3a0bf-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a0bf-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3a0bf-139">Продукт</span><span class="sxs-lookup"><span data-stu-id="3a0bf-139">Product</span></span><br/>                  | <span data-ttu-id="3a0bf-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3a0bf-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3a0bf-141">Header</span><span class="sxs-lookup"><span data-stu-id="3a0bf-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a0bf-142"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a0bf-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3a0bf-143">IID</span><span class="sxs-lookup"><span data-stu-id="3a0bf-143">IID</span></span><br/>                      | <span data-ttu-id="3a0bf-144">IID \_ ивмдисплай определен как 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="3a0bf-144">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3a0bf-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a0bf-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0bf-146">**ивмдисплай**</span><span class="sxs-lookup"><span data-stu-id="3a0bf-146">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

