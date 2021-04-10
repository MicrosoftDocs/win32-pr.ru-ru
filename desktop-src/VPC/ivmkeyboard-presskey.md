---
title: Метод Ивмкэйбоард Пресскэй (Впккоминтерфацес. h)
description: Имитирует нажатой клавиша.
ms.assetid: d945128a-ffde-465c-b615-83a1d5dc789f
keywords:
- Метод Пресскэй Virtual PC
- Метод Пресскэй Virtual PC, интерфейс Ивмкэйбоард
- Ивмкэйбоард интерфейс Virtual PC, метод Пресскэй
topic_type:
- apiref
api_name:
- IVMKeyboard.PressKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8175447a819afa7f761899a7e0dd3cbbcc780631
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071756"
---
# <a name="ivmkeyboardpresskey-method"></a><span data-ttu-id="62221-106">Ивмкэйбоард: метод:P Ресскэй</span><span class="sxs-lookup"><span data-stu-id="62221-106">IVMKeyboard::PressKey method</span></span>

<span data-ttu-id="62221-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="62221-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="62221-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="62221-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="62221-109">Имитирует нажатой клавиша.</span><span class="sxs-lookup"><span data-stu-id="62221-109">Simulates a key being pressed down.</span></span>

## <a name="syntax"></a><span data-ttu-id="62221-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62221-110">Syntax</span></span>


```C++
HRESULT PressKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="62221-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="62221-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62221-112">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62221-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62221-113">Код ключа для нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="62221-113">The key code for the key to be pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62221-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62221-114">Return value</span></span>

<span data-ttu-id="62221-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="62221-115">This method can return one of these values.</span></span>



| <span data-ttu-id="62221-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="62221-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="62221-117">Описание</span><span class="sxs-lookup"><span data-stu-id="62221-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62221-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="62221-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="62221-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="62221-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="62221-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="62221-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="62221-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="62221-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="62221-122"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="62221-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="62221-123">Указанная строка пуста или содержит недопустимый код ключа.</span><span class="sxs-lookup"><span data-stu-id="62221-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="62221-124"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="62221-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="62221-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="62221-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="62221-126">Требования</span><span class="sxs-lookup"><span data-stu-id="62221-126">Requirements</span></span>



| <span data-ttu-id="62221-127">Требование</span><span class="sxs-lookup"><span data-stu-id="62221-127">Requirement</span></span> | <span data-ttu-id="62221-128">Значение</span><span class="sxs-lookup"><span data-stu-id="62221-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="62221-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62221-129">Minimum supported client</span></span><br/> | <span data-ttu-id="62221-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="62221-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62221-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62221-131">Minimum supported server</span></span><br/> | <span data-ttu-id="62221-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="62221-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="62221-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="62221-133">End of client support</span></span><br/>    | <span data-ttu-id="62221-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="62221-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="62221-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="62221-135">Product</span></span><br/>                  | <span data-ttu-id="62221-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="62221-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="62221-137">Header</span><span class="sxs-lookup"><span data-stu-id="62221-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="62221-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="62221-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="62221-139">IID</span><span class="sxs-lookup"><span data-stu-id="62221-139">IID</span></span><br/>                      | <span data-ttu-id="62221-140">IID \_ ивмкэйбоард определен как 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="62221-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="62221-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62221-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62221-142">**ивмкэйбоард**</span><span class="sxs-lookup"><span data-stu-id="62221-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

