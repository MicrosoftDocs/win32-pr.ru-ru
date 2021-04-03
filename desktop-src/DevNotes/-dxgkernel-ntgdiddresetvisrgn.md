---
description: Используется, чтобы позволить пользовательскому режиму получить действительное представление о области отсечения для Windows на рабочем столе. Эта Обрезка может изменяться асинхронно с точки зрения потоков пользовательского режима.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Функция Нтгдиддресетвисргн (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895381"
---
# <a name="ntgdiddresetvisrgn-function"></a><span data-ttu-id="50ba9-104">Функция Нтгдиддресетвисргн</span><span class="sxs-lookup"><span data-stu-id="50ba9-104">NtGdiDdResetVisrgn function</span></span>

<span data-ttu-id="50ba9-105">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="50ba9-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="50ba9-106">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="50ba9-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="50ba9-107">Используется, чтобы позволить пользовательскому режиму получить действительное представление о области отсечения для Windows на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="50ba9-107">Used to enable the user mode to gain a valid understanding of the clipping region for windows on the desktop.</span></span> <span data-ttu-id="50ba9-108">Эта Обрезка может изменяться асинхронно с точки зрения потоков пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="50ba9-108">This clipping can change asynchronously from the point of view of user-mode threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ba9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50ba9-109">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="50ba9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="50ba9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50ba9-111">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50ba9-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50ba9-112">Указатель на объект пользовательского режима любой поверхности, принадлежащей устройству DirectDraw, для которого требуется сбросить обрезку.</span><span class="sxs-lookup"><span data-stu-id="50ba9-112">Pointer to the user-mode object of any surface belonging to the DirectDraw device for which clipping is to be reset.</span></span> <span data-ttu-id="50ba9-113">Дополнительные сведения см. в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="50ba9-113">For details, see the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="50ba9-114">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50ba9-114">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50ba9-115">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="50ba9-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50ba9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50ba9-116">Return value</span></span>

<span data-ttu-id="50ba9-117">В случае успеха эта функция возвращает **значение true**. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="50ba9-117">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="50ba9-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50ba9-118">Remarks</span></span>

<span data-ttu-id="50ba9-119">Обрезка может изменяться асинхронно с точки зрения потоков пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="50ba9-119">Clipping can change asynchronously from the point of view of user-mode threads.</span></span> <span data-ttu-id="50ba9-120">Компоненты DirectDraw и Windows интерфейс графических устройств (GDI) режима ядра поддерживают счетчик, который увеличивается при каждом изменении списка обрезки для всего рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="50ba9-120">The kernel-mode parts of DirectDraw and Windows Graphics Device Interface (GDI) maintain a counter that is incremented whenever the clipping list for the entire desktop changes.</span></span> <span data-ttu-id="50ba9-121">Вызов этой функции записывает этот счетчик в каждую существующую основную поверхность DirectDraw в системе.</span><span class="sxs-lookup"><span data-stu-id="50ba9-121">A call to this function records this counter with every existing DirectDraw primary surface on the system.</span></span>

<span data-ttu-id="50ba9-122">В любое время, когда одна из этих основных поверхностей будет изменена операцией [IDirectDrawSurface7:: БЛТ](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) или [IDirectDrawSurface7:: Lock](/previous-versions/ms858221(v=msdn.10)) (см. документацию по DDK), счетчик, записанный с помощью области, сравнивается с глобальным счетчиком.</span><span class="sxs-lookup"><span data-stu-id="50ba9-122">At any later time when one of these primary surfaces is modified by a [IDirectDrawSurface7::Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) or [IDirectDrawSurface7::Lock](/previous-versions/ms858221(v=msdn.10)) operation (see DDK documentation), then the counter recorded with the surface is compared with the global counter.</span></span> <span data-ttu-id="50ba9-123">Если эти значения различаются, код ошибки ДДЕРР \_ висргнчанжед возвращается в код пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="50ba9-123">If these values are different, an error code DDERR\_VISRGNCHANGED is returned to the user-mode code.</span></span> <span data-ttu-id="50ba9-124">Затем код пользовательского режима повторно запросит текущую обрезку для рабочего стола, вызовите **нтгдиддресетвисргн** и повторите попытку IDirectDrawSurface7:: БЛТ, примененную к основной поверхности, с учетом новой обрезки.</span><span class="sxs-lookup"><span data-stu-id="50ba9-124">The user-mode code will then re-query the current clipping for the desktop, call **NtGdiDdResetVisrgn**, and re-try the IDirectDrawSurface7::Blt applied to the primary surface, respecting the new clipping.</span></span> <span data-ttu-id="50ba9-125">В конечном итоге обрезка, которая была вычислена в коде пользовательского режима, будет совпадать с текущей обрезка, принадлежащей режиму ядра, и IDirectDrawSurface7:: БЛТ будет разрешено продолжить.</span><span class="sxs-lookup"><span data-stu-id="50ba9-125">Eventually, the clipping that was sampled by the user-mode code will be the same as the current clipping owned by kernel mode, and the IDirectDrawSurface7::Blt will be allowed to continue.</span></span>

<span data-ttu-id="50ba9-126">Приложениям рекомендуется использовать интерфейс [идиректдравклиппер](/previous-versions/aa919448(v=msdn.10)) или метод повторной отправки [IDirect3DDevice8::P](/previous-versions/ms889707(v=msdn.10)) для управления асинхронными обрезками.</span><span class="sxs-lookup"><span data-stu-id="50ba9-126">Applications are advised to use the [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) interface or [IDirect3DDevice8::Present](/previous-versions/ms889707(v=msdn.10)) method to handle asynchronous clipping changes.</span></span> <span data-ttu-id="50ba9-127">Эти конструкции реализуют асинхронное обрезание в автоматизированном и независимом от операционной системы виде.</span><span class="sxs-lookup"><span data-stu-id="50ba9-127">These constructs implement asynchronous clipping in an automated and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="50ba9-128">Требования</span><span class="sxs-lookup"><span data-stu-id="50ba9-128">Requirements</span></span>



| <span data-ttu-id="50ba9-129">Требование</span><span class="sxs-lookup"><span data-stu-id="50ba9-129">Requirement</span></span> | <span data-ttu-id="50ba9-130">Значение</span><span class="sxs-lookup"><span data-stu-id="50ba9-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50ba9-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50ba9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="50ba9-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50ba9-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="50ba9-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50ba9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="50ba9-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50ba9-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="50ba9-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="50ba9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="50ba9-136"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="50ba9-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50ba9-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50ba9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ba9-138">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="50ba9-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="50ba9-139">**ддресетвисргн**</span><span class="sxs-lookup"><span data-stu-id="50ba9-139">**DdResetVisrgn**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
