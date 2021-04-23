---
description: Извлекает общую поверхность DirectX, которая осуществляет резервное копирование заданного окна. Эту область можно записать в, чтобы обновить содержимое окна.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: Функция Двмдксжетвиндовшаредсурфаце
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711553"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a><span data-ttu-id="f5ef8-104">Функция Двмдксжетвиндовшаредсурфаце</span><span class="sxs-lookup"><span data-stu-id="f5ef8-104">DwmDxGetWindowSharedSurface function</span></span>

<span data-ttu-id="f5ef8-105">Извлекает общую поверхность DirectX, которая осуществляет резервное копирование заданного окна.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-105">Retrieves the DirectX shared surface backing a given window.</span></span> <span data-ttu-id="f5ef8-106">Эту область можно записать в, чтобы обновить содержимое окна.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-106">This surface can be written to in order to update the contents of the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ef8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5ef8-107">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a><span data-ttu-id="f5ef8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5ef8-108">Parameters</span></span>

`hwnd`

<span data-ttu-id="f5ef8-109">[**HWND**](/windows/desktop/winprog/windows-data-types) , указывающий обновляемое окно.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-109">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window to be updated.</span></span>

`luidAdapter`

<span data-ttu-id="f5ef8-110">[**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) адаптера, на котором должна располагаться поверхность.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-110">The [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) of the adapter where the surface should be located.</span></span>

`hmonitorAssociation`

<span data-ttu-id="f5ef8-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-111">Reserved.</span></span>

`dwFlags`

<span data-ttu-id="f5ef8-112">Этот параметр может принимать одно из следующих значений или побитовое сочетание или несколько значений, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-112">This parameter can be one of the following values, or a bitwise OR combination of multiple values where appropriate.</span></span>

| <span data-ttu-id="f5ef8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f5ef8-113">Value</span></span> | <span data-ttu-id="f5ef8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f5ef8-114">Meaning</span></span> |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <span data-ttu-id="f5ef8-115"><dt>**DWM \_ \_ \_ Время ожидания для флага перенаправления**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5ef8-115"><dt>**DWM\_REDIRECTION\_FLAG\_WAIT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f5ef8-116">Заставляет функцию блокироваться до тех пор, пока не будет пройдена вертикальная синхронизация (вертикальной синхронизации) со времени последнего вызова функции.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-116">Causes the function to block until a vertical synchronization (VSync) has passed since the last time the function was called successfully.</span></span> |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <span data-ttu-id="f5ef8-117"><dt>**DWM \_ \_Поддержка флага перенаправления \_ \_ \_ на \_ \_ поверхности GDI,**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="f5ef8-117"><dt>**DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="f5ef8-118">Указывает, что вызывающее приложение может выполнять демонстрацию к общей поверхности GDI.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-118">Indicates that the calling application is capable of presenting to a GDI shared surface.</span></span> |

`pfmtWindow`

<span data-ttu-id="f5ef8-119">На входе — желаемый формат поверхности.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-119">On input, the desired format of the surface.</span></span> <span data-ttu-id="f5ef8-120">На выходе фактический формат возвращаемой поверхности.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-120">On output, the actual format of the returned surface.</span></span>

`phDxSurface`

<span data-ttu-id="f5ef8-121">В выходных данных — общий маркер для поверхности.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-121">On output, the shared handle to the surface.</span></span>

`puiUpdateId`

<span data-ttu-id="f5ef8-122">На выходе — идентификатор обновления.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-122">On output, the ID of the update.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5ef8-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5ef8-123">Return value</span></span>

<span data-ttu-id="f5ef8-124">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-124">This function can return one of these values.</span></span>

| <span data-ttu-id="f5ef8-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f5ef8-125">Return code</span></span> | <span data-ttu-id="f5ef8-126">Описание</span><span class="sxs-lookup"><span data-stu-id="f5ef8-126">Description</span></span> |
|-|-|
| <span data-ttu-id="f5ef8-127">**\_ОК**</span><span class="sxs-lookup"><span data-stu-id="f5ef8-127">**S\_OK**</span></span> | <span data-ttu-id="f5ef8-128">Вызов выполнен успешно, и вы должны обновить поверхность, убедиться, что идентификатор обновления передается в [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (в элементе **пресенсисторитокен** структуры подготовки к **\_ просмотру** при отправке обновления, а [**двмдксупдатевиндовшаредсурфаце**](dwmdxupdatewindowsharedsurface.md) должен вызываться с тем же идентификатором обновления.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-128">The call succeeded, and you should update the surface, being sure to pass the update ID to [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (in the **PresentHistoryToken** member of the **D3DKMT\_RENDER** structure when the update is submitted, and then [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) should be called with the same update ID.</span></span> <span data-ttu-id="f5ef8-129">Обратите внимание, что **двмдксупдатевиндовшаредсурфаце** должен вызываться независимо от фактического обновления поверхности.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-129">Note that **DwmDxUpdateWindowSharedSurface** should be called regardless of whether the surface was actually updated or not.</span></span> |
| <span data-ttu-id="f5ef8-130">**\_ \_ \_ поверхность перенаправления GDI DWM S \_**</span><span class="sxs-lookup"><span data-stu-id="f5ef8-130">**DWM\_S\_GDI\_REDIRECTION\_SURFACE**</span></span> | <span data-ttu-id="f5ef8-131">Вызов был произведен, и необходимо обновить поверхность, вызвав [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)и установив для модели **Пресенсисторитокен** Member значение  **D3DKMT \_ PM \_ redirectd \_ БЛТ** и указав идентификатор обновления в элементе **БЛТ** объединения.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-131">The call succeeded, and you should update the surface by calling [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent), and setting **PresentHistoryToken** member's **Model** to **D3DKMT\_PM\_REDIRECTED\_BLT**, and providing the update ID in the **Blt** member of the union.</span></span> <span data-ttu-id="f5ef8-132">Это значение возвращается, только если в *dwFlags* указана **\_ \_ Поддержка флага перенаправления DWM \_ \_ \_ для \_ \_ поверхности GDI** .</span><span class="sxs-lookup"><span data-stu-id="f5ef8-132">This value is only returned if **DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE** was specified in *dwFlags*.</span></span> |
| <span data-ttu-id="f5ef8-133">**\_адаптер DWM \_ E \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="f5ef8-133">**DWM\_E\_ADAPTER\_NOT\_FOUND**</span></span> | <span data-ttu-id="f5ef8-134">Недопустимое значение *луидадаптер* .</span><span class="sxs-lookup"><span data-stu-id="f5ef8-134">The value of *luidAdapter* is not valid.</span></span> |
| <span data-ttu-id="f5ef8-135">**DWM \_ E \_ компоситиондисаблед**</span><span class="sxs-lookup"><span data-stu-id="f5ef8-135">**DWM\_E\_COMPOSITIONDISABLED**</span></span> | <span data-ttu-id="f5ef8-136">DWM сейчас не включен, и приложение должно предоставить другой способ.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-136">DWM is not currently enabled, and the application will need to present another way.</span></span> |

## <a name="remarks"></a><span data-ttu-id="f5ef8-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5ef8-137">Remarks</span></span>

<span data-ttu-id="f5ef8-138">Этот API предназначен для реализации графического драйвера или среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-138">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="f5ef8-139">Приложение не может вызывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-139">An application may not call this method.</span></span> <span data-ttu-id="f5ef8-140">Эта документация действительна только для Windows 7, и этот API не гарантирует существование и не работает аналогичным образом в других версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-140">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="f5ef8-141">Эта функция отсутствует в заголовке или библиотеке статической компоновки, она находится по порядковому номеру 100 в dwmapi.dll.</span><span class="sxs-lookup"><span data-stu-id="f5ef8-141">This function is not present in any header or static-link library, and it is located at ordinal 100 in dwmapi.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ef8-142">Требования</span><span class="sxs-lookup"><span data-stu-id="f5ef8-142">Requirements</span></span>

| <span data-ttu-id="f5ef8-143">Требование</span><span class="sxs-lookup"><span data-stu-id="f5ef8-143">Requirement</span></span> | <span data-ttu-id="f5ef8-144">Значение</span><span class="sxs-lookup"><span data-stu-id="f5ef8-144">Value</span></span> |
|-|-|
| <span data-ttu-id="f5ef8-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5ef8-145">Minimum supported client</span></span> | <span data-ttu-id="f5ef8-146">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f5ef8-146">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="f5ef8-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5ef8-147">Minimum supported server</span></span> | <span data-ttu-id="f5ef8-148">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f5ef8-148">None supported</span></span> |
| <span data-ttu-id="f5ef8-149">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f5ef8-149">End of client support</span></span> | <span data-ttu-id="f5ef8-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5ef8-150">Windows 7</span></span> |
| <span data-ttu-id="f5ef8-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f5ef8-151">Header</span></span> | <span data-ttu-id="f5ef8-152">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f5ef8-152">N/A</span></span> |
| <span data-ttu-id="f5ef8-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f5ef8-153">DLL</span></span> | <span data-ttu-id="f5ef8-154">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="f5ef8-154">Dwmapi.dll</span></span> |
