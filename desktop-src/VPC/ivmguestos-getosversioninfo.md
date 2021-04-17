---
title: Метод Ивмгуестос Жетосверсионинфо (Впккоминтерфацес. h)
description: Извлекает сведения о версии гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Метод Жетосверсионинфо Virtual PC
- Метод Жетосверсионинфо Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, метод Жетосверсионинфо
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672857"
---
# <a name="ivmguestosgetosversioninfo-method"></a><span data-ttu-id="f2f8f-106">Метод Ивмгуестос:: Жетосверсионинфо</span><span class="sxs-lookup"><span data-stu-id="f2f8f-106">IVMGuestOS::GetOsVersionInfo method</span></span>

<span data-ttu-id="f2f8f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f2f8f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f2f8f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f2f8f-109">Извлекает сведения о версии гостевой операционной системы, работающей на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-109">Retrieves version information for the guest operating system running in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2f8f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2f8f-110">Syntax</span></span>


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f2f8f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2f8f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2f8f-112">*гуестосверсионинфо* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f2f8f-112">*guestOsVersionInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f8f-113">Указатель на структуру [**гуестосверсионинфоекс**](guestosversioninfoex.md) .</span><span class="sxs-lookup"><span data-stu-id="f2f8f-113">A pointer to a [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2f8f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2f8f-114">Return value</span></span>

<span data-ttu-id="f2f8f-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f2f8f-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="f2f8f-116">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f2f8f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f2f8f-117">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2f8f-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f2f8f-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="f2f8f-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f2f8f-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="f2f8f-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="f2f8f-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f2f8f-122"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (Error \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="f2f8f-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="f2f8f-123">Недостаточно памяти для выполнения этого запроса.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-123">There is not enough memory available to complete this request.</span></span><br/> |
| <dl> <span data-ttu-id="f2f8f-124"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f2f8f-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="f2f8f-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-125">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="f2f8f-126"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="f2f8f-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="f2f8f-127">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-127">The VM is not running.</span></span><br/>                                         |
| <dl> <span data-ttu-id="f2f8f-128"><dt>**Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_**</dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="f2f8f-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="f2f8f-129">Компоненты интеграции не установлены в этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-129">Integration components are not installed in this VM.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="f2f8f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="f2f8f-130">Requirements</span></span>



| <span data-ttu-id="f2f8f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="f2f8f-131">Requirement</span></span> | <span data-ttu-id="f2f8f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f2f8f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f8f-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2f8f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f8f-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f2f8f-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2f8f-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2f8f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f8f-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f2f8f-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f2f8f-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f2f8f-137">End of client support</span></span><br/>    | <span data-ttu-id="f2f8f-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2f8f-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f2f8f-139">Продукт</span><span class="sxs-lookup"><span data-stu-id="f2f8f-139">Product</span></span><br/>                  | <span data-ttu-id="f2f8f-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f2f8f-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f2f8f-141">Header</span><span class="sxs-lookup"><span data-stu-id="f2f8f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2f8f-142"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f8f-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f2f8f-143">IID</span><span class="sxs-lookup"><span data-stu-id="f2f8f-143">IID</span></span><br/>                      | <span data-ttu-id="f2f8f-144">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="f2f8f-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f2f8f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2f8f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f8f-146">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="f2f8f-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

