---
title: Метод Исофткбд Жетсофткэйбоардпоссизе (Софткбдк. h)
description: Метод Исофткбд Жетсофткэйбоардпоссизе извлекает начальную точку и размер экранной клавиатуры.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Платформа служб текстового ввода метода Жетсофткэйбоардпоссизе
- Платформа текстовых служб метода Жетсофткэйбоардпоссизе, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Жетсофткэйбоардпоссизе
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340910"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a><span data-ttu-id="99403-106">Метод Исофткбд:: Жетсофткэйбоардпоссизе</span><span class="sxs-lookup"><span data-stu-id="99403-106">ISoftKbd::GetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="99403-107">Метод **исофткбд:: жетсофткэйбоардпоссизе** извлекает начальную точку и размер экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="99403-107">The **ISoftKbd::GetSoftKeyboardPosSize** method retrieves the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="99403-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99403-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a><span data-ttu-id="99403-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="99403-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99403-110">*лпстартпоинт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="99403-110">*lpStartPoint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99403-111">Указатель на буфер, в котором этот метод получает структуру [точек](/previous-versions//dd162805(v=vs.85)) , указывающую координаты верхнего левого положения экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="99403-111">Pointer to a buffer in which this method retrieves a [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="99403-112">*лпвидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="99403-112">*lpwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99403-113">Указатель на буфер, в котором этот метод получает ширину экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="99403-113">Pointer to a buffer in which this method retrieves the width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="99403-114">*лфеигхт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="99403-114">*lpheight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99403-115">Указатель на буфер, в котором этот метод получает высоту экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="99403-115">Pointer to a buffer in which this method retrieves the height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99403-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99403-116">Return value</span></span>

<span data-ttu-id="99403-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="99403-117">This method can return one of these values.</span></span>



| <span data-ttu-id="99403-118">Значение</span><span class="sxs-lookup"><span data-stu-id="99403-118">Value</span></span>                                                                                        | <span data-ttu-id="99403-119">Описание</span><span class="sxs-lookup"><span data-stu-id="99403-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="99403-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="99403-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="99403-121">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="99403-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="99403-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="99403-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="99403-123">Один из параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="99403-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="99403-124">Требования</span><span class="sxs-lookup"><span data-stu-id="99403-124">Requirements</span></span>



| <span data-ttu-id="99403-125">Требование</span><span class="sxs-lookup"><span data-stu-id="99403-125">Requirement</span></span> | <span data-ttu-id="99403-126">Значение</span><span class="sxs-lookup"><span data-stu-id="99403-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99403-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99403-127">Minimum supported client</span></span><br/> | <span data-ttu-id="99403-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="99403-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="99403-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99403-129">Minimum supported server</span></span><br/> | <span data-ttu-id="99403-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="99403-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="99403-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="99403-131">Redistributable</span></span><br/>          | <span data-ttu-id="99403-132">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="99403-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="99403-133">Header</span><span class="sxs-lookup"><span data-stu-id="99403-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="99403-134"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="99403-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="99403-135">IDL</span><span class="sxs-lookup"><span data-stu-id="99403-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99403-136"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="99403-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="99403-137">DLL</span><span class="sxs-lookup"><span data-stu-id="99403-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99403-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99403-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99403-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99403-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99403-140">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="99403-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="99403-141">**Исофткбд:: Сетсофткэйбоардпоссизе**</span><span class="sxs-lookup"><span data-stu-id="99403-141">**ISoftKbd::SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

