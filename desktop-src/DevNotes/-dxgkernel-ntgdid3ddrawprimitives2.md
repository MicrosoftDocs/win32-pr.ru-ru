---
description: Отображает примитивы и возвращает обновленное состояние рендеринга.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: Функция NtGdiD3DDrawPrimitives2 (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072387"
---
# <a name="ntgdid3ddrawprimitives2-function"></a><span data-ttu-id="dff44-103">Функция NtGdiD3DDrawPrimitives2</span><span class="sxs-lookup"><span data-stu-id="dff44-103">NtGdiD3DDrawPrimitives2 function</span></span>

<span data-ttu-id="dff44-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dff44-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="dff44-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="dff44-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="dff44-106">Отображает примитивы и возвращает обновленное состояние рендеринга.</span><span class="sxs-lookup"><span data-stu-id="dff44-106">Renders primitives and returns the updated render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="dff44-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dff44-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a><span data-ttu-id="dff44-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dff44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff44-109">*хкмдбуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dff44-109">*hCmdBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff44-110">Обозначает [**\_ \_ локальную структуру поверхности DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , которая определяет поверхность DirectDraw, содержащую данные команды.</span><span class="sxs-lookup"><span data-stu-id="dff44-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the command data.</span></span>

</dd> <dt>

<span data-ttu-id="dff44-111">*хвбуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dff44-111">*hVBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff44-112">Маркер [**\_ \_ локальной структуры области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , которая определяет поверхность DirectDraw, содержащую данные вершин.</span><span class="sxs-lookup"><span data-stu-id="dff44-112">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the vertex data.</span></span>

</dd> <dt>

<span data-ttu-id="dff44-113">*пдед* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dff44-113">*pded* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dff44-114">Указатель на структуру [**\_ DRAWPRIMITIVES2DATA D3DNTHAL**](/windows-hardware/drivers/ddi/) , которая содержит сведения, необходимые драйверу для отрисовки одного или нескольких примитивов.</span><span class="sxs-lookup"><span data-stu-id="dff44-114">Pointer to a [**D3DNTHAL\_DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to render one or more primitives.</span></span>

</dd> <dt>

<span data-ttu-id="dff44-115">*пфпвидмемкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dff44-115">*pfpVidMemCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dff44-116">Новый указатель на видеопамять, если драйвер заменял буфер команд.</span><span class="sxs-lookup"><span data-stu-id="dff44-116">New pointer to video memory if the driver swapped the command buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dff44-117">*пдвсизекмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dff44-117">*pdwSizeCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dff44-118">Указывает минимальное число байтов, которое драйвер должен увеличить буфер команд переключения.</span><span class="sxs-lookup"><span data-stu-id="dff44-118">Specifies the minimum number of bytes that the driver must increase the swap command buffer by.</span></span>

</dd> <dt>

<span data-ttu-id="dff44-119">*пфпвидмемвткс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dff44-119">*pfpVidMemVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dff44-120">Новый указатель на видеопамять, если драйвер заменял буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="dff44-120">New pointer to video memory if the driver swapped the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dff44-121">*пдвсизевткс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dff44-121">*pdwSizeVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dff44-122">Указывает минимальное число байтов, которое драйвер должен выделить для буфера вершин подкачки.</span><span class="sxs-lookup"><span data-stu-id="dff44-122">Specifies the minimum number of bytes that the driver must allocate for the swap vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dff44-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dff44-123">Return value</span></span>

<span data-ttu-id="dff44-124">**NtGdiD3DDrawPrimitives2** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="dff44-124">**NtGdiD3DDrawPrimitives2** returns one of the following callback codes.</span></span>



| <span data-ttu-id="dff44-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dff44-125">Return code</span></span>                                                                                              | <span data-ttu-id="dff44-126">Описание</span><span class="sxs-lookup"><span data-stu-id="dff44-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dff44-127"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="dff44-127"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="dff44-128">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="dff44-128">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="dff44-129">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="dff44-129">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="dff44-130">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="dff44-130">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="dff44-131"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="dff44-131"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="dff44-132">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="dff44-132">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="dff44-133">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="dff44-133">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="dff44-134">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="dff44-134">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dff44-135">Требования</span><span class="sxs-lookup"><span data-stu-id="dff44-135">Requirements</span></span>



| <span data-ttu-id="dff44-136">Требование</span><span class="sxs-lookup"><span data-stu-id="dff44-136">Requirement</span></span> | <span data-ttu-id="dff44-137">Значение</span><span class="sxs-lookup"><span data-stu-id="dff44-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dff44-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dff44-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dff44-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dff44-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dff44-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dff44-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dff44-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dff44-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dff44-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dff44-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="dff44-143"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="dff44-143"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dff44-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dff44-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff44-145">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="dff44-145">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
