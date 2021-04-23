---
title: Метод Ивмкэйбоард Прессандрелеасекэй (Впккоминтерфацес. h)
description: Имитирует нажатое клавиша, а затем освобождается.
ms.assetid: 2a7fc36f-f1bf-4f1d-b8f7-ea5b167c82a7
keywords:
- Метод Прессандрелеасекэй Virtual PC
- Метод Прессандрелеасекэй Virtual PC, интерфейс Ивмкэйбоард
- Ивмкэйбоард интерфейс Virtual PC, метод Прессандрелеасекэй
topic_type:
- apiref
api_name:
- IVMKeyboard.PressAndReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4adbcac2c79c02ce69584bbfdf21a6b08b350a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691867"
---
# <a name="ivmkeyboardpressandreleasekey-method"></a><span data-ttu-id="f4016-106">Ивмкэйбоард: метод:P Рессандрелеасекэй</span><span class="sxs-lookup"><span data-stu-id="f4016-106">IVMKeyboard::PressAndReleaseKey method</span></span>

<span data-ttu-id="f4016-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f4016-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f4016-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f4016-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f4016-109">Имитирует нажатое клавиша, а затем освобождается.</span><span class="sxs-lookup"><span data-stu-id="f4016-109">Simulates a key being pressed down and then released.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4016-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4016-110">Syntax</span></span>


```C++
HRESULT PressAndReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="f4016-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4016-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4016-112">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4016-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4016-113">Код ключа для нажатия и освобождения ключа.</span><span class="sxs-lookup"><span data-stu-id="f4016-113">The key code for the key to be pressed and released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4016-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4016-114">Return value</span></span>

<span data-ttu-id="f4016-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f4016-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f4016-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="f4016-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="f4016-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f4016-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f4016-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4016-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f4016-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f4016-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f4016-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="f4016-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f4016-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f4016-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="f4016-122"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f4016-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="f4016-123">Указанная строка пуста или содержит недопустимый код ключа.</span><span class="sxs-lookup"><span data-stu-id="f4016-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="f4016-124"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f4016-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f4016-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f4016-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="f4016-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f4016-126">Requirements</span></span>



| <span data-ttu-id="f4016-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f4016-127">Requirement</span></span> | <span data-ttu-id="f4016-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f4016-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4016-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4016-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f4016-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f4016-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4016-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4016-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f4016-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f4016-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f4016-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f4016-133">End of client support</span></span><br/>    | <span data-ttu-id="f4016-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4016-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f4016-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="f4016-135">Product</span></span><br/>                  | <span data-ttu-id="f4016-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f4016-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f4016-137">Header</span><span class="sxs-lookup"><span data-stu-id="f4016-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4016-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4016-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f4016-139">IID</span><span class="sxs-lookup"><span data-stu-id="f4016-139">IID</span></span><br/>                      | <span data-ttu-id="f4016-140">IID \_ ивмкэйбоард определен как 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="f4016-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f4016-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4016-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4016-142">**ивмкэйбоард**</span><span class="sxs-lookup"><span data-stu-id="f4016-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

