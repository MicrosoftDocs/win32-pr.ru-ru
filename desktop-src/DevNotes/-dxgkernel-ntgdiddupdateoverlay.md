---
description: Перемещает или изменяет визуальные атрибуты поверхности наложения.
ms.assetid: 6d39166c-0efc-450d-adf4-9f4dfdf7c57f
title: Функция Нтгдиддупдатеоверлай (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUpdateOverlay
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bbe610c27d83061bda0996ce9acc082efa95e3a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990372"
---
# <a name="ntgdiddupdateoverlay-function"></a><span data-ttu-id="b5224-103">Функция Нтгдиддупдатеоверлай</span><span class="sxs-lookup"><span data-stu-id="b5224-103">NtGdiDdUpdateOverlay function</span></span>

<span data-ttu-id="b5224-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b5224-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b5224-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="b5224-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b5224-106">Перемещает или изменяет визуальные атрибуты поверхности наложения.</span><span class="sxs-lookup"><span data-stu-id="b5224-106">Repositions or modifies the visual attributes of an overlay surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5224-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5224-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUpdateOverlay(
  _In_    HANDLE                hSurfaceDestination,
  _In_    HANDLE                hSurfaceSource,
  _Inout_ PDD_UPDATEOVERLAYDATA puUpdateOverlayData
);
```



## <a name="parameters"></a><span data-ttu-id="b5224-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5224-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5224-109">*хсурфацедестинатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5224-109">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5224-110">Обработчик для ранее созданного объекта DirectDraw режима ядра.</span><span class="sxs-lookup"><span data-stu-id="b5224-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="b5224-111">*хсурфацесаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5224-111">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5224-112">Обрабатывает [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , описывающую поверхность наложения.</span><span class="sxs-lookup"><span data-stu-id="b5224-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="b5224-113">*пуупдатеоверлайдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b5224-113">*puUpdateOverlayData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5224-114">Указатель на структуру [**DD \_ упдатеоверлайдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) , которая содержит сведения, необходимые для обновления оверлея.</span><span class="sxs-lookup"><span data-stu-id="b5224-114">Pointer to a [**DD\_UPDATEOVERLAYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) structure that contains the information required to update the overlay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5224-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5224-115">Return value</span></span>

<span data-ttu-id="b5224-116">**Нтгдиддупдатеоверлай** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b5224-116">**NtGdiDdUpdateOverlay** returns one of the following callback codes.</span></span>



| <span data-ttu-id="b5224-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b5224-117">Return code</span></span>                                                                                              | <span data-ttu-id="b5224-118">Описание</span><span class="sxs-lookup"><span data-stu-id="b5224-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5224-119"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="b5224-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="b5224-120">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="b5224-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="b5224-121">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="b5224-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="b5224-122">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="b5224-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b5224-123"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="b5224-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="b5224-124">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="b5224-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="b5224-125">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b5224-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="b5224-126">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="b5224-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b5224-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b5224-127">Requirements</span></span>



| <span data-ttu-id="b5224-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b5224-128">Requirement</span></span> | <span data-ttu-id="b5224-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b5224-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5224-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5224-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b5224-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b5224-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b5224-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5224-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b5224-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b5224-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5224-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b5224-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5224-135"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5224-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5224-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5224-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5224-137">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="b5224-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
