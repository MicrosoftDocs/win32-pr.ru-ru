---
description: Возвращает список несжатых форматов пикселей, которые могут быть отображены с помощью указанного профиля DirectX Video Acceleration (ДКСВА).
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'Метод IDirect3DVideoDevice9:: Жетункомпресседдксваформатс (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345075"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a><span data-ttu-id="1c35d-103">Метод IDirect3DVideoDevice9:: Жетункомпресседдксваформатс</span><span class="sxs-lookup"><span data-stu-id="1c35d-103">IDirect3DVideoDevice9::GetUncompressedDXVAFormats method</span></span>

<span data-ttu-id="1c35d-104">Возвращает список несжатых форматов пикселей, которые могут быть отображены с помощью указанного профиля DirectX Video Acceleration (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="1c35d-104">Gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c35d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c35d-105">Syntax</span></span>


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a><span data-ttu-id="1c35d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c35d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c35d-107">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="1c35d-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="1c35d-108">Указатель на идентификатор GUID, указывающий профиль ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="1c35d-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="1c35d-109">Чтобы получить список поддерживаемых профилей, вызовите [**IDirect3DVideoDevice9:: жетдксвагуидс**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="1c35d-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c35d-110">*пнумформатс*</span><span class="sxs-lookup"><span data-stu-id="1c35d-110">*pNumFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="1c35d-111">В поле входные данные указывает количество элементов в массиве *пформатс* .</span><span class="sxs-lookup"><span data-stu-id="1c35d-111">On input, specifies the number of elements in the *pFormats* array.</span></span> <span data-ttu-id="1c35d-112">Если *пформатс* имеет **значение NULL**, значение `*pNumFormats` должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1c35d-112">If *pFormats* is **NULL**, the value of `*pNumFormats` must be zero.</span></span>

<span data-ttu-id="1c35d-113">В выходных данных, если *пформатс* имеет **значение NULL**, *пнумформатс* получает число поддерживаемых форматов пикселей.</span><span class="sxs-lookup"><span data-stu-id="1c35d-113">On output, if *pFormats* is **NULL**, *pNumFormats* receives the number of supported pixel formats.</span></span> <span data-ttu-id="1c35d-114">В противном случае *пнумформатс* получает фактическое число форматов пикселей, скопированных в массив *пформатс* .</span><span class="sxs-lookup"><span data-stu-id="1c35d-114">Otherwise, *pNumFormats* receives the actual number of pixel formats copied to the *pFormats* array.</span></span>

</dd> <dt>

<span data-ttu-id="1c35d-115">*пформатс*</span><span class="sxs-lookup"><span data-stu-id="1c35d-115">*pFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="1c35d-116">Адрес массива значений **D3DFORMAT** или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1c35d-116">Address of an array of **D3DFORMAT** values, or **NULL**.</span></span> <span data-ttu-id="1c35d-117">Если значение не **равно NULL**, массив получает список форматов пикселей.</span><span class="sxs-lookup"><span data-stu-id="1c35d-117">If the value is non-**NULL**, the array receives a list of pixel formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c35d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c35d-118">Return value</span></span>

<span data-ttu-id="1c35d-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1c35d-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1c35d-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1c35d-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c35d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c35d-121">Remarks</span></span>

<span data-ttu-id="1c35d-122">Вызовите этот метод дважды.</span><span class="sxs-lookup"><span data-stu-id="1c35d-122">Call this method twice.</span></span> <span data-ttu-id="1c35d-123">При первом вызове задайте для *Пформатс* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1c35d-123">On the first call, set *pFormats* to **NULL**.</span></span> <span data-ttu-id="1c35d-124">Параметр *пнумформатс* получает количество форматов.</span><span class="sxs-lookup"><span data-stu-id="1c35d-124">The *pNumFormats* parameter receives the number of formats.</span></span> <span data-ttu-id="1c35d-125">Выделите массив **D3DFORMAT** с требуемым размером и снова вызовите метод.</span><span class="sxs-lookup"><span data-stu-id="1c35d-125">Allocate a **D3DFORMAT** array with the required size, and call the method again.</span></span> <span data-ttu-id="1c35d-126">На этот раз задайте *пформатс* в качестве адреса массива.</span><span class="sxs-lookup"><span data-stu-id="1c35d-126">This time, set *pFormats* to the address of the array.</span></span> <span data-ttu-id="1c35d-127">Метод заполняет массив списком форматов пикселей.</span><span class="sxs-lookup"><span data-stu-id="1c35d-127">The method fills the array with the list of pixel formats.</span></span>

<span data-ttu-id="1c35d-128">Драйвер должен возвращать форматы в порядке убывания предпочтений, при этом наиболее предпочтительный формат указан первыми.</span><span class="sxs-lookup"><span data-stu-id="1c35d-128">The driver should return the formats in decreasing order of preference, with the most preferred format listed first.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c35d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="1c35d-129">Requirements</span></span>



| <span data-ttu-id="1c35d-130">Требование</span><span class="sxs-lookup"><span data-stu-id="1c35d-130">Requirement</span></span> | <span data-ttu-id="1c35d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1c35d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1c35d-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c35d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1c35d-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c35d-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c35d-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c35d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1c35d-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1c35d-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1c35d-136">Header</span><span class="sxs-lookup"><span data-stu-id="1c35d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c35d-137"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c35d-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c35d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c35d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c35d-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="1c35d-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




