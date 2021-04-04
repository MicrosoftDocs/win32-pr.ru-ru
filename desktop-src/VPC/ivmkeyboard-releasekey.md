---
title: Метод Ивмкэйбоард Релеасекэй (Впккоминтерфацес. h)
description: Имитирует освобождение ключа.
ms.assetid: 112bf11d-d768-4487-ab41-e915aa4e6a24
keywords:
- Метод Релеасекэй Virtual PC
- Метод Релеасекэй Virtual PC, интерфейс Ивмкэйбоард
- Ивмкэйбоард интерфейс Virtual PC, метод Релеасекэй
topic_type:
- apiref
api_name:
- IVMKeyboard.ReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8585f592ae1cad65157536f841500c42bb06bfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988847"
---
# <a name="ivmkeyboardreleasekey-method"></a><span data-ttu-id="3fbbd-106">Метод Ивмкэйбоард:: Релеасекэй</span><span class="sxs-lookup"><span data-stu-id="3fbbd-106">IVMKeyboard::ReleaseKey method</span></span>

<span data-ttu-id="3fbbd-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3fbbd-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3fbbd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3fbbd-109">Имитирует освобождение ключа.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-109">Simulates a key being released.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fbbd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fbbd-110">Syntax</span></span>


```C++
HRESULT ReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="3fbbd-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fbbd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fbbd-112">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3fbbd-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fbbd-113">Код ключа для освобождения ключа.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-113">The key code for the key to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fbbd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3fbbd-114">Return value</span></span>

<span data-ttu-id="3fbbd-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-115">This method can return one of these values.</span></span>



| <span data-ttu-id="3fbbd-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="3fbbd-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="3fbbd-117">Описание</span><span class="sxs-lookup"><span data-stu-id="3fbbd-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3fbbd-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3fbbd-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3fbbd-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3fbbd-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="3fbbd-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3fbbd-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="3fbbd-122"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3fbbd-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="3fbbd-123">Указанная строка пуста или содержит недопустимый код ключа.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="3fbbd-124"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3fbbd-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3fbbd-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="3fbbd-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3fbbd-126">Requirements</span></span>



| <span data-ttu-id="3fbbd-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3fbbd-127">Requirement</span></span> | <span data-ttu-id="3fbbd-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3fbbd-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbbd-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fbbd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3fbbd-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3fbbd-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fbbd-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fbbd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3fbbd-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3fbbd-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3fbbd-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3fbbd-133">End of client support</span></span><br/>    | <span data-ttu-id="3fbbd-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3fbbd-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3fbbd-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="3fbbd-135">Product</span></span><br/>                  | <span data-ttu-id="3fbbd-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3fbbd-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3fbbd-137">Header</span><span class="sxs-lookup"><span data-stu-id="3fbbd-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fbbd-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fbbd-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3fbbd-139">IID</span><span class="sxs-lookup"><span data-stu-id="3fbbd-139">IID</span></span><br/>                      | <span data-ttu-id="3fbbd-140">IID \_ ивмкэйбоард определен как 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="3fbbd-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3fbbd-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fbbd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbbd-142">**ивмкэйбоард**</span><span class="sxs-lookup"><span data-stu-id="3fbbd-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

