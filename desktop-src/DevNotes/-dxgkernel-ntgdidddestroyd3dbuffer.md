---
description: Уничтожает ранее выделенный объект поверхности Microsoft DirectDraw в режиме ядра, созданный с помощью элемента Двкапс структуры ДДСКАПС, равным ДДСКАПС \_ ексекутебуффер.
ms.assetid: c737b706-25be-49b8-8d8c-35f48aea2889
title: Функция NtGdiDdDestroyD3DBuffer (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: e88394e8cc3d13e1d117a1e53eab1190b1290ca4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806940"
---
# <a name="ntgdidddestroyd3dbuffer-function"></a><span data-ttu-id="b2676-103">Функция NtGdiDdDestroyD3DBuffer</span><span class="sxs-lookup"><span data-stu-id="b2676-103">NtGdiDdDestroyD3DBuffer function</span></span>

<span data-ttu-id="b2676-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b2676-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b2676-105">Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="b2676-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b2676-106">Уничтожает ранее выделенный объект поверхности Microsoft DirectDraw в режиме ядра, созданный с помощью элемента **двкапс** структуры [**ддскапс**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) , равным ддскапс \_ ексекутебуффер.</span><span class="sxs-lookup"><span data-stu-id="b2676-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object that was created with the **dwCaps** member of the [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) structure set to DDSCAPS\_EXECUTEBUFFER.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2676-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2676-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyD3DBuffer(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="b2676-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2676-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2676-109">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2676-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2676-110">Обрабатывайте структуру [**DD \_ дестройсурфацедата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) , которая содержит сведения, необходимые для уничтожения команды Direct3D или буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="b2676-110">Handle to a [**DD\_DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) structure that contains the information needed to destroy a Direct3D command or vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2676-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2676-111">Return value</span></span>

<span data-ttu-id="b2676-112">**NtGdiDdDestroyD3DBuffer** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b2676-112">**NtGdiDdDestroyD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="b2676-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b2676-113">Return code</span></span>                                                                                              | <span data-ttu-id="b2676-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b2676-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2676-115"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="b2676-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="b2676-116">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="b2676-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="b2676-117">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="b2676-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="b2676-118">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="b2676-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b2676-119"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="b2676-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="b2676-120">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="b2676-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="b2676-121">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b2676-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="b2676-122">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="b2676-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b2676-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b2676-123">Requirements</span></span>



| <span data-ttu-id="b2676-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b2676-124">Requirement</span></span> | <span data-ttu-id="b2676-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b2676-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2676-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2676-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b2676-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2676-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b2676-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2676-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b2676-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2676-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b2676-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b2676-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2676-131"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2676-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2676-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2676-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2676-133">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="b2676-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
