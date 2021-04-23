---
title: Метод Ивмвиртуалпк Жетконфигуратионвалуе (Впккоминтерфацес. h)
description: Получает значение указанного параметра конфигурации.
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Метод Жетконфигуратионвалуе Virtual PC
- Метод Жетконфигуратионвалуе Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Жетконфигуратионвалуе
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11851e2dc2e51c0dc5eed876fc755655ed488554
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136911"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a><span data-ttu-id="8d90c-106">Метод Ивмвиртуалпк:: Жетконфигуратионвалуе</span><span class="sxs-lookup"><span data-stu-id="8d90c-106">IVMVirtualPC::GetConfigurationValue method</span></span>

<span data-ttu-id="8d90c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8d90c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8d90c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8d90c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8d90c-109">Получает значение указанного параметра конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8d90c-109">Retrieves the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d90c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d90c-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="8d90c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d90c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d90c-112">*преференцекэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d90c-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d90c-113">Ключ, используемый для задания предпочтения, который хранится в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8d90c-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="8d90c-114">*преференцевалуе* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8d90c-114">*preferenceValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8d90c-115">Значение предпочтения.</span><span class="sxs-lookup"><span data-stu-id="8d90c-115">The preference value.</span></span> <span data-ttu-id="8d90c-116">Этот параметр может иметь один из следующих **вариантов** : **VT \_ Array** \| **VT \_ UI1** (RAW bytes), **VT \_ BSTR** (String), **VT \_ I4** (целое число) или **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="8d90c-116">This parameter may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d90c-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d90c-117">Return value</span></span>

<span data-ttu-id="8d90c-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="8d90c-118">This method can return one of these values.</span></span>



| <span data-ttu-id="8d90c-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="8d90c-119">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="8d90c-120">Описание</span><span class="sxs-lookup"><span data-stu-id="8d90c-120">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8d90c-121"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8d90c-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="8d90c-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8d90c-122">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="8d90c-123"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="8d90c-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="8d90c-124">Параметр *преференцекэй* или *Преференцевалуе* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8d90c-124">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="8d90c-125"><dt>**Виртуальная машина \_ E \_ преф \_ не \_ Найдено**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="8d90c-125"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xa0040300</dt></span></span> </dl>                   | <span data-ttu-id="8d90c-126">Предпочтение не найдено.</span><span class="sxs-lookup"><span data-stu-id="8d90c-126">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="8d90c-127"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="8d90c-127"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="8d90c-128">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="8d90c-128">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="8d90c-129"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8d90c-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="8d90c-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8d90c-130">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="8d90c-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d90c-131">Remarks</span></span>

<span data-ttu-id="8d90c-132">Этот метод обеспечивает доступ низкого уровня к любому значению предпочтения для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d90c-132">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="8d90c-133">Его можно использовать для получения значений предпочтений для определяемых пользователем ключей.</span><span class="sxs-lookup"><span data-stu-id="8d90c-133">It can be used to retrieve preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d90c-134">Требования</span><span class="sxs-lookup"><span data-stu-id="8d90c-134">Requirements</span></span>



| <span data-ttu-id="8d90c-135">Требование</span><span class="sxs-lookup"><span data-stu-id="8d90c-135">Requirement</span></span> | <span data-ttu-id="8d90c-136">Значение</span><span class="sxs-lookup"><span data-stu-id="8d90c-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d90c-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d90c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8d90c-138">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8d90c-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8d90c-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d90c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8d90c-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8d90c-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8d90c-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8d90c-141">End of client support</span></span><br/>    | <span data-ttu-id="8d90c-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8d90c-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8d90c-143">Продукт</span><span class="sxs-lookup"><span data-stu-id="8d90c-143">Product</span></span><br/>                  | <span data-ttu-id="8d90c-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8d90c-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8d90c-145">Header</span><span class="sxs-lookup"><span data-stu-id="8d90c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d90c-146"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d90c-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8d90c-147">IID</span><span class="sxs-lookup"><span data-stu-id="8d90c-147">IID</span></span><br/>                      | <span data-ttu-id="8d90c-148">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="8d90c-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8d90c-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d90c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d90c-150">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="8d90c-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

