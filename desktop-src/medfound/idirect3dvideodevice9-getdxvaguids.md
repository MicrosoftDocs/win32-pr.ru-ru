---
description: Возвращает список профилей DirectX Video Acceleration (ДКСВА), поддерживаемых драйвером экрана.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'Метод IDirect3DVideoDevice9:: Жетдксвагуидс (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711790"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a><span data-ttu-id="dfc8b-103">Метод IDirect3DVideoDevice9:: Жетдксвагуидс</span><span class="sxs-lookup"><span data-stu-id="dfc8b-103">IDirect3DVideoDevice9::GetDXVAGuids method</span></span>

<span data-ttu-id="dfc8b-104">Возвращает список профилей DirectX Video Acceleration (ДКСВА), поддерживаемых драйвером экрана.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-104">Gets a list of DirectX Video Acceleration (DXVA) profiles that are supported by the display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc8b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfc8b-105">Syntax</span></span>


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a><span data-ttu-id="dfc8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfc8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfc8b-107">*пнумгуидс*</span><span class="sxs-lookup"><span data-stu-id="dfc8b-107">*pNumGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="dfc8b-108">В поле входные данные указывает количество элементов в массиве *пгуидс* .</span><span class="sxs-lookup"><span data-stu-id="dfc8b-108">On input, specifies the number of elements in the *pGuids* array.</span></span> <span data-ttu-id="dfc8b-109">Если *пгуидс* имеет **значение NULL**, значение `*pNumGuids` должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-109">If *pGuids* is **NULL**, the value of `*pNumGuids` must be zero.</span></span>

<span data-ttu-id="dfc8b-110">В выходных данных, если *пгуидс* имеет **значение NULL**, *пнумгуидс* получает количество профилей дксва с ограниченным режимом.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-110">On output, if *pGuids* is **NULL**, *pNumGuids* receives the number of restricted-mode DXVA profiles.</span></span> <span data-ttu-id="dfc8b-111">В противном случае *пнумгуидс* получает фактическое число идентификаторов GUID, копируемых в массив *пгуидс* .</span><span class="sxs-lookup"><span data-stu-id="dfc8b-111">Otherwise, *pNumGuids* receives the actual number of GUIDs that are copied to the *pGuids* array.</span></span>

</dd> <dt>

<span data-ttu-id="dfc8b-112">*пгуидс*</span><span class="sxs-lookup"><span data-stu-id="dfc8b-112">*pGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="dfc8b-113">Адрес массива идентификаторов GUID или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-113">Address of an array of GUIDs or **NULL**.</span></span> <span data-ttu-id="dfc8b-114">Если значение не **равно NULL**, массив получает список идентификаторов GUID, которые ОПРЕДЕЛЯЮТ профили дксва с ограниченным режимом.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-114">If the value is non-**NULL**, the array receives a list of GUIDs that specify restricted-mode DXVA profiles.</span></span> <span data-ttu-id="dfc8b-115">Эти идентификаторы GUID определены в дксва. h и описаны в [спецификации дксва 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="dfc8b-115">These GUIDs are defined in dxva.h, and are documented in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfc8b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfc8b-116">Return value</span></span>

<span data-ttu-id="dfc8b-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dfc8b-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dfc8b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfc8b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfc8b-119">Remarks</span></span>

<span data-ttu-id="dfc8b-120">Вызовите этот метод дважды.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-120">Call this method twice.</span></span> <span data-ttu-id="dfc8b-121">При первом вызове задайте для *Пгуидс* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-121">On the first call, set *pGuids* to **NULL**.</span></span> <span data-ttu-id="dfc8b-122">Параметр *пнумгуидс* получает количество идентификаторов GUID для профиля дксва.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-122">The *pNumGuids* parameter receives the number of DXVA profile GUIDs.</span></span> <span data-ttu-id="dfc8b-123">Выделите массив идентификаторов GUID с требуемым размером и снова вызовите метод.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-123">Allocate an array of GUIDs with the required size and call the method again.</span></span> <span data-ttu-id="dfc8b-124">На этот раз задайте *пгуидс* в качестве адреса массива.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-124">This time, set *pGuids* to the address of the array.</span></span> <span data-ttu-id="dfc8b-125">Метод заполняет массив списком идентификаторов GUID профиля ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-125">The method fills the array with the list of DXVA profile GUIDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfc8b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="dfc8b-126">Requirements</span></span>



| <span data-ttu-id="dfc8b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="dfc8b-127">Requirement</span></span> | <span data-ttu-id="dfc8b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dfc8b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dfc8b-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfc8b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dfc8b-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfc8b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dfc8b-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfc8b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dfc8b-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dfc8b-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dfc8b-133">Header</span><span class="sxs-lookup"><span data-stu-id="dfc8b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfc8b-134"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfc8b-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfc8b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfc8b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc8b-136">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="dfc8b-136">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
