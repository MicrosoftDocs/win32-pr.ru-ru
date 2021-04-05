---
description: Создает объект поверхности режима ядра, представляющий объект поверхности пользовательского режима, на который ссылается Пусурфацелокал.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Функция Нтгдиддкреатесурфацеобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072367"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a><span data-ttu-id="26865-103">Функция Нтгдиддкреатесурфацеобжект</span><span class="sxs-lookup"><span data-stu-id="26865-103">NtGdiDdCreateSurfaceObject function</span></span>

<span data-ttu-id="26865-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="26865-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="26865-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="26865-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="26865-106">Создает объект поверхности режима ядра, представляющий объект поверхности пользовательского режима, на который ссылается *пусурфацелокал*.</span><span class="sxs-lookup"><span data-stu-id="26865-106">Creates a kernel-mode surface object that represents the user-mode surface object referenced by *puSurfaceLocal*.</span></span>

## <a name="syntax"></a><span data-ttu-id="26865-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26865-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a><span data-ttu-id="26865-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="26865-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26865-109">*хдиректдравлокал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26865-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26865-110">Обработчик для объекта DirectDraw режима ядра.</span><span class="sxs-lookup"><span data-stu-id="26865-110">Handle to the kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="26865-111">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26865-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26865-112">Предыдущий маркер на той же поверхности.</span><span class="sxs-lookup"><span data-stu-id="26865-112">Previous handle to the same surface.</span></span> <span data-ttu-id="26865-113">Используется при повторном создании поверхности после переключения режима.</span><span class="sxs-lookup"><span data-stu-id="26865-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="26865-114">*пусурфацелокал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26865-114">*puSurfaceLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26865-115">Указатель на [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , представляющую объект поверхности пользовательского режима DirectDraw, с которым необходимо связать выделенную память.</span><span class="sxs-lookup"><span data-stu-id="26865-115">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw user-mode surface object with which to associate the allocated memory.</span></span> <span data-ttu-id="26865-116">Дополнительные сведения см. в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="26865-116">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="26865-117">*пусурфацеморе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26865-117">*puSurfaceMore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26865-118">Указатель на [**область DD \_ \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) , который содержит дополнительные локальные данные для каждого отдельного объекта Surface.</span><span class="sxs-lookup"><span data-stu-id="26865-118">Pointer to the [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local data for each individual surface object.</span></span> <span data-ttu-id="26865-119">Дополнительные сведения см. в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="26865-119">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="26865-120">*пусурфацеглобал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26865-120">*puSurfaceGlobal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26865-121">Указатель на [**\_ \_ глобальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) , которая содержит данные поверхности, совместно используемые глобально с несколькими поверхностями.</span><span class="sxs-lookup"><span data-stu-id="26865-121">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure that contains surface data shared globally with multiple surfaces.</span></span> <span data-ttu-id="26865-122">Дополнительные сведения см. в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="26865-122">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="26865-123">*бкомплете* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26865-123">*bComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26865-124">Флаг завершения объектов в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="26865-124">Kernel-mode object completion flag.</span></span> <span data-ttu-id="26865-125">Может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="26865-125">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="26865-126">УСЛОВИЯ</span><span class="sxs-lookup"><span data-stu-id="26865-126">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="26865-127">Завершите всю обработку, касающуюся представления режима ядра.</span><span class="sxs-lookup"><span data-stu-id="26865-127">Complete all processing concerning the kernel-mode representation.</span></span>

</dd> <dt>



 <span data-ttu-id="26865-128">ISFALSE</span><span class="sxs-lookup"><span data-stu-id="26865-128">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="26865-129">Создайте объект, но не настраиваете внутренние данные, такие как указатель памяти.</span><span class="sxs-lookup"><span data-stu-id="26865-129">Create the object, but do not set up internal data such as the memory pointer.</span></span> <span data-ttu-id="26865-130">Объекты, созданные с помощью **false** , могут быть присоединены с помощью [**нтгдиддаттачсурфаце**](-dxgkernel-ntgdiddattachsurface.md) и завершаются вызовом [**нтгдиддкреатесурфаце**](-dxgkernel-ntgdiddcreatesurface.md).</span><span class="sxs-lookup"><span data-stu-id="26865-130">Objects created using **FALSE** can be attached using [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) and are completed by a call to [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26865-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26865-131">Return value</span></span>

<span data-ttu-id="26865-132">В случае успеха эта функция возвращает маркер в представление поверхности режима ядра; в противном случае возвращается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="26865-132">If successful, this function returns a handle to the kernel-mode surface representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="26865-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26865-133">Remarks</span></span>

<span data-ttu-id="26865-134">В приложениях рекомендуется использовать интерфейсы API DirectDraw и [Direct3D](../direct3d10/d3d10-graphics-reference.md) для создания объектов графических устройств и управления ими.</span><span class="sxs-lookup"><span data-stu-id="26865-134">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="26865-135">Эти конструкции являются абстрактным процессом создания устройств в упрощенном и независимом от операционной системе виде.</span><span class="sxs-lookup"><span data-stu-id="26865-135">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="26865-136">Требования</span><span class="sxs-lookup"><span data-stu-id="26865-136">Requirements</span></span>



| <span data-ttu-id="26865-137">Требование</span><span class="sxs-lookup"><span data-stu-id="26865-137">Requirement</span></span> | <span data-ttu-id="26865-138">Значение</span><span class="sxs-lookup"><span data-stu-id="26865-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26865-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26865-139">Minimum supported client</span></span><br/> | <span data-ttu-id="26865-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26865-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="26865-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26865-141">Minimum supported server</span></span><br/> | <span data-ttu-id="26865-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26865-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="26865-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="26865-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="26865-144"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="26865-144"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26865-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26865-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26865-146">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="26865-146">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="26865-147">**ддкреатесурфацеобжект**</span><span class="sxs-lookup"><span data-stu-id="26865-147">**DdCreateSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[<span data-ttu-id="26865-148">**нтгдиддделетесурфацеобжект**</span><span class="sxs-lookup"><span data-stu-id="26865-148">**NtGdiDdDeleteSurfaceObject**</span></span>](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[<span data-ttu-id="26865-149">**нтгдиддаттачсурфаце**</span><span class="sxs-lookup"><span data-stu-id="26865-149">**NtGdiDdAttachSurface**</span></span>](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[<span data-ttu-id="26865-150">**нтгдиддкреатесурфаце**</span><span class="sxs-lookup"><span data-stu-id="26865-150">**NtGdiDdCreateSurface**</span></span>](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
