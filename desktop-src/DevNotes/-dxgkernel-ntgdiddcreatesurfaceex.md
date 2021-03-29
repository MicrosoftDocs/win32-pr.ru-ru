---
description: Создает поверхность Microsoft Direct3D из поверхности Microsoft DirectDraw и связывает с ней значение запрошенного обработчика.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Функция Нтгдиддкреатесурфацеекс (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8aad613762773e466fb83eadf689b7703a8c4198
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140946"
---
# <a name="ntgdiddcreatesurfaceex-function"></a><span data-ttu-id="43f5b-103">Функция Нтгдиддкреатесурфацеекс</span><span class="sxs-lookup"><span data-stu-id="43f5b-103">NtGdiDdCreateSurfaceEx function</span></span>

<span data-ttu-id="43f5b-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="43f5b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="43f5b-105">Вместо этого используйте DirectDraw и Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="43f5b-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="43f5b-106">Создает поверхность Microsoft Direct3D из поверхности Microsoft DirectDraw и связывает с ней значение запрошенного обработчика.</span><span class="sxs-lookup"><span data-stu-id="43f5b-106">Creates a Microsoft Direct3D surface from a Microsoft DirectDraw surface and associates a requested handle value to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f5b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43f5b-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a><span data-ttu-id="43f5b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="43f5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f5b-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43f5b-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f5b-110">Обработчик для объекта DirectDraw, созданного приложением.</span><span class="sxs-lookup"><span data-stu-id="43f5b-110">Handle to the DirectDraw object created by the application.</span></span>

</dd> <dt>

<span data-ttu-id="43f5b-111">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43f5b-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f5b-112">Обработчик для поверхности DirectDraw, создаваемой для Direct3D.</span><span class="sxs-lookup"><span data-stu-id="43f5b-112">Handle to the DirectDraw surface to be created for Direct3D.</span></span> <span data-ttu-id="43f5b-113">Эти дескрипторы уникальны в разных [**\_ \_ локальных структурах DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) .</span><span class="sxs-lookup"><span data-stu-id="43f5b-113">These handles are unique within each different [**DD\_DIRECTDRAW\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) structure.</span></span>

</dd> <dt>

<span data-ttu-id="43f5b-114">*двсурфацехандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43f5b-114">*dwSurfaceHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f5b-115">Обработайте структуру [**DD \_ креатесурфацеексдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) , которая содержит сведения, необходимые драйверу для создания поверхности.</span><span class="sxs-lookup"><span data-stu-id="43f5b-115">Handle to a [**DD\_CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) structure that contains the information required for the driver to create the surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f5b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43f5b-116">Return value</span></span>

<span data-ttu-id="43f5b-117">**Нтгдиддкреатесурфацеекс** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="43f5b-117">**NtGdiDdCreateSurfaceEx** returns one of the following callback codes.</span></span>



| <span data-ttu-id="43f5b-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="43f5b-118">Return code</span></span>                                                                                              | <span data-ttu-id="43f5b-119">Описание</span><span class="sxs-lookup"><span data-stu-id="43f5b-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43f5b-120"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="43f5b-120"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="43f5b-121">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="43f5b-121">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="43f5b-122">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="43f5b-122">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="43f5b-123">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="43f5b-123">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="43f5b-124"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="43f5b-124"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="43f5b-125">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="43f5b-125">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="43f5b-126">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="43f5b-126">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="43f5b-127">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="43f5b-127">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="43f5b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="43f5b-128">Requirements</span></span>



| <span data-ttu-id="43f5b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="43f5b-129">Requirement</span></span> | <span data-ttu-id="43f5b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="43f5b-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43f5b-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43f5b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="43f5b-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43f5b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="43f5b-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43f5b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="43f5b-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43f5b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43f5b-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="43f5b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="43f5b-136"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="43f5b-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43f5b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43f5b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f5b-138">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="43f5b-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
