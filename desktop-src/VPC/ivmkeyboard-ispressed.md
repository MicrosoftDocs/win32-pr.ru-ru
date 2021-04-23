---
title: Метод Ивмкэйбоард (Впккоминтерфацес. h)
description: Определяет, является ли указанный ключ недоступным.
ms.assetid: 7541d678-762a-4c2e-80cd-686bb56c9cd7
keywords:
- Виртуальный ПК с напечатным методом
- Виртуальный ПК, нажимает метод Virtual PC, интерфейс Ивмкэйбоард
- Интерфейс Ивмкэйбоард Virtual PC, метод onPress
topic_type:
- apiref
api_name:
- IVMKeyboard.IsPressed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a4185fa0310994bc1cffa917348dfca2fdedfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803100"
---
# <a name="ivmkeyboardispressed-method"></a><span data-ttu-id="51ffc-106">Метод Ивмкэйбоард:: onPress</span><span class="sxs-lookup"><span data-stu-id="51ffc-106">IVMKeyboard::IsPressed method</span></span>

<span data-ttu-id="51ffc-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="51ffc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="51ffc-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="51ffc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="51ffc-109">Определяет, является ли указанный ключ недоступным.</span><span class="sxs-lookup"><span data-stu-id="51ffc-109">Determines whether the specified key is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ffc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51ffc-110">Syntax</span></span>


```C++
HRESULT IsPressed(
  [in]          BSTR         key,
  [out, retval] VARIANT_BOOL *pressed
);
```



## <a name="parameters"></a><span data-ttu-id="51ffc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="51ffc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ffc-112">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51ffc-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51ffc-113">Код ключа для ключа, состояние которого запрашивается.</span><span class="sxs-lookup"><span data-stu-id="51ffc-113">The key code for the key whose state is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="51ffc-114">*нажато* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="51ffc-114">*pressed* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="51ffc-115">**Значение true** , если клавиша в данный момент нажата; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="51ffc-115">**TRUE** if the key is currently pressed down, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ffc-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51ffc-116">Return value</span></span>

<span data-ttu-id="51ffc-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="51ffc-117">This method can return one of these values.</span></span>



| <span data-ttu-id="51ffc-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="51ffc-118">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="51ffc-119">Описание</span><span class="sxs-lookup"><span data-stu-id="51ffc-119">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="51ffc-120"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="51ffc-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="51ffc-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="51ffc-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="51ffc-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="51ffc-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="51ffc-123">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="51ffc-123">A parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="51ffc-124"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="51ffc-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="51ffc-125">Указанная строка пуста или содержит недопустимый код ключа.</span><span class="sxs-lookup"><span data-stu-id="51ffc-125">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="51ffc-126"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="51ffc-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="51ffc-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="51ffc-127">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="51ffc-128">Требования</span><span class="sxs-lookup"><span data-stu-id="51ffc-128">Requirements</span></span>



| <span data-ttu-id="51ffc-129">Требование</span><span class="sxs-lookup"><span data-stu-id="51ffc-129">Requirement</span></span> | <span data-ttu-id="51ffc-130">Значение</span><span class="sxs-lookup"><span data-stu-id="51ffc-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51ffc-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51ffc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="51ffc-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="51ffc-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51ffc-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51ffc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="51ffc-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="51ffc-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="51ffc-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="51ffc-135">End of client support</span></span><br/>    | <span data-ttu-id="51ffc-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51ffc-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="51ffc-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="51ffc-137">Product</span></span><br/>                  | <span data-ttu-id="51ffc-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="51ffc-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="51ffc-139">Header</span><span class="sxs-lookup"><span data-stu-id="51ffc-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="51ffc-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="51ffc-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="51ffc-141">IID</span><span class="sxs-lookup"><span data-stu-id="51ffc-141">IID</span></span><br/>                      | <span data-ttu-id="51ffc-142">IID \_ ивмкэйбоард определен как 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="51ffc-142">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="51ffc-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51ffc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ffc-144">**ивмкэйбоард**</span><span class="sxs-lookup"><span data-stu-id="51ffc-144">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

