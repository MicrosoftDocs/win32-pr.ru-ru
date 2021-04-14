---
description: Определяет, может ли драйвер создать команду уровня драйвера или буфер вершин указанного описания.
ms.assetid: c67492d9-c4ba-4206-8beb-3d67235192f9
title: Функция NtGdiDdCanCreateD3DBuffer (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 849eb2ba9c1349c54c20703217989b0b92ee78e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647141"
---
# <a name="ntgdiddcancreated3dbuffer-function"></a><span data-ttu-id="657e6-103">Функция NtGdiDdCanCreateD3DBuffer</span><span class="sxs-lookup"><span data-stu-id="657e6-103">NtGdiDdCanCreateD3DBuffer function</span></span>

<span data-ttu-id="657e6-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="657e6-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="657e6-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="657e6-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="657e6-106">Определяет, может ли драйвер создать команду уровня драйвера или буфер вершин указанного описания.</span><span class="sxs-lookup"><span data-stu-id="657e6-106">Determines whether the driver can create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="657e6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="657e6-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCanCreateD3DBuffer(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="657e6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="657e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="657e6-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="657e6-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="657e6-110">Обработчик для [**\_ \_ глобальной структуры DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) , представляющей объект DIRECTDRAW.</span><span class="sxs-lookup"><span data-stu-id="657e6-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="657e6-111">*пуканкреатесурфацедата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="657e6-111">*puCanCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="657e6-112">Указатель на структуру [**DD \_ канкреатесурфацедата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) .</span><span class="sxs-lookup"><span data-stu-id="657e6-112">Pointer to a [**DD\_CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) structure.</span></span> <span data-ttu-id="657e6-113">Эта структура содержит сведения, необходимые драйверу для определения возможности создания буфера команд или вершин.</span><span class="sxs-lookup"><span data-stu-id="657e6-113">This structure contains the information required for the driver to determine whether a command or vertex buffer can be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="657e6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="657e6-114">Return value</span></span>

<span data-ttu-id="657e6-115">**NtGdiDdCanCreateD3DBuffer** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="657e6-115">**NtGdiDdCanCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="657e6-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="657e6-116">Return code</span></span>                                                                                              | <span data-ttu-id="657e6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="657e6-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="657e6-118"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="657e6-118"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="657e6-119">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="657e6-119">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="657e6-120">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="657e6-120">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="657e6-121">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="657e6-121">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="657e6-122"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="657e6-122"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="657e6-123">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="657e6-123">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="657e6-124">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="657e6-124">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="657e6-125">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="657e6-125">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="657e6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="657e6-126">Requirements</span></span>



| <span data-ttu-id="657e6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="657e6-127">Requirement</span></span> | <span data-ttu-id="657e6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="657e6-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="657e6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="657e6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="657e6-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="657e6-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="657e6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="657e6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="657e6-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="657e6-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="657e6-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="657e6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="657e6-134"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="657e6-134"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="657e6-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="657e6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657e6-136">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="657e6-136">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
