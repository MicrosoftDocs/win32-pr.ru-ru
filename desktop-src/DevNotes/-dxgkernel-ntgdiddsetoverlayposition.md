---
description: Задает расположение оверлея.
ms.assetid: dd495118-9ceb-4100-a7ec-794659bb4461
title: Функция Нтгдиддсетоверлайпоситион (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetOverlayPosition
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 73882e20fd7065d208835c2005d102b1312e8ce1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072365"
---
# <a name="ntgdiddsetoverlayposition-function"></a><span data-ttu-id="6cf81-103">Функция Нтгдиддсетоверлайпоситион</span><span class="sxs-lookup"><span data-stu-id="6cf81-103">NtGdiDdSetOverlayPosition function</span></span>

<span data-ttu-id="6cf81-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6cf81-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="6cf81-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="6cf81-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="6cf81-106">Задает расположение оверлея.</span><span class="sxs-lookup"><span data-stu-id="6cf81-106">Sets the position for an overlay.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cf81-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cf81-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetOverlayPosition(
  _In_    HANDLE                     hSurfaceSource,
  _In_    HANDLE                     hSurfaceDestination,
  _Inout_ PDD_SETOVERLAYPOSITIONDATA puSetOverlayPositionData
);
```



## <a name="parameters"></a><span data-ttu-id="6cf81-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cf81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cf81-109">*хсурфацесаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6cf81-109">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf81-110">Обозначает [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , представляющую поверхность наложения DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="6cf81-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="6cf81-111">*хсурфацедестинатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6cf81-111">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf81-112">Указатель на [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , представляющую занятую область.</span><span class="sxs-lookup"><span data-stu-id="6cf81-112">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure representing the surface that is being overlaid.</span></span>

</dd> <dt>

<span data-ttu-id="6cf81-113">*пусетоверлайпоситиондата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6cf81-113">*puSetOverlayPositionData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cf81-114">Указатель на структуру [**DD \_ сетоверлайпоситиондата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) , которая содержит сведения, необходимые для задания позиции оверлея.</span><span class="sxs-lookup"><span data-stu-id="6cf81-114">Pointer to a [**DD\_SETOVERLAYPOSITIONDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) structure that contains the information required to set the overlay position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cf81-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cf81-115">Return value</span></span>

<span data-ttu-id="6cf81-116">**Нтгдиддсетоверлайпоситион** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6cf81-116">**NtGdiDdSetOverlayPosition** returns one of the following callback codes.</span></span>



| <span data-ttu-id="6cf81-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6cf81-117">Return code</span></span>                                                                                              | <span data-ttu-id="6cf81-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6cf81-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6cf81-119"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="6cf81-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="6cf81-120">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="6cf81-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="6cf81-121">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="6cf81-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="6cf81-122">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="6cf81-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="6cf81-123"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="6cf81-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="6cf81-124">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="6cf81-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="6cf81-125">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6cf81-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="6cf81-126">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="6cf81-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6cf81-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6cf81-127">Requirements</span></span>



| <span data-ttu-id="6cf81-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6cf81-128">Requirement</span></span> | <span data-ttu-id="6cf81-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6cf81-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf81-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cf81-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf81-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6cf81-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6cf81-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cf81-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf81-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6cf81-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6cf81-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6cf81-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cf81-135"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cf81-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf81-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cf81-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf81-137">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="6cf81-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
