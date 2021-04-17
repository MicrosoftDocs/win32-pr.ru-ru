---
title: Метод Исофткбд Сеткэйбоардлабелтексткомбинатион (Софткбдк. h)
description: Метод Исофткбд Сеткэйбоардлабелтексткомбинатион задает сочетание метки и текста, используемого для описания мягкой клавиатуры.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Платформа служб текстового ввода метода Сеткэйбоардлабелтексткомбинатион
- Платформа текстовых служб метода Сеткэйбоардлабелтексткомбинатион, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Сеткэйбоардлабелтексткомбинатион
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682019"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a><span data-ttu-id="d5f0e-106">Метод Исофткбд:: Сеткэйбоардлабелтексткомбинатион</span><span class="sxs-lookup"><span data-stu-id="d5f0e-106">ISoftKbd::SetKeyboardLabelTextCombination method</span></span>

<span data-ttu-id="d5f0e-107">Метод **исофткбд:: сеткэйбоардлабелтексткомбинатион** задает сочетание метки и текста, используемого для описания мягкой клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="d5f0e-107">The **ISoftKbd::SetKeyboardLabelTextCombination** method sets a combination of label and text used to describe a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f0e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5f0e-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a><span data-ttu-id="d5f0e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5f0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f0e-110">*нмодифиеркомбинатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5f0e-110">*nModifierCombination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f0e-111">Сочетание метки и текста, используемого для описания экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="d5f0e-111">Combination of label and text used to describe the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f0e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5f0e-112">Return value</span></span>

<span data-ttu-id="d5f0e-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d5f0e-113">This method can return one of these values.</span></span>



| <span data-ttu-id="d5f0e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d5f0e-114">Value</span></span>                                                                                        | <span data-ttu-id="d5f0e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d5f0e-115">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="d5f0e-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f0e-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d5f0e-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="d5f0e-117">The method was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="d5f0e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f0e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d5f0e-119">Недопустимый параметр *нмодифиеркомбинатион* .</span><span class="sxs-lookup"><span data-stu-id="d5f0e-119">The *nModifierCombination* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d5f0e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d5f0e-120">Requirements</span></span>



| <span data-ttu-id="d5f0e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d5f0e-121">Requirement</span></span> | <span data-ttu-id="d5f0e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d5f0e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f0e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5f0e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f0e-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d5f0e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d5f0e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5f0e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f0e-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d5f0e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d5f0e-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d5f0e-127">Redistributable</span></span><br/>          | <span data-ttu-id="d5f0e-128">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="d5f0e-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="d5f0e-129">Header</span><span class="sxs-lookup"><span data-stu-id="d5f0e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f0e-130"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f0e-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="d5f0e-131">IDL</span><span class="sxs-lookup"><span data-stu-id="d5f0e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5f0e-132"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5f0e-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="d5f0e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f0e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f0e-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5f0e-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f0e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5f0e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f0e-136">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="d5f0e-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="d5f0e-137">**Исофткбд:: Сеткэйбоардлабелтекст**</span><span class="sxs-lookup"><span data-stu-id="d5f0e-137">**ISoftKbd::SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





