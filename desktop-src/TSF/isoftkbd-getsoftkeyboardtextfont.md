---
title: Метод Исофткбд Жетсофткэйбоардтекстфонт (Софткбдк. h)
description: Метод Исофткбд Жетсофткэйбоардтекстфонт извлекает шрифт текста, используемый программируемой клавиатурой.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Платформа служб текстового ввода метода Жетсофткэйбоардтекстфонт
- Платформа текстовых служб метода Жетсофткэйбоардтекстфонт, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Жетсофткэйбоардтекстфонт
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136946"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a><span data-ttu-id="47893-106">Метод Исофткбд:: Жетсофткэйбоардтекстфонт</span><span class="sxs-lookup"><span data-stu-id="47893-106">ISoftKbd::GetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="47893-107">Метод **исофткбд:: жетсофткэйбоардтекстфонт** извлекает шрифт текста, используемый программируемой клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="47893-107">The **ISoftKbd::GetSoftKeyboardTextFont** method retrieves the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="47893-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47893-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="47893-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="47893-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47893-110">*плогфонт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="47893-110">*pLogFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47893-111">Указатель на буфер, в котором этот метод получает структуру [**логфонтв**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , определяющую шрифт текста для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="47893-111">Pointer to a buffer in which this method retrieves a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47893-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47893-112">Return value</span></span>

<span data-ttu-id="47893-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="47893-113">This method can return one of these values.</span></span>



| <span data-ttu-id="47893-114">Значение</span><span class="sxs-lookup"><span data-stu-id="47893-114">Value</span></span>                                                                                        | <span data-ttu-id="47893-115">Описание</span><span class="sxs-lookup"><span data-stu-id="47893-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="47893-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="47893-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="47893-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="47893-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="47893-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="47893-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="47893-119">Недопустимый параметр *плогфонт* .</span><span class="sxs-lookup"><span data-stu-id="47893-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="47893-120">Требования</span><span class="sxs-lookup"><span data-stu-id="47893-120">Requirements</span></span>



| <span data-ttu-id="47893-121">Требование</span><span class="sxs-lookup"><span data-stu-id="47893-121">Requirement</span></span> | <span data-ttu-id="47893-122">Значение</span><span class="sxs-lookup"><span data-stu-id="47893-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47893-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47893-123">Minimum supported client</span></span><br/> | <span data-ttu-id="47893-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47893-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="47893-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47893-125">Minimum supported server</span></span><br/> | <span data-ttu-id="47893-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47893-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="47893-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="47893-127">Redistributable</span></span><br/>          | <span data-ttu-id="47893-128">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="47893-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="47893-129">Header</span><span class="sxs-lookup"><span data-stu-id="47893-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="47893-130"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="47893-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="47893-131">IDL</span><span class="sxs-lookup"><span data-stu-id="47893-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47893-132"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47893-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="47893-133">DLL</span><span class="sxs-lookup"><span data-stu-id="47893-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47893-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47893-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47893-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47893-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47893-136">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="47893-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="47893-137">**Исофткбд:: Сетсофткэйбоардтекстфонт**</span><span class="sxs-lookup"><span data-stu-id="47893-137">**ISoftKbd::SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

