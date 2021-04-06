---
title: Метод Исофткбд Сеткэйбоардлабелтекст (Софткбдк. h)
description: Метод Исофткбд Сеткэйбоардлабелтекст задает текст метки из макета для экранной клавиатуры.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Платформа служб текстового ввода метода Сеткэйбоардлабелтекст
- Платформа текстовых служб метода Сеткэйбоардлабелтекст, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Сеткэйбоардлабелтекст
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803244"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a><span data-ttu-id="39f29-106">Метод Исофткбд:: Сеткэйбоардлабелтекст</span><span class="sxs-lookup"><span data-stu-id="39f29-106">ISoftKbd::SetKeyboardLabelText method</span></span>

<span data-ttu-id="39f29-107">Метод **исофткбд:: сеткэйбоардлабелтекст** задает текст метки из макета для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="39f29-107">The **ISoftKbd::SetKeyboardLabelText** method sets the label text from the layout for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f29-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39f29-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a><span data-ttu-id="39f29-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="39f29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39f29-110">*hKl* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39f29-110">*hKl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39f29-111">Маркер, используемый для получения установленного макета для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="39f29-111">Handle that is used to retrieve the installed layout for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39f29-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39f29-112">Return value</span></span>

<span data-ttu-id="39f29-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="39f29-113">This method can return one of these values.</span></span>



| <span data-ttu-id="39f29-114">Значение</span><span class="sxs-lookup"><span data-stu-id="39f29-114">Value</span></span>                                                                                        | <span data-ttu-id="39f29-115">Описание</span><span class="sxs-lookup"><span data-stu-id="39f29-115">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="39f29-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="39f29-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="39f29-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="39f29-117">The method was successful.</span></span><br/>      |
| <dl> <span data-ttu-id="39f29-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="39f29-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="39f29-119">Недопустимый параметр *hKl* .</span><span class="sxs-lookup"><span data-stu-id="39f29-119">The *hKl* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="39f29-120">Требования</span><span class="sxs-lookup"><span data-stu-id="39f29-120">Requirements</span></span>



| <span data-ttu-id="39f29-121">Требование</span><span class="sxs-lookup"><span data-stu-id="39f29-121">Requirement</span></span> | <span data-ttu-id="39f29-122">Значение</span><span class="sxs-lookup"><span data-stu-id="39f29-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39f29-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39f29-123">Minimum supported client</span></span><br/> | <span data-ttu-id="39f29-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39f29-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39f29-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39f29-125">Minimum supported server</span></span><br/> | <span data-ttu-id="39f29-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39f29-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="39f29-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="39f29-127">Redistributable</span></span><br/>          | <span data-ttu-id="39f29-128">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="39f29-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="39f29-129">Header</span><span class="sxs-lookup"><span data-stu-id="39f29-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="39f29-130"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="39f29-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="39f29-131">IDL</span><span class="sxs-lookup"><span data-stu-id="39f29-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39f29-132"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39f29-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="39f29-133">DLL</span><span class="sxs-lookup"><span data-stu-id="39f29-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39f29-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39f29-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f29-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39f29-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f29-136">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="39f29-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="39f29-137">**Исофткбд:: Сеткэйбоардлабелтексткомбинатион**</span><span class="sxs-lookup"><span data-stu-id="39f29-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





