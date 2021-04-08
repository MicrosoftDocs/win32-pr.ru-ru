---
title: Свойство БИОСГУИД Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Идентификатор GUID BIOS.
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- БИОСГУИД свойство Virtual PC
- БИОСГУИД свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство БИОСГУИД
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891862"
---
# <a name="ivmvirtualmachinebiosguid-property"></a><span data-ttu-id="98296-106">Свойство Ивмвиртуалмачине:: БИОСГУИД</span><span class="sxs-lookup"><span data-stu-id="98296-106">IVMVirtualMachine::BIOSGUID property</span></span>

<span data-ttu-id="98296-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="98296-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="98296-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="98296-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="98296-109">Извлекает и устанавливает GUID BIOS.</span><span class="sxs-lookup"><span data-stu-id="98296-109">Retrieves and sets the BIOS GUID.</span></span>

<span data-ttu-id="98296-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="98296-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="98296-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98296-111">Syntax</span></span>


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a><span data-ttu-id="98296-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="98296-112">Property value</span></span>

<span data-ttu-id="98296-113">Указывает GUID BIOS.</span><span class="sxs-lookup"><span data-stu-id="98296-113">Specifies the BIOS GUID.</span></span> <span data-ttu-id="98296-114">Включить левые и правые фигурные скобки вокруг шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="98296-114">Include left and right braces around the hex digits.</span></span>

## <a name="error-codes"></a><span data-ttu-id="98296-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="98296-115">Error codes</span></span>



| <span data-ttu-id="98296-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="98296-116">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="98296-117">Значение</span><span class="sxs-lookup"><span data-stu-id="98296-117">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="98296-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="98296-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="98296-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="98296-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="98296-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="98296-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="98296-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="98296-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="98296-122"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="98296-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="98296-123">Параметр недопустим или является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="98296-123">The parameter is not valid or is an empty string.</span></span><br/>   |
| <dl> <span data-ttu-id="98296-124"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="98296-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="98296-125">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="98296-125">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="98296-126"><dt>Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="98296-126"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="98296-127">Виртуальная машина находится в работающем или сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="98296-127">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="98296-128"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="98296-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="98296-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="98296-129">An unexpected error has occurred.</span></span><br/>                   |



## <a name="remarks"></a><span data-ttu-id="98296-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98296-130">Remarks</span></span>

<span data-ttu-id="98296-131">Это свойство не будет содержать действительные сведения до тех пор, пока виртуальная машина не запустится в первый раз.</span><span class="sxs-lookup"><span data-stu-id="98296-131">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="98296-132">При считывании перед начальным запуском будет возвращена пустая строка.</span><span class="sxs-lookup"><span data-stu-id="98296-132">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="98296-133">Требования</span><span class="sxs-lookup"><span data-stu-id="98296-133">Requirements</span></span>



| <span data-ttu-id="98296-134">Требование</span><span class="sxs-lookup"><span data-stu-id="98296-134">Requirement</span></span> | <span data-ttu-id="98296-135">Значение</span><span class="sxs-lookup"><span data-stu-id="98296-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="98296-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98296-136">Minimum supported client</span></span><br/> | <span data-ttu-id="98296-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="98296-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98296-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98296-138">Minimum supported server</span></span><br/> | <span data-ttu-id="98296-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="98296-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="98296-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="98296-140">End of client support</span></span><br/>    | <span data-ttu-id="98296-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="98296-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="98296-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="98296-142">Product</span></span><br/>                  | <span data-ttu-id="98296-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="98296-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="98296-144">Header</span><span class="sxs-lookup"><span data-stu-id="98296-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="98296-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="98296-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="98296-146">IID</span><span class="sxs-lookup"><span data-stu-id="98296-146">IID</span></span><br/>                      | <span data-ttu-id="98296-147">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="98296-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="98296-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98296-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98296-149">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="98296-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

