---
title: Метод Исофткбд Сетсофткэйбоардколорс (Софткбдк. h)
description: Метод Исофткбд Сетсофткэйбоардколорс задает цвет экранной клавиатуры для указанного типа цвета.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Платформа служб текстового ввода метода Сетсофткэйбоардколорс
- Платформа текстовых служб метода Сетсофткэйбоардколорс, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Сетсофткэйбоардколорс
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38357331db2440c35ca7557d08c97729fde9c9f0
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "105684716"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a><span data-ttu-id="530cf-106">Метод Исофткбд:: Сетсофткэйбоардколорс</span><span class="sxs-lookup"><span data-stu-id="530cf-106">ISoftKbd::SetSoftKeyboardColors method</span></span>

<span data-ttu-id="530cf-107">Метод **исофткбд:: сетсофткэйбоардколорс** задает цвет экранной клавиатуры для указанного типа цвета.</span><span class="sxs-lookup"><span data-stu-id="530cf-107">The **ISoftKbd::SetSoftKeyboardColors** method sets the soft keyboard color for the specified color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="530cf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="530cf-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a><span data-ttu-id="530cf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="530cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="530cf-110">*колортипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="530cf-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="530cf-111">Значение типа, указывающее тип цвета для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="530cf-111">A value specifying the color type for the soft keyboard.</span></span> <span data-ttu-id="530cf-112">Для перечисления [**колортипе**](/windows/win32/api/icm/ne-icm-colortype) определены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="530cf-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="530cf-113">*Цветовая палитра* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="530cf-113">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="530cf-114">32-битное значение [**COLORREF**](/windows/desktop/gdi/colorref) , УКАЗЫВАЮЩЕЕ цвет RGB.</span><span class="sxs-lookup"><span data-stu-id="530cf-114">A 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="530cf-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="530cf-115">Return value</span></span>

<span data-ttu-id="530cf-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="530cf-116">This method can return one of these values.</span></span>



| <span data-ttu-id="530cf-117">Значение</span><span class="sxs-lookup"><span data-stu-id="530cf-117">Value</span></span>                                                                                        | <span data-ttu-id="530cf-118">Описание</span><span class="sxs-lookup"><span data-stu-id="530cf-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="530cf-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="530cf-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="530cf-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="530cf-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="530cf-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="530cf-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="530cf-122">Один из параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="530cf-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="530cf-123">Требования</span><span class="sxs-lookup"><span data-stu-id="530cf-123">Requirements</span></span>



| <span data-ttu-id="530cf-124">Требование</span><span class="sxs-lookup"><span data-stu-id="530cf-124">Requirement</span></span> | <span data-ttu-id="530cf-125">Значение</span><span class="sxs-lookup"><span data-stu-id="530cf-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="530cf-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="530cf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="530cf-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="530cf-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="530cf-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="530cf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="530cf-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="530cf-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="530cf-130">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="530cf-130">Redistributable</span></span><br/>          | <span data-ttu-id="530cf-131">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="530cf-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="530cf-132">Header</span><span class="sxs-lookup"><span data-stu-id="530cf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="530cf-133"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="530cf-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="530cf-134">IDL</span><span class="sxs-lookup"><span data-stu-id="530cf-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="530cf-135"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="530cf-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="530cf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="530cf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="530cf-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="530cf-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="530cf-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="530cf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530cf-139">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="530cf-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="530cf-140">**Исофткбд:: Жетсофткэйбоардколорс**</span><span class="sxs-lookup"><span data-stu-id="530cf-140">**ISoftKbd::GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[<span data-ttu-id="530cf-141">**колортипе**</span><span class="sxs-lookup"><span data-stu-id="530cf-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="530cf-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="530cf-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

