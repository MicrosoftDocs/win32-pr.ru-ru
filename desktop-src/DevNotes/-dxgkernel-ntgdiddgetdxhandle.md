---
description: Возвращает маркер API Microsoft DirectX в режиме ядра для использования при последующих вызовах точек входа в режиме ядра, управляющих механизмом API DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Функция Нтгдидджетдксхандле (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655851"
---
# <a name="ntgdiddgetdxhandle-function"></a><span data-ttu-id="fa4a3-103">Функция Нтгдидджетдксхандле</span><span class="sxs-lookup"><span data-stu-id="fa4a3-103">NtGdiDdGetDxHandle function</span></span>

<span data-ttu-id="fa4a3-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="fa4a3-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="fa4a3-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="fa4a3-106">Возвращает маркер API Microsoft DirectX в режиме ядра для использования при последующих вызовах точек входа в режиме ядра, управляющих механизмом API DirectX.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-106">Returns the kernel-mode Microsoft DirectX  API handle to use in subsequent calls to the kernel-mode entry points that control the DirectX  API mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4a3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa4a3-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a><span data-ttu-id="fa4a3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa4a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa4a3-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa4a3-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa4a3-110">Обработчик объекта DirectDraw, который владеет поверхностью.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-110">Handle to DirectDraw object owning the surface.</span></span> <span data-ttu-id="fa4a3-111">Этот параметр является необязательным и может иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-111">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fa4a3-112">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa4a3-112">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa4a3-113">Обработчик, для которого возвращается маркер API DirectX в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-113">Handle to surface for which to return a kernel-mode DirectX API handle.</span></span> <span data-ttu-id="fa4a3-114">Этот параметр является необязательным и может иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-114">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fa4a3-115">*брелеасе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa4a3-115">*bRelease* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa4a3-116">Задайте значение **true** , если необходимо освободить интерфейс режима ядра API DirectX.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-116">Set to **TRUE** if the DirectX API kernel mode interface should be released.</span></span> <span data-ttu-id="fa4a3-117">В противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-117">Otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa4a3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa4a3-118">Return value</span></span>

<span data-ttu-id="fa4a3-119">Обработчик DirectX API, используемый в последующих точках входа ядра, ориентированных на API DirectX.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-119">A DirectX API handle used in subsequent DirectX API-oriented kernel entry points.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa4a3-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa4a3-120">Remarks</span></span>

<span data-ttu-id="fa4a3-121">Если указаны оба *хдиректдрав* и *хсурфаце* , *хсурфаце* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-121">If both *hDirectDraw* and *hSurface* are specified, *hSurface* is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa4a3-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fa4a3-122">Requirements</span></span>



| <span data-ttu-id="fa4a3-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fa4a3-123">Requirement</span></span> | <span data-ttu-id="fa4a3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fa4a3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fa4a3-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa4a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa4a3-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fa4a3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fa4a3-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa4a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa4a3-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fa4a3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fa4a3-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fa4a3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa4a3-130"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa4a3-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa4a3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa4a3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa4a3-132">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="fa4a3-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




