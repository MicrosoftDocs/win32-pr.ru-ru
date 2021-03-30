---
description: Запрашивает в ранее созданное представление в режиме ядра объекта Microsoft DirectDraw для его возможностей.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Функция Нтгдиддкуеридиректдравобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 557854f70f4f1a55022b16d1bfe045efbc017a13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896242"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a><span data-ttu-id="3f9fe-103">Функция Нтгдиддкуеридиректдравобжект</span><span class="sxs-lookup"><span data-stu-id="3f9fe-103">NtGdiDdQueryDirectDrawObject function</span></span>

<span data-ttu-id="3f9fe-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3f9fe-105">Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3f9fe-106">Запрашивает в ранее созданное представление в режиме ядра объекта Microsoft DirectDraw для его возможностей.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-106">Queries a previously created kernel-mode representation of a Microsoft DirectDraw object for its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f9fe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f9fe-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a><span data-ttu-id="3f9fe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f9fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f9fe-109">*хдиректдравлокал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f9fe-110">Обработано ранее созданное устройство DirectDraw режима ядра.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-110">Handle to the previously-created kernel-mode DirectDraw device.</span></span>

</dd> <dt>

<span data-ttu-id="3f9fe-111">*фалинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-111">*pHalInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f9fe-112">Указатель на структуру [**DD \_ халинфо**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) , которая будет заполнена возможностями устройства.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-112">Pointer to a [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) structure that will be filled with the device's capabilities.</span></span> <span data-ttu-id="3f9fe-113">Дополнительные сведения см. в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-113">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="3f9fe-114">*пкаллбаккфлагс*</span><span class="sxs-lookup"><span data-stu-id="3f9fe-114">*pCallBackFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="3f9fe-115">Указатель на предоставленный вызывающим объектом буфер, в котором хранятся флаги обратного вызова, переданные драйвером.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-115">Pointer to a caller-provided buffer that stores driver-reported callback flags.</span></span> <span data-ttu-id="3f9fe-116">Буфер должен иметь размер 3 \* sizeof (DWORD) и сохраняет флаги обратного вызова в следующем порядке: пкаллбаккфлагс \[ 0 \] для флагов в параметрах [**\_ обратного вызова DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), Пкаллбаккфлагс \[ 1 \] для флагов в [**DD \_ сурфацекаллбаккс**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)и пкаллбаккфлагс \[ 2 \] для флагов в [**DD \_ палеттекаллбаккс**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span><span class="sxs-lookup"><span data-stu-id="3f9fe-116">The buffer should be of size 3\*sizeof(DWORD) and stores callback flags in the following order: pCallBackFlags\[0\] for flags in [**DD\_CALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), pCallBackFlags\[1\] for flags in [**DD\_SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks), and pCallBackFlags\[2\] for flags in [**DD\_PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span></span> <span data-ttu-id="3f9fe-117">Дополнительные сведения см. в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-117">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="3f9fe-118">*puD3dCallbacks* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-118">*puD3dCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f9fe-119">Указатель на таблицу указателей обратного вызова Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-119">Pointer to a table of Direct3D callback pointers.</span></span> <span data-ttu-id="3f9fe-120">Таблица заполняется указателями на функции в Gdi32.dll, имитирующие драйвер экрана Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-120">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="3f9fe-121">Эта таблица обратного вызова идентична \_ структуре D3DHAL D3DCALLBACKS, обсуждаемой в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-121">This callback table is identical to the D3DHAL\_D3DCALLBACKS structure discussed in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="3f9fe-122">*puD3dDriverData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-122">*puD3dDriverData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f9fe-123">Указатель на [**данные \_ глобалдривердата D3DHAL**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) , как описано в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-123">Pointer to [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) data, as described in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="3f9fe-124">*puD3dBufferCallbacks* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-124">*puD3dBufferCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f9fe-125">Указатель на таблицу указателей обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-125">Pointer to a table of callback pointers.</span></span> <span data-ttu-id="3f9fe-126">Таблица заполняется указателями на функции в Gdi32.dll, имитирующие драйвер экрана Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-126">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="3f9fe-127">Эта таблица обратного вызова идентична \_ структуре ддхал ддексебуфкаллбаккс, которая сопоставляется с структурой [**\_ D3DBUFCALLBACKS DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) , обсуждаемой в документации по DDK, за исключением того, что члены XxxD3DBuffer в **DD \_ D3DBUFCALLBACKS** заменяются ксксксексекутебуффер в ддхал \_ ддексебуфкаллбаккс.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-127">This callback table is identical to the DDHAL\_DDEXEBUFCALLBACKS structure, which maps to the [**DD\_D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) structure discussed in the DDK documentation, except that members XxxD3DBuffer in **DD\_D3DBUFCALLBACKS** are replaced with XxxExecuteBuffer in DDHAL\_DDEXEBUFCALLBACKS.</span></span>

</dd> <dt>

<span data-ttu-id="3f9fe-128">*puD3dTextureFormats* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-128">*puD3dTextureFormats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f9fe-129">Указатель на массив структур [**ддсурфацедеск**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) , определяющих набор допустимых форматов текстуры.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-129">Pointer to an array of [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structures that define the set of permissible texture formats.</span></span>

</dd> <dt>

<span data-ttu-id="3f9fe-130">*пунумхеапс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-130">*puNumHeaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f9fe-131">Указатель на элемент **двнумхеапс** в [**DD \_ халинфо**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**Вмидата**.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-131">Pointer to the **dwNumHeaps** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span></span> <span data-ttu-id="3f9fe-132">Член **двнумхеапс** указывает количество куч памяти в *пувмлист*.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-132">The **dwNumHeaps** member specifies the number of memory heaps in *puvmList*.</span></span> <span data-ttu-id="3f9fe-133">Дополнительные сведения см. в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-133">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="3f9fe-134">*пувмлист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-134">*puvmList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f9fe-135">Указатель на список дескрипторов кучи видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-135">Pointer to a list of video memory heap descriptors.</span></span> <span data-ttu-id="3f9fe-136">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-136">Can be **NULL**.</span></span> <span data-ttu-id="3f9fe-137">Этот параметр не используется, так как управление видеопамятью полностью обрабатывается в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-137">This parameter is not used because video memory management is handled entirely within kernel mode.</span></span>

</dd> <dt>

<span data-ttu-id="3f9fe-138">*пунумфауркк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-138">*puNumFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f9fe-139">Указатель на элемент **пунумфауркккодес** в [**DD \_ халинфо**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**Ддкапс**.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-139">Pointer to the **puNumFourCCCodes** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span></span> <span data-ttu-id="3f9fe-140">Элемент **пунумфауркккодес** указывает количество кодов с [четырьмя символами (FOURCC)](../directshow/fourcc-codes.md) , поддерживаемых драйвером.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-140">The **puNumFourCCCodes** member specifies the number of [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) codes that the driver supports.</span></span> <span data-ttu-id="3f9fe-141">Дополнительные сведения см. в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-141">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="3f9fe-142">*пуфауркк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-142">*puFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f9fe-143">Указатель на список поддерживаемых форматов поверхностей [с четырьмя символами (FOURCC)](../directshow/fourcc-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="3f9fe-143">Pointer to a list of supported [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) surface formats.</span></span> <span data-ttu-id="3f9fe-144">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-144">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f9fe-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f9fe-145">Return value</span></span>

<span data-ttu-id="3f9fe-146">В случае успеха эта функция возвращает **значение true**. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-146">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f9fe-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f9fe-147">Remarks</span></span>

<span data-ttu-id="3f9fe-148">Вызов этой функции предназначен для выполнения в два этапа.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-148">A call to this function is designed to be made in a two-step process.</span></span> <span data-ttu-id="3f9fe-149">На первом шаге *пуфауркк*, *пувмлист* и *puD3dTextureFormats* должны иметь **значение NULL**, а [**ддкуеридиректдравобжект**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) будет заполнять [**DD \_ халинфо**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**Ддкапс**. **двнумфауркккодес**, **DD \_ халинфо**.**Вмидата**. **двнумхеапс** и [**D3DHAL \_ глобалдривердата**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**Двнумтекстуреформатс** с числом возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-149">In the first step, *puFourCC*, *puvmList* and *puD3dTextureFormats* should be **NULL**, and [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) will fill in [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.**dwNumFourCCCodes**, **DD\_HALINFO**.**vmiData**.**dwNumHeaps**, and [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** with the number of entries that are to be returned.</span></span> <span data-ttu-id="3f9fe-150">Во втором вызове вызывающий объект должен выделить массивы указанного размера и передать эти указатели вместо значений **null** в параметрах *пуфауркк*, *пувмлист* и *puD3dTextureFormats* .</span><span class="sxs-lookup"><span data-stu-id="3f9fe-150">In the second call, the caller should allocate arrays of the indicated size and pass those pointers instead of **NULL** values in the *puFourCC*, *puvmList* and *puD3dTextureFormats* parameters.</span></span> <span data-ttu-id="3f9fe-151">После этого массивы будут заполнены соответствующими данными.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-151">The arrays will then be populated with appropriate data.</span></span>

<span data-ttu-id="3f9fe-152">В приложениях рекомендуется использовать интерфейсы API DirectDraw и [Direct3D](../direct3d10/d3d10-graphics-reference.md) для создания объектов графических устройств и управления ими.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-152">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="3f9fe-153">Эти конструкции являются абстрактным процессом создания устройств в упрощенном и независимом от операционной системе виде.</span><span class="sxs-lookup"><span data-stu-id="3f9fe-153">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f9fe-154">Требования</span><span class="sxs-lookup"><span data-stu-id="3f9fe-154">Requirements</span></span>



| <span data-ttu-id="3f9fe-155">Требование</span><span class="sxs-lookup"><span data-stu-id="3f9fe-155">Requirement</span></span> | <span data-ttu-id="3f9fe-156">Значение</span><span class="sxs-lookup"><span data-stu-id="3f9fe-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f9fe-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f9fe-157">Minimum supported client</span></span><br/> | <span data-ttu-id="3f9fe-158">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3f9fe-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f9fe-159">Minimum supported server</span></span><br/> | <span data-ttu-id="3f9fe-160">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f9fe-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3f9fe-161">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3f9fe-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f9fe-162"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f9fe-162"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f9fe-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f9fe-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f9fe-164">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="3f9fe-164">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="3f9fe-165">**ддкуеридиректдравобжект**</span><span class="sxs-lookup"><span data-stu-id="3f9fe-165">**DdQueryDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[<span data-ttu-id="3f9fe-166">**нтгдиддкреатедиректдравобжект**</span><span class="sxs-lookup"><span data-stu-id="3f9fe-166">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
