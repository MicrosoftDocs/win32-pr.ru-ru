---
description: Управляет элементами управления яркостью и яркостью на поверхности наложения.
ms.assetid: 2f617c89-5505-4d84-be7d-473b216c0571
title: Функция Нтгдиддколорконтрол (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdColorControl
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 45ed8683a892b07fa63fbe79b657669e647126cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140955"
---
# <a name="ntgdiddcolorcontrol-function"></a><span data-ttu-id="e8827-103">Функция Нтгдиддколорконтрол</span><span class="sxs-lookup"><span data-stu-id="e8827-103">NtGdiDdColorControl function</span></span>

<span data-ttu-id="e8827-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e8827-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e8827-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="e8827-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e8827-106">Управляет элементами управления яркостью и яркостью на поверхности наложения.</span><span class="sxs-lookup"><span data-stu-id="e8827-106">Controls the luminance and brightness controls of an overlay surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8827-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8827-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdColorControl(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_COLORCONTROLDATA puColorControlData
);
```



## <a name="parameters"></a><span data-ttu-id="e8827-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8827-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8827-109">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8827-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8827-110">Маркер [**\_ \_ локальной структуры области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , представляющей поверхность наложения.</span><span class="sxs-lookup"><span data-stu-id="e8827-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure representing the overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="e8827-111">*пуколорконтролдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e8827-111">*puColorControlData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8827-112">Указатель на структуру [**DD \_ колорконтролдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_colorcontroldata) , которая содержит сведения об элементе управления цветом для указанной поверхности наложения.</span><span class="sxs-lookup"><span data-stu-id="e8827-112">Pointer to a [**DD\_COLORCONTROLDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_colorcontroldata) structure that contains the color control information for a specified overlay surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8827-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8827-113">Return value</span></span>

<span data-ttu-id="e8827-114">**Нтгдиддколорконтрол** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e8827-114">**NtGdiDdColorControl** returns one of the following callback codes.</span></span>



| <span data-ttu-id="e8827-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e8827-115">Return code</span></span>                                                                                              | <span data-ttu-id="e8827-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e8827-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8827-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="e8827-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="e8827-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="e8827-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="e8827-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="e8827-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="e8827-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="e8827-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e8827-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="e8827-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="e8827-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="e8827-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="e8827-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e8827-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="e8827-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="e8827-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e8827-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e8827-125">Requirements</span></span>



| <span data-ttu-id="e8827-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e8827-126">Requirement</span></span> | <span data-ttu-id="e8827-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e8827-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8827-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8827-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e8827-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8827-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e8827-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8827-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e8827-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8827-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e8827-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e8827-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8827-133"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8827-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8827-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8827-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8827-135">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="e8827-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
