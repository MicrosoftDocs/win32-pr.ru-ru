---
description: Удаляет вложение, созданное с помощью Нтгдиддаттачсурфаце, между двумя объектами поверхности режима ядра.
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: Функция Нтгдиддунаттачсурфаце (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4513020a40c9b704e0b84e1a8b1c582be95db78f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990373"
---
# <a name="ntgdiddunattachsurface-function"></a><span data-ttu-id="84e74-103">Функция Нтгдиддунаттачсурфаце</span><span class="sxs-lookup"><span data-stu-id="84e74-103">NtGdiDdUnattachSurface function</span></span>

<span data-ttu-id="84e74-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="84e74-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="84e74-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="84e74-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="84e74-106">Удаляет вложение, созданное с помощью [**нтгдиддаттачсурфаце**](-dxgkernel-ntgdiddattachsurface.md), между двумя объектами поверхности режима ядра.</span><span class="sxs-lookup"><span data-stu-id="84e74-106">Removes an attachment, created with [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), between two kernel-mode surface objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="84e74-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84e74-107">Syntax</span></span>


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a><span data-ttu-id="84e74-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="84e74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84e74-109">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84e74-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84e74-110">Объект поверхности режима ядра, переданный в качестве параметра Хсурфацефром в [**нтгдиддаттачсурфаце**](-dxgkernel-ntgdiddattachsurface.md).</span><span class="sxs-lookup"><span data-stu-id="84e74-110">The kernel-mode surface object that was passed as the hSurfaceFrom parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span></span>

</dd> <dt>

<span data-ttu-id="84e74-111">*хсурфацеаттачед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84e74-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84e74-112">Объект поверхности режима ядра, переданный в качестве параметра Хсурфацето в [ **нтгдиддаттачсурфаце**](-dxgkernel-ntgdiddattachsurface.md)</span><span class="sxs-lookup"><span data-stu-id="84e74-112">The kernel-mode surface object that was passed as the hSurfaceTo parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84e74-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84e74-113">Return value</span></span>

<span data-ttu-id="84e74-114">**Нтгдиддунаттачсурфаце** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="84e74-114">**NtGdiDdUnattachSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="84e74-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="84e74-115">Return code</span></span>                                                                                              | <span data-ttu-id="84e74-116">Описание</span><span class="sxs-lookup"><span data-stu-id="84e74-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84e74-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="84e74-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="84e74-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="84e74-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="84e74-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="84e74-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="84e74-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="84e74-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="84e74-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="84e74-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="84e74-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="84e74-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="84e74-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="84e74-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="84e74-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="84e74-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="84e74-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84e74-125">Remarks</span></span>

<span data-ttu-id="84e74-126">Рекомендуется, чтобы приложения использовали API DirectDraw, который обрабатывает вложения поверхности на более высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="84e74-126">It is recommended that applications use the DirectDraw  API, which handles surface attachments in a higher-level manner.</span></span>

<span data-ttu-id="84e74-127">Вызывать эту функцию необязательно, так как ядро автоматически уничтожает все вложения при вызове [**нтгдидддестройсурфаце**](-dxgkernel-ntgdidddestroysurface.md) .</span><span class="sxs-lookup"><span data-stu-id="84e74-127">It is not necessary to call this function because the kernel will automatically destroy all attachments when [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="84e74-128">Требования</span><span class="sxs-lookup"><span data-stu-id="84e74-128">Requirements</span></span>



| <span data-ttu-id="84e74-129">Требование</span><span class="sxs-lookup"><span data-stu-id="84e74-129">Requirement</span></span> | <span data-ttu-id="84e74-130">Значение</span><span class="sxs-lookup"><span data-stu-id="84e74-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84e74-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84e74-131">Minimum supported client</span></span><br/> | <span data-ttu-id="84e74-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="84e74-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="84e74-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84e74-133">Minimum supported server</span></span><br/> | <span data-ttu-id="84e74-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="84e74-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="84e74-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="84e74-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="84e74-136"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="84e74-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84e74-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84e74-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84e74-138">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="84e74-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




