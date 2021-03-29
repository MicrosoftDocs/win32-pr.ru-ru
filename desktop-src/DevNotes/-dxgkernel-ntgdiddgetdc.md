---
description: Создает контекст устройства (DC) для указанной поверхности.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Функция Нтгдидджетдк (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141487"
---
# <a name="ntgdiddgetdc-function"></a><span data-ttu-id="198d1-103">Функция Нтгдидджетдк</span><span class="sxs-lookup"><span data-stu-id="198d1-103">NtGdiDdGetDC function</span></span>

<span data-ttu-id="198d1-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="198d1-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="198d1-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="198d1-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="198d1-106">Создает контекст устройства (DC) для указанной поверхности.</span><span class="sxs-lookup"><span data-stu-id="198d1-106">Creates a device context (DC) for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="198d1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="198d1-107">Syntax</span></span>


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a><span data-ttu-id="198d1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="198d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="198d1-109">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="198d1-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="198d1-110">Обработчик для поверхности DirectDraw в режиме ядра, который ранее возвращался [**нтгдиддкреатесурфаце**](-dxgkernel-ntgdiddcreatesurface.md) или [**нтгдиддкреатесурфацеобжект**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span><span class="sxs-lookup"><span data-stu-id="198d1-110">Handle to a kernel-mode DirectDraw surface previously returned by [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) or [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="198d1-111">*пуколортабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="198d1-111">*puColorTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="198d1-112">Указатель на таблицу цветов переопределения для возвращенного контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="198d1-112">Pointer to an override color table for the returned DC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="198d1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="198d1-113">Return value</span></span>

<span data-ttu-id="198d1-114">В случае успеха эта функция возвращает допустимый **HDC**; в противном случае возвращается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="198d1-114">If successful, this function returns a valid **HDC**; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="198d1-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="198d1-115">Remarks</span></span>

<span data-ttu-id="198d1-116">В любой момент времени на одну поверхность может быть только один контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="198d1-116">Only one DC is allowed per surface at any given time.</span></span> <span data-ttu-id="198d1-117">Последующие вызовы **нтгдидджетдк** будут завершаться ошибкой, пока не будет освобожден предыдущий контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="198d1-117">Subsequent calls to **NtGdiDdGetDC** will fail until the previous DC is released.</span></span>

<span data-ttu-id="198d1-118">Приложениям рекомендуется вызывать метод [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) , который предоставляет те же функциональные возможности, что и не зависит от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="198d1-118">Applications are advised to call [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) instead, which provides the same functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="198d1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="198d1-119">Requirements</span></span>



| <span data-ttu-id="198d1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="198d1-120">Requirement</span></span> | <span data-ttu-id="198d1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="198d1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="198d1-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="198d1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="198d1-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="198d1-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="198d1-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="198d1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="198d1-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="198d1-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="198d1-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="198d1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="198d1-127"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="198d1-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="198d1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="198d1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="198d1-129">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="198d1-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="198d1-130">**дджетдк**</span><span class="sxs-lookup"><span data-stu-id="198d1-130">**DdGetDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
