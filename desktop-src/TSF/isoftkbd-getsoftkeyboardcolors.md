---
title: Метод Исофткбд Жетсофткэйбоардколорс (Софткбдк. h)
description: Метод Исофткбд Жетсофткэйбоардколорс извлекает цвет экранной клавиатуры, соответствующий заданному типу цвета.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Платформа служб текстового ввода метода Жетсофткэйбоардколорс
- Платформа текстовых служб метода Жетсофткэйбоардколорс, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Жетсофткэйбоардколорс
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "105684714"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a><span data-ttu-id="0db57-106">Метод Исофткбд:: Жетсофткэйбоардколорс</span><span class="sxs-lookup"><span data-stu-id="0db57-106">ISoftKbd::GetSoftKeyboardColors method</span></span>

<span data-ttu-id="0db57-107">Метод **исофткбд:: жетсофткэйбоардколорс** получает цвет экранной клавиатуры, соответствующий заданному типу цвета.</span><span class="sxs-lookup"><span data-stu-id="0db57-107">The **ISoftKbd::GetSoftKeyboardColors** method retrieves the soft keyboard color corresponding to the supplied color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db57-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0db57-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a><span data-ttu-id="0db57-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0db57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db57-110">*колортипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0db57-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db57-111">Значение типа, указывающее тип цвета, который требуется получить для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="0db57-111">A value specifying the color type to retrieve for the soft keyboard.</span></span> <span data-ttu-id="0db57-112">Для перечисления [**колортипе**](/windows/win32/api/icm/ne-icm-colortype) определены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="0db57-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="0db57-113">*лпколор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0db57-113">*lpColor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0db57-114">Указатель на буфер, в котором этот метод получает 32-битное значение [**COLORREF**](/windows/desktop/gdi/colorref) , УКАЗЫВАЮЩЕЕ цвет RGB.</span><span class="sxs-lookup"><span data-stu-id="0db57-114">Pointer to a buffer in which this method retrieves a 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db57-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0db57-115">Return value</span></span>

<span data-ttu-id="0db57-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="0db57-116">This method can return one of these values.</span></span>



| <span data-ttu-id="0db57-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0db57-117">Value</span></span>                                                                                        | <span data-ttu-id="0db57-118">Описание</span><span class="sxs-lookup"><span data-stu-id="0db57-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0db57-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0db57-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0db57-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="0db57-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="0db57-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0db57-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0db57-122">Один из параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="0db57-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0db57-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0db57-123">Requirements</span></span>



| <span data-ttu-id="0db57-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0db57-124">Requirement</span></span> | <span data-ttu-id="0db57-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0db57-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0db57-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0db57-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0db57-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0db57-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0db57-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0db57-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0db57-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0db57-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0db57-130">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0db57-130">Redistributable</span></span><br/>          | <span data-ttu-id="0db57-131">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="0db57-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="0db57-132">Header</span><span class="sxs-lookup"><span data-stu-id="0db57-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db57-133"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db57-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="0db57-134">IDL</span><span class="sxs-lookup"><span data-stu-id="0db57-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0db57-135"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0db57-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="0db57-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0db57-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0db57-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0db57-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db57-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0db57-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db57-139">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="0db57-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="0db57-140">**Исофткбд:: Сетсофткэйбоардколорс**</span><span class="sxs-lookup"><span data-stu-id="0db57-140">**ISoftKbd::SetSoftKeyboardColors**</span></span>](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[<span data-ttu-id="0db57-141">**колортипе**</span><span class="sxs-lookup"><span data-stu-id="0db57-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="0db57-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="0db57-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

