---
description: Уведомляет DWM о входящем обновлении к общей поверхности окна.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: Функция Двмдксупдатевиндовшаредсурфаце
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
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544199"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a><span data-ttu-id="36f1d-103">Функция Двмдксупдатевиндовшаредсурфаце</span><span class="sxs-lookup"><span data-stu-id="36f1d-103">DwmDxUpdateWindowSharedSurface function</span></span>

<span data-ttu-id="36f1d-104">Уведомляет DWM о входящем обновлении к общей поверхности окна.</span><span class="sxs-lookup"><span data-stu-id="36f1d-104">Notifies the DWM of an incoming update to a window shared surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36f1d-105">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a><span data-ttu-id="36f1d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36f1d-106">Parameters</span></span>

`hwnd`

<span data-ttu-id="36f1d-107">[**HWND**](/windows/desktop/winprog/windows-data-types) , указывающий обновляемое окно.</span><span class="sxs-lookup"><span data-stu-id="36f1d-107">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window being updated.</span></span>

`uiUpdateId`

<span data-ttu-id="36f1d-108">ИДЕНТИФИКАТОР обновления, полученный из [**двмдксжетвиндовшаредсурфаце**](dwmdxgetwindowsharedsurface.md).</span><span class="sxs-lookup"><span data-stu-id="36f1d-108">The update ID retrieved from [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span></span>

`dwFlags`

<span data-ttu-id="36f1d-109">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="36f1d-109">Reserved.</span></span>

`hmonitorAssociation`

<span data-ttu-id="36f1d-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="36f1d-110">Reserved.</span></span>

`prc`

<span data-ttu-id="36f1d-111">Rect обновляемого окна в пространстве координат окна.</span><span class="sxs-lookup"><span data-stu-id="36f1d-111">The rect of the window being updated, in window coordinate space.</span></span> <span data-ttu-id="36f1d-112">Прямоугольник со значением NULL указывает, что регион не обновлялся.</span><span class="sxs-lookup"><span data-stu-id="36f1d-112">A NULL rectangle indicates that no region was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="36f1d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36f1d-113">Return value</span></span>

<span data-ttu-id="36f1d-114">**С \_ ОК** в случае успеха, в противном случае — значение **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="36f1d-114">**S\_OK** if successful, otherwise a FAILED **HRESULT.**</span></span>

## <a name="remarks"></a><span data-ttu-id="36f1d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36f1d-115">Remarks</span></span>

<span data-ttu-id="36f1d-116">Этот API предназначен для реализации графического драйвера или среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="36f1d-116">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="36f1d-117">Приложение не может вызывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="36f1d-117">An application may not call this method.</span></span> <span data-ttu-id="36f1d-118">Эта документация действительна только для Windows 7, и этот API не гарантирует существование и не работает аналогичным образом в других версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="36f1d-118">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="36f1d-119">Эта функция отсутствует в заголовке или библиотеке статической компоновки, она находится по порядковому номеру 101 в dwmapi.dll.</span><span class="sxs-lookup"><span data-stu-id="36f1d-119">This function is not present in any header or static-link library, and it is located at ordinal 101 in dwmapi.dll.</span></span>

<span data-ttu-id="36f1d-120">Этот метод следует вызывать только после того, как [**двмдксжетвиндовшаредсурфаце**](dwmdxgetwindowsharedsurface.md) возвращает " **\_ ОК**", и должен вызываться в этом сценарии независимо от того, обновлена ли поверхность.</span><span class="sxs-lookup"><span data-stu-id="36f1d-120">This method should only ever be called after [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) returns **S\_OK**, and must be called in that scenario, regardless of whether the surface is updated or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f1d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="36f1d-121">Requirements</span></span>

| <span data-ttu-id="36f1d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="36f1d-122">Requirement</span></span> | <span data-ttu-id="36f1d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="36f1d-123">Value</span></span> |
|-|-|
| <span data-ttu-id="36f1d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36f1d-124">Minimum supported client</span></span> | <span data-ttu-id="36f1d-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="36f1d-125">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="36f1d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36f1d-126">Minimum supported server</span></span> | <span data-ttu-id="36f1d-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="36f1d-127">None supported</span></span> |
| <span data-ttu-id="36f1d-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="36f1d-128">End of client support</span></span> | <span data-ttu-id="36f1d-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="36f1d-129">Windows 7</span></span> |
| <span data-ttu-id="36f1d-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="36f1d-130">Header</span></span> | <span data-ttu-id="36f1d-131">Н/Д</span><span class="sxs-lookup"><span data-stu-id="36f1d-131">N/A</span></span> |
| <span data-ttu-id="36f1d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="36f1d-132">DLL</span></span> | <span data-ttu-id="36f1d-133">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="36f1d-133">Dwmapi.dll</span></span> |
