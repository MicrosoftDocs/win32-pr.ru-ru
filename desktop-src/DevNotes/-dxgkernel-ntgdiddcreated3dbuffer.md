---
description: Используется для создания команды уровня драйвера или буфера вершин указанного описания.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: Функция NtGdiDdCreateD3DBuffer (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2d402a70822fba094d22c82b8767ee3298b86374
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990376"
---
# <a name="ntgdiddcreated3dbuffer-function"></a><span data-ttu-id="50857-103">Функция NtGdiDdCreateD3DBuffer</span><span class="sxs-lookup"><span data-stu-id="50857-103">NtGdiDdCreateD3DBuffer function</span></span>

<span data-ttu-id="50857-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="50857-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="50857-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="50857-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="50857-106">Используется для создания команды уровня драйвера или буфера вершин указанного описания.</span><span class="sxs-lookup"><span data-stu-id="50857-106">Used to create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="50857-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50857-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="50857-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50857-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50857-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50857-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50857-110">Обработчик для [**\_ \_ глобальной структуры DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) , представляющей драйвер.</span><span class="sxs-lookup"><span data-stu-id="50857-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="50857-111">*хсурфаце* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="50857-111">*hSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50857-112">Указатель на массив маркеров поверхности.</span><span class="sxs-lookup"><span data-stu-id="50857-112">Pointer to an array of surface handles.</span></span> <span data-ttu-id="50857-113">Вызывающий объект может установить для этих дескрипторов предыдущие значения дескриптора, если они будут повторно созданы после переключения режима.</span><span class="sxs-lookup"><span data-stu-id="50857-113">The caller can set these handles to the previous handle values if the surfaces are being re-created after a mode switch.</span></span> <span data-ttu-id="50857-114">Этот процесс называется "восстановлением" в документации по DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="50857-114">This process is called "restoring" in the DirectDraw documentation.</span></span>

</dd> <dt>

<span data-ttu-id="50857-115">*пусурфацедескриптион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="50857-115">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50857-116">Указатель на структуру [**ддсурфацедеск**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) , описывающую поверхность или буфер, которые должен создать драйвер.</span><span class="sxs-lookup"><span data-stu-id="50857-116">Pointer to a [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="50857-117">*пусурфацеглобалдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="50857-117">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50857-118">Указатель на [**\_ \_ глобальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) , содержащую данные поверхности, которые совместно используются глобально с несколькими поверхностями.</span><span class="sxs-lookup"><span data-stu-id="50857-118">Pointer to a [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="50857-119">*пусурфацелокалдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="50857-119">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50857-120">Указатель на список локальных структур [**DD \_ Surface \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , описывающих объекты Surface, созданные драйвером.</span><span class="sxs-lookup"><span data-stu-id="50857-120">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span> <span data-ttu-id="50857-121">В этом массиве обычно присутствует только одна запись.</span><span class="sxs-lookup"><span data-stu-id="50857-121">There is usually only one entry in this array.</span></span>

</dd> <dt>

<span data-ttu-id="50857-122">*пусурфацеморедата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="50857-122">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50857-123">Указатель на [**область DD \_ . \_ Дополнительная**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) структура, содержащая дополнительные данные локальной поверхности.</span><span class="sxs-lookup"><span data-stu-id="50857-123">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="50857-124">*пукреатесурфацедата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="50857-124">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50857-125">Указатель на структуру [**DD \_ креатесурфацедата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) , которая содержит сведения, необходимые для создания буфера.</span><span class="sxs-lookup"><span data-stu-id="50857-125">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="50857-126">*пухсурфаце* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="50857-126">*puhSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50857-127">Используется API DirectDraw и не должен заполняться драйвером.</span><span class="sxs-lookup"><span data-stu-id="50857-127">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50857-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50857-128">Return value</span></span>

<span data-ttu-id="50857-129">**NtGdiDdCreateD3DBuffer** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="50857-129">**NtGdiDdCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="50857-130">Код возврата</span><span class="sxs-lookup"><span data-stu-id="50857-130">Return code</span></span>                                                                                              | <span data-ttu-id="50857-131">Описание</span><span class="sxs-lookup"><span data-stu-id="50857-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50857-132"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="50857-132"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="50857-133">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="50857-133">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="50857-134">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="50857-134">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="50857-135">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="50857-135">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="50857-136"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="50857-136"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="50857-137">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="50857-137">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="50857-138">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="50857-138">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="50857-139">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="50857-139">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="50857-140">Требования</span><span class="sxs-lookup"><span data-stu-id="50857-140">Requirements</span></span>



| <span data-ttu-id="50857-141">Требование</span><span class="sxs-lookup"><span data-stu-id="50857-141">Requirement</span></span> | <span data-ttu-id="50857-142">Значение</span><span class="sxs-lookup"><span data-stu-id="50857-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50857-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50857-143">Minimum supported client</span></span><br/> | <span data-ttu-id="50857-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50857-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="50857-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50857-145">Minimum supported server</span></span><br/> | <span data-ttu-id="50857-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50857-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="50857-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="50857-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="50857-148"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="50857-148"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50857-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50857-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50857-150">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="50857-150">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
