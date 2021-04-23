---
title: Метод Исофткбд Сетсофткэйбоардпоссизе (Софткбдк. h)
description: Метод Исофткбд Сетсофткэйбоардпоссизе задает начальную точку и размер экранной клавиатуры.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- Платформа служб текстового ввода метода Сетсофткэйбоардпоссизе
- Платформа текстовых служб метода Сетсофткэйбоардпоссизе, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Сетсофткэйбоардпоссизе
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7131d9c46c90917f2ebdf471916f872aedb2e33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492099"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a><span data-ttu-id="25f92-106">Метод Исофткбд:: Сетсофткэйбоардпоссизе</span><span class="sxs-lookup"><span data-stu-id="25f92-106">ISoftKbd::SetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="25f92-107">Метод **исофткбд:: сетсофткэйбоардпоссизе** задает начальную точку и размер экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="25f92-107">The **ISoftKbd::SetSoftKeyboardPosSize** method sets the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f92-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25f92-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a><span data-ttu-id="25f92-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="25f92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f92-110">*StartPoint* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25f92-110">*StartPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f92-111">Структура [точек](/previous-versions//dd162805(v=vs.85)) , указывающая координаты левого верхнего положения экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="25f92-111">A [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="25f92-112">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25f92-112">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f92-113">Ширина экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="25f92-113">Width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="25f92-114">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25f92-114">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f92-115">Высота экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="25f92-115">Height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25f92-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25f92-116">Return value</span></span>

<span data-ttu-id="25f92-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="25f92-117">This method can return one of these values.</span></span>



| <span data-ttu-id="25f92-118">Значение</span><span class="sxs-lookup"><span data-stu-id="25f92-118">Value</span></span>                                                                                        | <span data-ttu-id="25f92-119">Описание</span><span class="sxs-lookup"><span data-stu-id="25f92-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="25f92-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="25f92-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="25f92-121">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="25f92-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="25f92-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="25f92-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="25f92-123">Один из параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="25f92-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="25f92-124">Требования</span><span class="sxs-lookup"><span data-stu-id="25f92-124">Requirements</span></span>



| <span data-ttu-id="25f92-125">Требование</span><span class="sxs-lookup"><span data-stu-id="25f92-125">Requirement</span></span> | <span data-ttu-id="25f92-126">Значение</span><span class="sxs-lookup"><span data-stu-id="25f92-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25f92-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25f92-127">Minimum supported client</span></span><br/> | <span data-ttu-id="25f92-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="25f92-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="25f92-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25f92-129">Minimum supported server</span></span><br/> | <span data-ttu-id="25f92-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="25f92-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="25f92-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="25f92-131">Redistributable</span></span><br/>          | <span data-ttu-id="25f92-132">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="25f92-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="25f92-133">Header</span><span class="sxs-lookup"><span data-stu-id="25f92-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="25f92-134"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="25f92-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="25f92-135">IDL</span><span class="sxs-lookup"><span data-stu-id="25f92-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25f92-136"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25f92-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="25f92-137">DLL</span><span class="sxs-lookup"><span data-stu-id="25f92-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25f92-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25f92-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f92-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25f92-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f92-140">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="25f92-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

