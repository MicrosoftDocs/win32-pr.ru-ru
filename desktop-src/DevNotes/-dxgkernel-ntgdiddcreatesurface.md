---
description: Функция Нтгдиддкреатесурфаце — подключает поверхность к другой поверхности.
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Функция Нтгдиддкреатесурфаце (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bf8e13cff80ddea4e102c045c174565e7e835274
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085782"
---
# <a name="ntgdiddcreatesurface-function"></a><span data-ttu-id="db778-103">Функция Нтгдиддкреатесурфаце</span><span class="sxs-lookup"><span data-stu-id="db778-103">NtGdiDdCreateSurface function</span></span>

<span data-ttu-id="db778-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="db778-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="db778-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="db778-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="db778-106">Присоединяет поверхность к другой поверхности.</span><span class="sxs-lookup"><span data-stu-id="db778-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="db778-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db778-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="db778-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="db778-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db778-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db778-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db778-110">Обработчик для [**\_ \_ глобальной структуры DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) , представляющей драйвер.</span><span class="sxs-lookup"><span data-stu-id="db778-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="db778-111">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db778-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db778-112">Предыдущий маркер на той же поверхности.</span><span class="sxs-lookup"><span data-stu-id="db778-112">Previous handle to the same surface.</span></span> <span data-ttu-id="db778-113">Используется при повторном создании поверхности после переключения режима.</span><span class="sxs-lookup"><span data-stu-id="db778-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="db778-114">*пусурфацедескриптион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="db778-114">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db778-115">Указатель на структуру [**ддсурфацедеск**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) , описывающую поверхность или буфер, которые должен создать драйвер.</span><span class="sxs-lookup"><span data-stu-id="db778-115">Pointer to the [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="db778-116">*пусурфацеглобалдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="db778-116">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db778-117">Указатель на [**\_ \_ глобальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) , содержащую данные поверхности, которые доступны глобально с несколькими поверхностями.</span><span class="sxs-lookup"><span data-stu-id="db778-117">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="db778-118">*пусурфацелокалдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="db778-118">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db778-119">Указатель на список локальных структур [**DD \_ Surface \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , описывающих объекты Surface, созданные драйвером.</span><span class="sxs-lookup"><span data-stu-id="db778-119">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="db778-120">*пусурфацеморедата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="db778-120">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db778-121">Указатель на [**область DD \_ . \_ Дополнительная**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) структура, содержащая дополнительные данные локальной поверхности.</span><span class="sxs-lookup"><span data-stu-id="db778-121">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="db778-122">*пукреатесурфацедата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="db778-122">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db778-123">Указатель на структуру [**DD \_ креатесурфацедата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) , которая содержит сведения, необходимые для создания поверхности.</span><span class="sxs-lookup"><span data-stu-id="db778-123">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create a surface.</span></span>

</dd> <dt>

<span data-ttu-id="db778-124">*пухсурфаце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db778-124">*puhSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db778-125">Используется API DirectDraw и не должен заполняться драйвером.</span><span class="sxs-lookup"><span data-stu-id="db778-125">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db778-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db778-126">Return value</span></span>

<span data-ttu-id="db778-127">**Нтгдиддкреатесурфаце** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="db778-127">**NtGdiDdCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="db778-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="db778-128">Return code</span></span>                                                                                              | <span data-ttu-id="db778-129">Описание</span><span class="sxs-lookup"><span data-stu-id="db778-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db778-130"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="db778-130"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="db778-131">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="db778-131">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="db778-132">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="db778-132">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="db778-133">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="db778-133">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="db778-134"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="db778-134"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="db778-135">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="db778-135">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="db778-136">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="db778-136">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="db778-137">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="db778-137">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db778-138">Remarks</span><span class="sxs-lookup"><span data-stu-id="db778-138">Remarks</span></span>

<span data-ttu-id="db778-139">Рекомендуется, чтобы приложение вызывало [IDirectDraw7:: креатесурфаце](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) , а не использовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="db778-139">It is recommended that your application call [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) instead of using this function.</span></span>

<span data-ttu-id="db778-140">При создании цепочки подключенных поверхностей, таких как цепочка подкачки или цепочка или MIP-карты, для первой поверхности следует вызывать [**нтгдиддкреатесурфацеобжект**](-dxgkernel-ntgdiddcreatesurfaceobject.md) .</span><span class="sxs-lookup"><span data-stu-id="db778-140">When creating a chain of attached surfaces, such as a swap chain or chain or mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) should be called for each surface first.</span></span> <span data-ttu-id="db778-141">Затем вызовите [**нтгдиддаттачсурфаце**](-dxgkernel-ntgdiddattachsurface.md) , чтобы присоединить их.</span><span class="sxs-lookup"><span data-stu-id="db778-141">Then call [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) to attach them.</span></span> <span data-ttu-id="db778-142">Наконец, вызовите **нтгдиддкреатесурфаце** для первой поверхности только в цепочке.</span><span class="sxs-lookup"><span data-stu-id="db778-142">Finally, call **NtGdiDdCreateSurface** for the first surface in the chain only.</span></span> <span data-ttu-id="db778-143">В этом случае *хсурфаце* будет маркером, возвращенным **нтгдиддкреатесурфацеобжект** для первой поверхности в цепочке.</span><span class="sxs-lookup"><span data-stu-id="db778-143">In this case, *hSurface* would be the handle returned by **NtGdiDdCreateSurfaceObject** for the first surface in the chain.</span></span>

<span data-ttu-id="db778-144">**Нтгдиддкреатесурфаце** следует вызывать только для создания поверхностей в локальной и нелокальной видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="db778-144">**NtGdiDdCreateSurface** should only be called to create surfaces in local and non-local video memory.</span></span> <span data-ttu-id="db778-145">Его никогда не следует вызывать для создания поверхностей системной памяти.</span><span class="sxs-lookup"><span data-stu-id="db778-145">It should never be called to create system memory surfaces.</span></span> <span data-ttu-id="db778-146">Для создания поверхностей системной памяти используйте вместо него [**нтгдиддкреатесурфацеобжект**](-dxgkernel-ntgdiddcreatesurfaceobject.md) .</span><span class="sxs-lookup"><span data-stu-id="db778-146">To create system memory surfaces, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="db778-147">Требования</span><span class="sxs-lookup"><span data-stu-id="db778-147">Requirements</span></span>



| <span data-ttu-id="db778-148">Требование</span><span class="sxs-lookup"><span data-stu-id="db778-148">Requirement</span></span> | <span data-ttu-id="db778-149">Значение</span><span class="sxs-lookup"><span data-stu-id="db778-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db778-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db778-150">Minimum supported client</span></span><br/> | <span data-ttu-id="db778-151">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db778-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="db778-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db778-152">Minimum supported server</span></span><br/> | <span data-ttu-id="db778-153">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db778-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="db778-154">Заголовок</span><span class="sxs-lookup"><span data-stu-id="db778-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="db778-155"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="db778-155"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db778-156">См. также</span><span class="sxs-lookup"><span data-stu-id="db778-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db778-157">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="db778-157">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
