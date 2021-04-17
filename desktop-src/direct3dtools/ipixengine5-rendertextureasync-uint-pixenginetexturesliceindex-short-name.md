---
description: Визуализирует текстуру в файл и возвращает результат в асинчрнаусли узла.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5:: Рендертекстуреасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd16214887514fa348a672c45d5eb85c2df6bca5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537295"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span data-ttu-id="effc0-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Метод IPixEngine5:: Рендертекстуреасинк</span><span class="sxs-lookup"><span data-stu-id="effc0-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::RenderTextureAsync method</span></span>

<span data-ttu-id="effc0-104">Визуализирует текстуру в файл и возвращает результат в асинчрнаусли узла.</span><span class="sxs-lookup"><span data-stu-id="effc0-104">Renders a texture to a file and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="effc0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="effc0-105">Syntax</span></span>


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="effc0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc0-106">Parameters</span></span>

<span data-ttu-id="effc0-107">*текстуреид* </span><span class="sxs-lookup"><span data-stu-id="effc0-107">*textureId* </span></span>  
<span data-ttu-id="effc0-108">Идентификатор текстуры для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="effc0-108">The ID of the texture to render.</span></span>

<span data-ttu-id="effc0-109">*слицеиндекс* </span><span class="sxs-lookup"><span data-stu-id="effc0-109">*sliceIndex* </span></span>  
<span data-ttu-id="effc0-110">Индекс среза в текстуре для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="effc0-110">The index of the slice within the texture to render.</span></span>

<span data-ttu-id="effc0-111">*форматоверриде* </span><span class="sxs-lookup"><span data-stu-id="effc0-111">*formatOverride* </span></span>  
<span data-ttu-id="effc0-112">Переопределение формата цвета.</span><span class="sxs-lookup"><span data-stu-id="effc0-112">The color format override.</span></span>

<span data-ttu-id="effc0-113">*сокращение*</span><span class="sxs-lookup"><span data-stu-id="effc0-113">*lower*</span></span>   

<span data-ttu-id="effc0-114">*границ*</span><span class="sxs-lookup"><span data-stu-id="effc0-114">*upper*</span></span>   

<span data-ttu-id="effc0-115">*шадерфиленаме* </span><span class="sxs-lookup"><span data-stu-id="effc0-115">*shaderFileName* </span></span>  
<span data-ttu-id="effc0-116">Строка COM, содержащая путь к файлу шейдера.</span><span class="sxs-lookup"><span data-stu-id="effc0-116">A COM string containing the pathname of the shader file.</span></span>

<span data-ttu-id="effc0-117">*нумфлоатшадерварс* </span><span class="sxs-lookup"><span data-stu-id="effc0-117">*numFloatShaderVars* </span></span>  
<span data-ttu-id="effc0-118">Число переменных шейдера с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="effc0-118">The number of floating-point shader variables</span></span>

<span data-ttu-id="effc0-119">*count6 \_ шадерфлоатварнаме* </span><span class="sxs-lookup"><span data-stu-id="effc0-119">*count6\_shaderFloatVarName* </span></span>  
<span data-ttu-id="effc0-120">Строки COM контианинг имена переменных шейдера с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="effc0-120">COM strings contianing the names of the floating-point shader variables.</span></span>

<span data-ttu-id="effc0-121">*count6 \_ шадерфлоатварвалуе* </span><span class="sxs-lookup"><span data-stu-id="effc0-121">*count6\_shaderFloatVarValue* </span></span>  
<span data-ttu-id="effc0-122">Переменные шейдера с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="effc0-122">The floating-point shader variables.</span></span>

<span data-ttu-id="effc0-123">*нумбулшадерварс* </span><span class="sxs-lookup"><span data-stu-id="effc0-123">*numBoolShaderVars* </span></span>  
<span data-ttu-id="effc0-124">Число переменных шейдера Boolean.</span><span class="sxs-lookup"><span data-stu-id="effc0-124">The number of boolean shader variables.</span></span>

<span data-ttu-id="effc0-125">*count9 \_ шадербулварнаме* </span><span class="sxs-lookup"><span data-stu-id="effc0-125">*count9\_shaderBoolVarName* </span></span>  
<span data-ttu-id="effc0-126">Строки COM контианинг имена логических переменных шейдера.</span><span class="sxs-lookup"><span data-stu-id="effc0-126">COM strings contianing the names of the boolean shader variables.</span></span>

<span data-ttu-id="effc0-127">*count9 \_ шадербулварвалуе* </span><span class="sxs-lookup"><span data-stu-id="effc0-127">*count9\_shaderBoolVarValue* </span></span>  
<span data-ttu-id="effc0-128">Логические переменные шейдера.</span><span class="sxs-lookup"><span data-stu-id="effc0-128">The boolean shader variables.</span></span>

<span data-ttu-id="effc0-129">*рендерконтентфиленаме* </span><span class="sxs-lookup"><span data-stu-id="effc0-129">*renderContentFileName* </span></span>  
<span data-ttu-id="effc0-130">Строка COM, содержащая путь к файлу, в котором была записана подготовленная текстура.</span><span class="sxs-lookup"><span data-stu-id="effc0-130">A COM string containing the pathname of the file where the rendered texture was written.</span></span>

<span data-ttu-id="effc0-131">*обратные вызовы* </span><span class="sxs-lookup"><span data-stu-id="effc0-131">*callbacks* </span></span>  
<span data-ttu-id="effc0-132">Адрес объекта, который предоставляет интерфейс обратных вызовов IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="effc0-132">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="effc0-133">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="effc0-133">*requestCookie* </span></span>  
<span data-ttu-id="effc0-134">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="effc0-134">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="effc0-135">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="effc0-135">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="effc0-136">Не используется.</span><span class="sxs-lookup"><span data-stu-id="effc0-136">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="effc0-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="effc0-137">Return value</span></span>

<span data-ttu-id="effc0-138">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="effc0-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="effc0-139">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="effc0-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="effc0-140">Требования</span><span class="sxs-lookup"><span data-stu-id="effc0-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="effc0-141">Header</span><span class="sxs-lookup"><span data-stu-id="effc0-141">Header</span></span></p></td><td><span data-ttu-id="effc0-142">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="effc0-142">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="effc0-143"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="effc0-143"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="effc0-144">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="effc0-144">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
