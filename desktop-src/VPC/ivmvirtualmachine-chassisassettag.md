---
title: Свойство Чассисассеттаг Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Тег ресурса шасси.
ms.assetid: 469816a8-3078-4960-a5e1-79d65b5fc8fc
keywords:
- Чассисассеттаг свойство Virtual PC
- Чассисассеттаг свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Чассисассеттаг
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisAssetTag
- IVMVirtualMachine.get_ChassisAssetTag
- IVMVirtualMachine.put_ChassisAssetTag
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72d02f71907121354c4d937436366548d41f9944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892185"
---
# <a name="ivmvirtualmachinechassisassettag-property"></a><span data-ttu-id="28dee-106">Свойство Ивмвиртуалмачине:: Чассисассеттаг</span><span class="sxs-lookup"><span data-stu-id="28dee-106">IVMVirtualMachine::ChassisAssetTag property</span></span>

<span data-ttu-id="28dee-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="28dee-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="28dee-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="28dee-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="28dee-109">Извлекает и задает тег актива шасси.</span><span class="sxs-lookup"><span data-stu-id="28dee-109">Retrieves and sets the chassis asset tag.</span></span>

<span data-ttu-id="28dee-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="28dee-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="28dee-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28dee-111">Syntax</span></span>


```C++
HRESULT put_ChassisAssetTag(
  [in]          BSTR chassisAssetTag
);

HRESULT get_ChassisAssetTag(
  [out, retval] BSTR *chassisAssetTag
);
```



## <a name="property-value"></a><span data-ttu-id="28dee-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="28dee-112">Property value</span></span>

<span data-ttu-id="28dee-113">Указывает тег актива шасси.</span><span class="sxs-lookup"><span data-stu-id="28dee-113">Specifies the chassis asset tag.</span></span>

## <a name="error-codes"></a><span data-ttu-id="28dee-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="28dee-114">Error codes</span></span>



| <span data-ttu-id="28dee-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="28dee-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="28dee-116">Значение</span><span class="sxs-lookup"><span data-stu-id="28dee-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28dee-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="28dee-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="28dee-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="28dee-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="28dee-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="28dee-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="28dee-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="28dee-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="28dee-121"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="28dee-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="28dee-122">Значение параметра больше 32 символов, пустая строка или недопустимо.</span><span class="sxs-lookup"><span data-stu-id="28dee-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="28dee-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="28dee-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="28dee-124">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="28dee-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="28dee-125"><dt>Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="28dee-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="28dee-126">Виртуальная машина находится в работающем или сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="28dee-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="28dee-127"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="28dee-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="28dee-128">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="28dee-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="28dee-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28dee-129">Remarks</span></span>

<span data-ttu-id="28dee-130">Это свойство не будет содержать действительные сведения до тех пор, пока виртуальная машина не запустится в первый раз.</span><span class="sxs-lookup"><span data-stu-id="28dee-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="28dee-131">При считывании перед начальным запуском будет возвращена пустая строка.</span><span class="sxs-lookup"><span data-stu-id="28dee-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="28dee-132">Требования</span><span class="sxs-lookup"><span data-stu-id="28dee-132">Requirements</span></span>



| <span data-ttu-id="28dee-133">Требование</span><span class="sxs-lookup"><span data-stu-id="28dee-133">Requirement</span></span> | <span data-ttu-id="28dee-134">Значение</span><span class="sxs-lookup"><span data-stu-id="28dee-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="28dee-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28dee-135">Minimum supported client</span></span><br/> | <span data-ttu-id="28dee-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="28dee-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="28dee-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28dee-137">Minimum supported server</span></span><br/> | <span data-ttu-id="28dee-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="28dee-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="28dee-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="28dee-139">End of client support</span></span><br/>    | <span data-ttu-id="28dee-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="28dee-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="28dee-141">Продукт</span><span class="sxs-lookup"><span data-stu-id="28dee-141">Product</span></span><br/>                  | <span data-ttu-id="28dee-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="28dee-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="28dee-143">Header</span><span class="sxs-lookup"><span data-stu-id="28dee-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="28dee-144"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="28dee-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="28dee-145">IID</span><span class="sxs-lookup"><span data-stu-id="28dee-145">IID</span></span><br/>                      | <span data-ttu-id="28dee-146">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="28dee-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="28dee-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28dee-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28dee-148">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="28dee-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

