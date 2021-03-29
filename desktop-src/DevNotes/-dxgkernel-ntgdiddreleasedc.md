---
description: Освобождает ранее созданный контекст устройства (DC) для указанного объекта поверхности Microsoft DirectDraw в режиме ядра.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: Функция Нтгдиддрелеаседк (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895385"
---
# <a name="ntgdiddreleasedc-function"></a><span data-ttu-id="3a146-103">Функция Нтгдиддрелеаседк</span><span class="sxs-lookup"><span data-stu-id="3a146-103">NtGdiDdReleaseDC function</span></span>

<span data-ttu-id="3a146-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3a146-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3a146-105">Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="3a146-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3a146-106">Освобождает ранее созданный контекст устройства (DC) для указанного объекта поверхности Microsoft DirectDraw в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="3a146-106">Releases the previously created device context (DC) for the indicated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a146-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a146-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="3a146-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a146-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a146-109">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a146-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a146-110">Обработчик для ранее созданного объекта поверхности DirectDraw режима ядра.</span><span class="sxs-lookup"><span data-stu-id="3a146-110">Handle to the previously created kernel-mode DirectDraw surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a146-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a146-111">Return value</span></span>

<span data-ttu-id="3a146-112">В случае успеха эта функция возвращает **значение true**. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3a146-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a146-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a146-113">Remarks</span></span>

<span data-ttu-id="3a146-114">Приложения, которым требуется получить контроллер домена для поверхности DirectDraw, могут использовать [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), который предоставляет эту функциональность независимо от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3a146-114">Applications that need to obtain a DC for a DirectDraw surface may use [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), which exposes this functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a146-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3a146-115">Requirements</span></span>



| <span data-ttu-id="3a146-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3a146-116">Requirement</span></span> | <span data-ttu-id="3a146-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3a146-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a146-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a146-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a146-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3a146-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3a146-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a146-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a146-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3a146-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a146-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3a146-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a146-123"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a146-123"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a146-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a146-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a146-125">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="3a146-125">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="3a146-126">**ддрелеаседк**</span><span class="sxs-lookup"><span data-stu-id="3a146-126">**DdReleaseDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
