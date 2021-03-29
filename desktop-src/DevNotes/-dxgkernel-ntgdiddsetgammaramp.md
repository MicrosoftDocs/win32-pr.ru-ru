---
description: Задает гамму-шкалу для устройства.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: Функция Нтгдиддсетгаммарамп (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140939"
---
# <a name="ntgdiddsetgammaramp-function"></a><span data-ttu-id="874da-103">Функция Нтгдиддсетгаммарамп</span><span class="sxs-lookup"><span data-stu-id="874da-103">NtGdiDdSetGammaRamp function</span></span>

<span data-ttu-id="874da-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="874da-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="874da-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="874da-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="874da-106">Задает гамму-шкалу для устройства.</span><span class="sxs-lookup"><span data-stu-id="874da-106">Sets the gamma ramp for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="874da-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="874da-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a><span data-ttu-id="874da-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="874da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="874da-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="874da-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="874da-110">Обработчик объекта драйвера режима ядра, для которого задается пандус.</span><span class="sxs-lookup"><span data-stu-id="874da-110">Handle to the kernel-mode driver object for which the ramp is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="874da-111">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="874da-111">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="874da-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="874da-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="874da-113">*лпгаммарамп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="874da-113">*lpGammaRamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="874da-114">Указатель на массив структур **ддгаммарамп** .</span><span class="sxs-lookup"><span data-stu-id="874da-114">Pointer to an array of **DDGAMMARAMP** structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="874da-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="874da-115">Return value</span></span>

<span data-ttu-id="874da-116">Если функция выполнена успешно, возвращается значение **true** .</span><span class="sxs-lookup"><span data-stu-id="874da-116">The return value is **TRUE** if the function is successful.</span></span> <span data-ttu-id="874da-117">В противном случае он имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="874da-117">Otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="874da-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="874da-118">Remarks</span></span>

<span data-ttu-id="874da-119">Рекомендуется, чтобы приложения использовали методы **идиректдравгаммаконтрол:: сетгаммарамп** или [**IDirect3DDevice9:: сетгаммарамп**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) , так как эти методы предлагают те же функциональные возможности, которые не зависят от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="874da-119">It is recommended that applications use the **IDirectDrawGammaControl::SetGammaRamp** or [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) methods instead because these methods offer the same functionality independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="874da-120">Требования</span><span class="sxs-lookup"><span data-stu-id="874da-120">Requirements</span></span>



| <span data-ttu-id="874da-121">Требование</span><span class="sxs-lookup"><span data-stu-id="874da-121">Requirement</span></span> | <span data-ttu-id="874da-122">Значение</span><span class="sxs-lookup"><span data-stu-id="874da-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="874da-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="874da-123">Minimum supported client</span></span><br/> | <span data-ttu-id="874da-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="874da-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="874da-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="874da-125">Minimum supported server</span></span><br/> | <span data-ttu-id="874da-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="874da-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="874da-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="874da-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="874da-128"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="874da-128"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="874da-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="874da-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="874da-130">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="874da-130">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
