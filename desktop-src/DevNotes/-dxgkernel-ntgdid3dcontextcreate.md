---
description: Создает контекст.
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: Функция NtGdiD3DContextCreate (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: f59a80d3efd5e077bc1eadea66255ff5e6ea7523
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140962"
---
# <a name="ntgdid3dcontextcreate-function"></a><span data-ttu-id="9eef9-103">Функция NtGdiD3DContextCreate</span><span class="sxs-lookup"><span data-stu-id="9eef9-103">NtGdiD3DContextCreate function</span></span>

<span data-ttu-id="9eef9-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9eef9-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="9eef9-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="9eef9-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="9eef9-106">Создает контекст.</span><span class="sxs-lookup"><span data-stu-id="9eef9-106">Creates a context.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eef9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9eef9-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a><span data-ttu-id="9eef9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9eef9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eef9-109">*хдиректдравлокал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9eef9-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eef9-110">Обработчик для объекта DirectDraw режима ядра, ранее созданного с помощью [**нтгдиддкреатедиректдравобжект**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), представляющего устройство, на котором будет создан контекст Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9eef9-110">Handle to a kernel-mode DirectDraw object, previously created with [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), representing the device on which the Direct3D context is to be created.</span></span>

</dd> <dt>

<span data-ttu-id="9eef9-111">*хсурфколор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9eef9-111">*hSurfColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eef9-112">Обработка [**\_ \_ локальной структуры области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , описывающей поверхность DirectDraw, которая будет использоваться в качестве целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="9eef9-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as the rendering target.</span></span>

</dd> <dt>

<span data-ttu-id="9eef9-113">*хсурфз* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9eef9-113">*hSurfZ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eef9-114">Обрабатывает [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , описывающую поверхность DirectDraw, которая будет использоваться в качестве буфера глубины.</span><span class="sxs-lookup"><span data-stu-id="9eef9-114">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as a depth buffer.</span></span> <span data-ttu-id="9eef9-115">Если этот член имеет **значение NULL**, буферизация глубины не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9eef9-115">If this member is **NULL**, no depth buffering is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="9eef9-116">*пдкЦи* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9eef9-116">*pdcci* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eef9-117">Указатель на структуру [**\_ контексткреатедата D3DNTHAL**](/windows-hardware/drivers/ddi/) , которая содержит сведения, необходимые для создания контекста и данных, которые драйвер должен хранить в новом контексте.</span><span class="sxs-lookup"><span data-stu-id="9eef9-117">Pointer to a [**D3DNTHAL\_CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required to create a context and the data that the driver should store in the new context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eef9-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9eef9-118">Return value</span></span>

<span data-ttu-id="9eef9-119">**NtGdiD3DContextCreate** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="9eef9-119">**NtGdiD3DContextCreate** returns one of the following callback codes.</span></span>



| <span data-ttu-id="9eef9-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9eef9-120">Return code</span></span>                                                                                              | <span data-ttu-id="9eef9-121">Описание</span><span class="sxs-lookup"><span data-stu-id="9eef9-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9eef9-122"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="9eef9-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="9eef9-123">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="9eef9-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="9eef9-124">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="9eef9-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="9eef9-125">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="9eef9-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="9eef9-126"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="9eef9-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="9eef9-127">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="9eef9-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="9eef9-128">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9eef9-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="9eef9-129">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="9eef9-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9eef9-130">Требования</span><span class="sxs-lookup"><span data-stu-id="9eef9-130">Requirements</span></span>



| <span data-ttu-id="9eef9-131">Требование</span><span class="sxs-lookup"><span data-stu-id="9eef9-131">Requirement</span></span> | <span data-ttu-id="9eef9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="9eef9-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9eef9-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9eef9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9eef9-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9eef9-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9eef9-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9eef9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9eef9-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9eef9-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9eef9-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9eef9-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eef9-138"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eef9-138"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eef9-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9eef9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eef9-140">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="9eef9-140">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
