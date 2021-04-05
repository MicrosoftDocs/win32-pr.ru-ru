---
title: Метод Ивмкэйбоард Типекэйсекуенце (Впккоминтерфацес. h)
description: Имитирует разделенный запятыми список вводимых ключей.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- Метод Типекэйсекуенце Virtual PC
- Метод Типекэйсекуенце Virtual PC, интерфейс Ивмкэйбоард
- Ивмкэйбоард интерфейс Virtual PC, метод Типекэйсекуенце
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989309"
---
# <a name="ivmkeyboardtypekeysequence-method"></a><span data-ttu-id="b5b7c-106">Метод Ивмкэйбоард:: Типекэйсекуенце</span><span class="sxs-lookup"><span data-stu-id="b5b7c-106">IVMKeyboard::TypeKeySequence method</span></span>

<span data-ttu-id="b5b7c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b5b7c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b5b7c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b5b7c-109">Имитирует разделенный запятыми список вводимых ключей.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-109">Simulates a comma-delimited list of keys being typed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b7c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5b7c-110">Syntax</span></span>


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a><span data-ttu-id="b5b7c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5b7c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5b7c-112">*кэйсекуенце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5b7c-112">*keySequence* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5b7c-113">Разделенная запятыми последовательность кодов клавиш для ввода.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-113">The comma-delimited sequence of key codes to be typed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5b7c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5b7c-114">Return value</span></span>

<span data-ttu-id="b5b7c-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b5b7c-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b5b7c-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="b5b7c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b5b7c-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5b7c-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b5b7c-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b5b7c-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b5b7c-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="b5b7c-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b5b7c-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="b5b7c-122"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b5b7c-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="b5b7c-123">Указанная строка пуста или содержит недопустимый код ключа.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="b5b7c-124"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b5b7c-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b5b7c-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="b5b7c-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5b7c-126">Remarks</span></span>

<span data-ttu-id="b5b7c-127">Строка ключевой последовательности — это разделенный запятыми набор идентификаторов ключей, которые используются для имитации последовательности нажатия и выпуска стандартной клавиатуры с 101-ключом в стиле «английский (США)».</span><span class="sxs-lookup"><span data-stu-id="b5b7c-127">A key sequence string is a comma-delimited set of key identifiers which are used to simulate the key press and release sequence of a standard U.S. 101-key AT-style keyboard.</span></span>

<span data-ttu-id="b5b7c-128">Если идентификатор ключа отображается в строке без предшествующего модификатора, в сеансе виртуальной машины отправляется код нажатия клавиши, после чего сразу же возвращается соответствующий код.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-128">If a key identifier appears in the string without a preceding modifier, a key-pressed code is sent to the virtual machine session, followed immediately by its corresponding key-released code.</span></span> <span data-ttu-id="b5b7c-129">Для изменения этого поведения можно использовать модификаторы ключа.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-129">Key modifiers can be used to change this behavior.</span></span>

<span data-ttu-id="b5b7c-130">Например, модификатор DOWN отправит код нажатия клавиши для следующего идентификатора ключа, не отправляя код, освобожденный с помощью ключа.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-130">For example, the DOWN modifier will send the key-pressed code for the following key identifier without sending the key-released code.</span></span> <span data-ttu-id="b5b7c-131">Это полезно для имитации клавиш CTRL, Alt и Shift, когда они сохраняются во время отправки других ключей.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-131">This is useful for simulating Ctrl, Alt, and Shift keys when they are held down while other keys are being sent.</span></span> <span data-ttu-id="b5b7c-132">Чтобы освободить ключ, его необходимо снова добавить в строку ключа вместе с предыдущим модификатором UP.</span><span class="sxs-lookup"><span data-stu-id="b5b7c-132">To release the key, it must be included in the key string again along with a preceding UP modifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5b7c-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b5b7c-133">Requirements</span></span>



| <span data-ttu-id="b5b7c-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b5b7c-134">Requirement</span></span> | <span data-ttu-id="b5b7c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b5b7c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b7c-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5b7c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b5b7c-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b5b7c-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5b7c-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5b7c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b5b7c-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b5b7c-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b5b7c-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b5b7c-140">End of client support</span></span><br/>    | <span data-ttu-id="b5b7c-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b5b7c-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b5b7c-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="b5b7c-142">Product</span></span><br/>                  | <span data-ttu-id="b5b7c-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b5b7c-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b5b7c-144">Header</span><span class="sxs-lookup"><span data-stu-id="b5b7c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5b7c-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5b7c-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b5b7c-146">IID</span><span class="sxs-lookup"><span data-stu-id="b5b7c-146">IID</span></span><br/>                      | <span data-ttu-id="b5b7c-147">IID \_ ивмкэйбоард определен как 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="b5b7c-147">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b5b7c-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5b7c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b7c-149">**ивмкэйбоард**</span><span class="sxs-lookup"><span data-stu-id="b5b7c-149">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> <dt>

[<span data-ttu-id="b5b7c-150">Последовательности ключей</span><span class="sxs-lookup"><span data-stu-id="b5b7c-150">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

