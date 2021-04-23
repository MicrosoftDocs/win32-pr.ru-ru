---
title: Метод Ивмкэйбоард ТипеасЦиитекст (Впккоминтерфацес. h)
description: Имитирует ряд вводимых в гостевой системе ключей ASCII.
ms.assetid: 6c7fbfed-d495-4f11-a7d1-dc08bd075870
keywords:
- Метод ТипеасЦиитекст Virtual PC
- Метод ТипеасЦиитекст Virtual PC, интерфейс Ивмкэйбоард
- Ивмкэйбоард интерфейс Virtual PC, метод ТипеасЦиитекст
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeAsciiText
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538df9fc3036e43dc36f4ca7425688157e9fca77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136294"
---
# <a name="ivmkeyboardtypeasciitext-method"></a><span data-ttu-id="dd4e4-106">Метод Ивмкэйбоард:: ТипеасЦиитекст</span><span class="sxs-lookup"><span data-stu-id="dd4e4-106">IVMKeyboard::TypeAsciiText method</span></span>

<span data-ttu-id="dd4e4-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dd4e4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dd4e4-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dd4e4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dd4e4-109">Имитирует ряд вводимых в гостевой системе ключей ASCII.</span><span class="sxs-lookup"><span data-stu-id="dd4e4-109">Simulates a series of ASCII keys being typed into the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd4e4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd4e4-110">Syntax</span></span>


```C++
HRESULT TypeAsciiText(
  [in] BSTR text
);
```



## <a name="parameters"></a><span data-ttu-id="dd4e4-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd4e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd4e4-112">*текстовая надпись* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd4e4-112">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd4e4-113">Текстовая строка ASCII, которую необходимо ввести в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="dd4e4-113">The ASCII text string to be typed inside the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd4e4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd4e4-114">Return value</span></span>

<span data-ttu-id="dd4e4-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="dd4e4-115">This method can return one of these values.</span></span>



| <span data-ttu-id="dd4e4-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="dd4e4-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="dd4e4-117">Описание</span><span class="sxs-lookup"><span data-stu-id="dd4e4-117">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dd4e4-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dd4e4-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="dd4e4-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dd4e4-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="dd4e4-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="dd4e4-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="dd4e4-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dd4e4-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="dd4e4-122"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="dd4e4-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="dd4e4-123">Указанная строка пуста.</span><span class="sxs-lookup"><span data-stu-id="dd4e4-123">The specified string is empty.</span></span><br/>    |
| <dl> <span data-ttu-id="dd4e4-124"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="dd4e4-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="dd4e4-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="dd4e4-125">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dd4e4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="dd4e4-126">Requirements</span></span>



| <span data-ttu-id="dd4e4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="dd4e4-127">Requirement</span></span> | <span data-ttu-id="dd4e4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dd4e4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4e4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd4e4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd4e4-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dd4e4-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd4e4-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd4e4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd4e4-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd4e4-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dd4e4-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dd4e4-133">End of client support</span></span><br/>    | <span data-ttu-id="dd4e4-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd4e4-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dd4e4-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="dd4e4-135">Product</span></span><br/>                  | <span data-ttu-id="dd4e4-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dd4e4-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dd4e4-137">Header</span><span class="sxs-lookup"><span data-stu-id="dd4e4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd4e4-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd4e4-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dd4e4-139">IID</span><span class="sxs-lookup"><span data-stu-id="dd4e4-139">IID</span></span><br/>                      | <span data-ttu-id="dd4e4-140">IID \_ ивмкэйбоард определен как 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="dd4e4-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="dd4e4-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd4e4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4e4-142">**ивмкэйбоард**</span><span class="sxs-lookup"><span data-stu-id="dd4e4-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

