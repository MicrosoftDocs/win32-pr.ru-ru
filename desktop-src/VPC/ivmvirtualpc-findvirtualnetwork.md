---
title: Метод Ивмвиртуалпк Финдвиртуалнетворк (Впккоминтерфацес. h)
description: Извлекает объект виртуальной сети, соответствующий запрошенному имени.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- Метод Финдвиртуалнетворк Virtual PC
- Метод Финдвиртуалнетворк Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Финдвиртуалнетворк
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59306d2e2022c1323ab52f1a47bd386347f504e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534856"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a><span data-ttu-id="ad875-106">Метод Ивмвиртуалпк:: Финдвиртуалнетворк</span><span class="sxs-lookup"><span data-stu-id="ad875-106">IVMVirtualPC::FindVirtualNetwork method</span></span>

<span data-ttu-id="ad875-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ad875-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ad875-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ad875-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ad875-109">Извлекает объект виртуальной сети, соответствующий запрошенному имени.</span><span class="sxs-lookup"><span data-stu-id="ad875-109">Retrieves a virtual network object that matches the requested name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad875-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad875-110">Syntax</span></span>


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="ad875-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad875-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad875-112">*virtualNetworkName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad875-112">*virtualNetworkName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad875-113">Имя искомой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ad875-113">The name of the virtual network to find.</span></span>

</dd> <dt>

<span data-ttu-id="ad875-114">*virtualNetwork* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ad875-114">*virtualNetwork* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ad875-115">Указатель на новый объект [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) , представляющий эту виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="ad875-115">A pointer to a new [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that represents this virtual network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad875-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad875-116">Return value</span></span>

<span data-ttu-id="ad875-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="ad875-117">This method can return one of these values.</span></span>



| <span data-ttu-id="ad875-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="ad875-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="ad875-119">Описание</span><span class="sxs-lookup"><span data-stu-id="ad875-119">Description</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad875-120"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ad875-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="ad875-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ad875-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ad875-122"><dt>**С \_ ЛОЖЬ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ad875-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="ad875-123">Не удалось найти указанную виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="ad875-123">The specified virtual network could not be found.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ad875-124"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="ad875-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="ad875-125">Параметр *virtualNetwork* имеет **значение NULL** , или виртуальная сеть не найдена.</span><span class="sxs-lookup"><span data-stu-id="ad875-125">The *virtualNetwork* parameter is **NULL** or the virtual network cannot be found.</span></span><br/>   |
| <dl> <span data-ttu-id="ad875-126"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ad875-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="ad875-127">Параметр *virtualNetworkName* недопустим или является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="ad875-127">The *virtualNetworkName* parameter is not valid or is an empty string.</span></span><br/>               |
| <dl> <span data-ttu-id="ad875-128"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="ad875-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="ad875-129">Не удалось найти файл виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ad875-129">The virtual network file could not be found.</span></span><br/>                                         |
| <dl> <span data-ttu-id="ad875-130"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ad875-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="ad875-131">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ad875-131">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="ad875-132"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="ad875-132"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="ad875-133">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="ad875-133">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ad875-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad875-134">Remarks</span></span>

<span data-ttu-id="ad875-135">Имена виртуальных сетей не учитывают регистр, например "Минетворк" и "минетворк" ссылаются на одну и ту же виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="ad875-135">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad875-136">Требования</span><span class="sxs-lookup"><span data-stu-id="ad875-136">Requirements</span></span>



| <span data-ttu-id="ad875-137">Требование</span><span class="sxs-lookup"><span data-stu-id="ad875-137">Requirement</span></span> | <span data-ttu-id="ad875-138">Значение</span><span class="sxs-lookup"><span data-stu-id="ad875-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad875-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad875-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ad875-140">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ad875-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad875-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad875-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ad875-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ad875-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ad875-143">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ad875-143">End of client support</span></span><br/>    | <span data-ttu-id="ad875-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad875-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ad875-145">Продукт</span><span class="sxs-lookup"><span data-stu-id="ad875-145">Product</span></span><br/>                  | <span data-ttu-id="ad875-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ad875-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ad875-147">Header</span><span class="sxs-lookup"><span data-stu-id="ad875-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad875-148"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad875-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ad875-149">IID</span><span class="sxs-lookup"><span data-stu-id="ad875-149">IID</span></span><br/>                      | <span data-ttu-id="ad875-150">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="ad875-150">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ad875-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad875-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad875-152">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="ad875-152">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

