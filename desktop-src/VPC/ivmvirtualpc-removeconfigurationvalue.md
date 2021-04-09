---
title: Метод Ивмвиртуалпк Ремовеконфигуратионвалуе (Впккоминтерфацес. h)
description: Удаляет значение указанного параметра конфигурации.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- Метод Ремовеконфигуратионвалуе Virtual PC
- Метод Ремовеконфигуратионвалуе Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Ремовеконфигуратионвалуе
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73821657ed7983e2d92fc379c3222f343763b3ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892405"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a><span data-ttu-id="78721-106">Метод Ивмвиртуалпк:: Ремовеконфигуратионвалуе</span><span class="sxs-lookup"><span data-stu-id="78721-106">IVMVirtualPC::RemoveConfigurationValue method</span></span>

<span data-ttu-id="78721-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="78721-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="78721-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="78721-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="78721-109">Удаляет значение указанного параметра конфигурации.</span><span class="sxs-lookup"><span data-stu-id="78721-109">Removes the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="78721-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78721-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a><span data-ttu-id="78721-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="78721-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78721-112">*преференцекэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78721-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78721-113">Ключ, используемый для задания предпочтения, который хранится в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="78721-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78721-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78721-114">Return value</span></span>

<span data-ttu-id="78721-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="78721-115">This method can return one of these values.</span></span>



| <span data-ttu-id="78721-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="78721-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="78721-117">Описание</span><span class="sxs-lookup"><span data-stu-id="78721-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="78721-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="78721-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="78721-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="78721-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="78721-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="78721-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="78721-121">Параметр *преференцекэй* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="78721-121">The *preferenceKey* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="78721-122"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="78721-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="78721-123">Параметр *преференцекэй* недопустим или является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="78721-123">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="78721-124"><dt>**Виртуальная машина \_ E \_ преф \_ не \_ Найдено**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="78721-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl>                   | <span data-ttu-id="78721-125">Предпочтение не найдено.</span><span class="sxs-lookup"><span data-stu-id="78721-125">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="78721-126"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="78721-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="78721-127">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="78721-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="78721-128"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="78721-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="78721-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="78721-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="78721-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78721-130">Remarks</span></span>

<span data-ttu-id="78721-131">Этот метод обеспечивает доступ низкого уровня к любому значению предпочтения для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="78721-131">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="78721-132">Его можно использовать для удаления значений предпочтений для определяемых пользователем ключей.</span><span class="sxs-lookup"><span data-stu-id="78721-132">It can be used to remove preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="78721-133">Требования</span><span class="sxs-lookup"><span data-stu-id="78721-133">Requirements</span></span>



| <span data-ttu-id="78721-134">Требование</span><span class="sxs-lookup"><span data-stu-id="78721-134">Requirement</span></span> | <span data-ttu-id="78721-135">Значение</span><span class="sxs-lookup"><span data-stu-id="78721-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78721-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78721-136">Minimum supported client</span></span><br/> | <span data-ttu-id="78721-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="78721-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78721-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78721-138">Minimum supported server</span></span><br/> | <span data-ttu-id="78721-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="78721-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="78721-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="78721-140">End of client support</span></span><br/>    | <span data-ttu-id="78721-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="78721-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="78721-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="78721-142">Product</span></span><br/>                  | <span data-ttu-id="78721-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="78721-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="78721-144">Header</span><span class="sxs-lookup"><span data-stu-id="78721-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="78721-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="78721-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="78721-146">IID</span><span class="sxs-lookup"><span data-stu-id="78721-146">IID</span></span><br/>                      | <span data-ttu-id="78721-147">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="78721-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="78721-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78721-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78721-149">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="78721-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

