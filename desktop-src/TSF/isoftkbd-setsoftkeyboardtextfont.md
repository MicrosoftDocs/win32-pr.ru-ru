---
title: Метод Исофткбд Сетсофткэйбоардтекстфонт (Софткбдк. h)
description: Метод Исофткбд Сетсофткэйбоардтекстфонт задает шрифт текста, используемый мягкой клавиатурой.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Платформа служб текстового ввода метода Сетсофткэйбоардтекстфонт
- Платформа текстовых служб метода Сетсофткэйбоардтекстфонт, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Сетсофткэйбоардтекстфонт
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682018"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a><span data-ttu-id="18815-106">Метод Исофткбд:: Сетсофткэйбоардтекстфонт</span><span class="sxs-lookup"><span data-stu-id="18815-106">ISoftKbd::SetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="18815-107">Метод **исофткбд:: сетсофткэйбоардтекстфонт** задает шрифт текста, используемый программируемой клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="18815-107">The **ISoftKbd::SetSoftKeyboardTextFont** method sets the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="18815-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18815-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="18815-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="18815-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18815-110">*плогфонт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18815-110">*pLogFont* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18815-111">Указатель на структуру [**логфонтв**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , определяющую шрифт текста для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="18815-111">Pointer to a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18815-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18815-112">Return value</span></span>

<span data-ttu-id="18815-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="18815-113">This method can return one of these values.</span></span>



| <span data-ttu-id="18815-114">Значение</span><span class="sxs-lookup"><span data-stu-id="18815-114">Value</span></span>                                                                                        | <span data-ttu-id="18815-115">Описание</span><span class="sxs-lookup"><span data-stu-id="18815-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="18815-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="18815-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="18815-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="18815-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="18815-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="18815-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="18815-119">Недопустимый параметр *плогфонт* .</span><span class="sxs-lookup"><span data-stu-id="18815-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18815-120">Требования</span><span class="sxs-lookup"><span data-stu-id="18815-120">Requirements</span></span>



| <span data-ttu-id="18815-121">Требование</span><span class="sxs-lookup"><span data-stu-id="18815-121">Requirement</span></span> | <span data-ttu-id="18815-122">Значение</span><span class="sxs-lookup"><span data-stu-id="18815-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18815-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18815-123">Minimum supported client</span></span><br/> | <span data-ttu-id="18815-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="18815-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="18815-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18815-125">Minimum supported server</span></span><br/> | <span data-ttu-id="18815-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="18815-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="18815-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="18815-127">Redistributable</span></span><br/>          | <span data-ttu-id="18815-128">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="18815-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="18815-129">Header</span><span class="sxs-lookup"><span data-stu-id="18815-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="18815-130"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="18815-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="18815-131">IDL</span><span class="sxs-lookup"><span data-stu-id="18815-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18815-132"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18815-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="18815-133">DLL</span><span class="sxs-lookup"><span data-stu-id="18815-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18815-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18815-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18815-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18815-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18815-136">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="18815-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="18815-137">**Исофткбд:: Жетсофткэйбоардтекстфонт**</span><span class="sxs-lookup"><span data-stu-id="18815-137">**ISoftKbd::GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

