---
description: Уничтожает ранее выделенный объект поверхности Microsoft DirectDraw в режиме ядра.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: Функция Нтгдидддестройсурфаце (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072443"
---
# <a name="ntgdidddestroysurface-function"></a><span data-ttu-id="ec15b-103">Функция Нтгдидддестройсурфаце</span><span class="sxs-lookup"><span data-stu-id="ec15b-103">NtGdiDdDestroySurface function</span></span>

<span data-ttu-id="ec15b-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ec15b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="ec15b-105">Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="ec15b-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="ec15b-106">Уничтожает ранее выделенный объект поверхности Microsoft DirectDraw в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="ec15b-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec15b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec15b-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a><span data-ttu-id="ec15b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec15b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec15b-109">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec15b-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec15b-110">Обработчик для ранее выделенного объекта поверхности режима ядра.</span><span class="sxs-lookup"><span data-stu-id="ec15b-110">Handle to previously allocated kernel-mode surface object.</span></span>

</dd> <dt>

<span data-ttu-id="ec15b-111">*бреалдестрой* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec15b-111">*bRealDestroy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec15b-112">Указывает, как уничтожить поверхность.</span><span class="sxs-lookup"><span data-stu-id="ec15b-112">Specifies how to destroy the surface.</span></span> <span data-ttu-id="ec15b-113">Может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ec15b-113">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="ec15b-114">УСЛОВИЯ</span><span class="sxs-lookup"><span data-stu-id="ec15b-114">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="ec15b-115">Удалите поверхность и свободную видеопамять.</span><span class="sxs-lookup"><span data-stu-id="ec15b-115">Destroy the surface and free video memory.</span></span>

</dd> <dt>



 <span data-ttu-id="ec15b-116">ISFALSE</span><span class="sxs-lookup"><span data-stu-id="ec15b-116">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="ec15b-117">Освободите видеопамять, но оставьте ее в неинициализированном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ec15b-117">Free the video memory but leave the surface in an uninitialized state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec15b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec15b-118">Return value</span></span>

<span data-ttu-id="ec15b-119">**Нтгдидддестройсурфаце** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ec15b-119">**NtGdiDdDestroySurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="ec15b-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ec15b-120">Return code</span></span>                                                                                              | <span data-ttu-id="ec15b-121">Описание</span><span class="sxs-lookup"><span data-stu-id="ec15b-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec15b-122"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="ec15b-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="ec15b-123">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="ec15b-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="ec15b-124">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="ec15b-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="ec15b-125">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="ec15b-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="ec15b-126"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="ec15b-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="ec15b-127">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="ec15b-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="ec15b-128">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ec15b-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="ec15b-129">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="ec15b-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec15b-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec15b-130">Remarks</span></span>

<span data-ttu-id="ec15b-131">Для создания и уничтожения поверхностей вместо этой функции в приложениях рекомендуется использовать интерфейсы API DirectDraw и Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ec15b-131">It is recommended that applications use the DirectDraw and Direct3D APIs to create and destroy surfaces instead of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec15b-132">Требования</span><span class="sxs-lookup"><span data-stu-id="ec15b-132">Requirements</span></span>



| <span data-ttu-id="ec15b-133">Требование</span><span class="sxs-lookup"><span data-stu-id="ec15b-133">Requirement</span></span> | <span data-ttu-id="ec15b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="ec15b-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec15b-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec15b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ec15b-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec15b-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ec15b-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec15b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ec15b-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec15b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ec15b-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ec15b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec15b-140"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec15b-140"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec15b-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec15b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec15b-142">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="ec15b-142">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




