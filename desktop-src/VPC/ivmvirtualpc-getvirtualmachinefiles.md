---
title: Метод Ивмвиртуалпк Жетвиртуалмачинефилес (Впккоминтерфацес. h)
description: Извлекает массив известных файлов конфигурации виртуальной машины.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- Метод Жетвиртуалмачинефилес Virtual PC
- Метод Жетвиртуалмачинефилес Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Жетвиртуалмачинефилес
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d1fe248b76756b39846d181341278f669d2f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341225"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a><span data-ttu-id="54ffb-106">Метод Ивмвиртуалпк:: Жетвиртуалмачинефилес</span><span class="sxs-lookup"><span data-stu-id="54ffb-106">IVMVirtualPC::GetVirtualMachineFiles method</span></span>

<span data-ttu-id="54ffb-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="54ffb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="54ffb-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="54ffb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="54ffb-109">Извлекает массив известных файлов конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="54ffb-109">Retrieves an array of known virtual machine configuration files.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ffb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54ffb-110">Syntax</span></span>


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a><span data-ttu-id="54ffb-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="54ffb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54ffb-112">*инаддитионалсеарчпасс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54ffb-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ffb-113">Эти пути будут искаться вместе с путями, заданными в свойствах [**ивмвиртуалпк:: сеарчпасс**](ivmvirtualpc-searchpaths.md) и [**Ивмвиртуалпк::D ефаултвмконфигуратионпас**](ivmvirtualpc-defaultvmconfigurationpath.md) .</span><span class="sxs-lookup"><span data-stu-id="54ffb-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="54ffb-114">*инексклудедрегистередвмс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54ffb-114">*inExcludedRegisteredVMs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ffb-115">**Значение true** , если зарегистрированные виртуальные машины должны быть исключены из массива, возвращаемого параметром *Аутвиртуалмачинефилелист* , и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="54ffb-115">**TRUE** if registered virtual machines should be excluded from the array return in the *outVirtualMachineFileList* parameter and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="54ffb-116">*аутвиртуалмачинефилелист* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="54ffb-116">*outVirtualMachineFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="54ffb-117">Массив строк пути для файлов конфигурации виртуальной машины, найденных по указанным путям поиска.</span><span class="sxs-lookup"><span data-stu-id="54ffb-117">An array of path strings for the virtual machine configuration files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54ffb-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54ffb-118">Return value</span></span>

<span data-ttu-id="54ffb-119">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="54ffb-119">This method can return one of these values.</span></span>



| <span data-ttu-id="54ffb-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="54ffb-120">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="54ffb-121">Описание</span><span class="sxs-lookup"><span data-stu-id="54ffb-121">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="54ffb-122"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="54ffb-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="54ffb-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="54ffb-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="54ffb-124"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="54ffb-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="54ffb-125">Параметр *аутвиртуалмачинефилелист* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="54ffb-125">The *outVirtualMachineFileList* parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="54ffb-126"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="54ffb-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="54ffb-127">Параметр *инаддитионалсеарчпасс* не является массивом строк.</span><span class="sxs-lookup"><span data-stu-id="54ffb-127">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="54ffb-128"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="54ffb-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="54ffb-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="54ffb-129">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="54ffb-130"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="54ffb-130"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="54ffb-131">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="54ffb-131">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54ffb-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54ffb-132">Remarks</span></span>

<span data-ttu-id="54ffb-133">Пути поиска, используемые для получения массива файлов конфигурации, будут содержать наборы, ранее [**ивмвиртуалпк:: сеарчпасс**](ivmvirtualpc-searchpaths.md) и [**Ивмвиртуалпк::D ефаултвмконфигуратионпас**](ivmvirtualpc-defaultvmconfigurationpath.md) в дополнение к тем, которые указаны параметром *инаддитионалсеарчпасс* .</span><span class="sxs-lookup"><span data-stu-id="54ffb-133">The search paths used to retrieve the array of configuration files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="54ffb-134">Требования</span><span class="sxs-lookup"><span data-stu-id="54ffb-134">Requirements</span></span>



| <span data-ttu-id="54ffb-135">Требование</span><span class="sxs-lookup"><span data-stu-id="54ffb-135">Requirement</span></span> | <span data-ttu-id="54ffb-136">Значение</span><span class="sxs-lookup"><span data-stu-id="54ffb-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="54ffb-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54ffb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="54ffb-138">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="54ffb-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="54ffb-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54ffb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="54ffb-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="54ffb-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="54ffb-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="54ffb-141">End of client support</span></span><br/>    | <span data-ttu-id="54ffb-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="54ffb-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="54ffb-143">Продукт</span><span class="sxs-lookup"><span data-stu-id="54ffb-143">Product</span></span><br/>                  | <span data-ttu-id="54ffb-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="54ffb-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="54ffb-145">Header</span><span class="sxs-lookup"><span data-stu-id="54ffb-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="54ffb-146"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="54ffb-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="54ffb-147">IID</span><span class="sxs-lookup"><span data-stu-id="54ffb-147">IID</span></span><br/>                      | <span data-ttu-id="54ffb-148">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="54ffb-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="54ffb-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54ffb-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ffb-150">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="54ffb-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

