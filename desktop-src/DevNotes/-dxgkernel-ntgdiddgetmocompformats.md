---
description: Указывает несжатые форматы, в которые оборудование может декодировать данные.
ms.assetid: 44bcc4e2-0f8e-4292-b4a4-1ebbf899c14a
title: Функция Нтгдидджетмокомпформатс (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetMoCompFormats
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f0cd14cd2dae7905a06d3368c7d472d7af5b9a48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895849"
---
# <a name="ntgdiddgetmocompformats-function"></a><span data-ttu-id="dfb26-103">Функция Нтгдидджетмокомпформатс</span><span class="sxs-lookup"><span data-stu-id="dfb26-103">NtGdiDdGetMoCompFormats function</span></span>

<span data-ttu-id="dfb26-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dfb26-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="dfb26-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="dfb26-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="dfb26-106">Указывает несжатые форматы, в которые оборудование может декодировать данные.</span><span class="sxs-lookup"><span data-stu-id="dfb26-106">Indicates the uncompressed formats to which the hardware can decode the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb26-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfb26-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetMoCompFormats(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_GETMOCOMPFORMATSDATA puGetMoCompFormatsData
);
```



## <a name="parameters"></a><span data-ttu-id="dfb26-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfb26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfb26-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfb26-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb26-110">Обработчик для ранее созданного объекта DirectDraw режима ядра.</span><span class="sxs-lookup"><span data-stu-id="dfb26-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="dfb26-111">*пужетмокомпформатсдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dfb26-111">*puGetMoCompFormatsData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb26-112">Указатель на структуру [**DD \_ жетмокомпформатсдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompformatsdata) , которая содержит несжатые сведения о форматировании оборудования.</span><span class="sxs-lookup"><span data-stu-id="dfb26-112">Pointer to a [**DD\_GETMOCOMPFORMATSDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompformatsdata) structure that contains the uncompressed format information for the hardware.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfb26-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfb26-113">Return value</span></span>

<span data-ttu-id="dfb26-114">**Нтгдидджетмокомпформатс** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="dfb26-114">**NtGdiDdGetMoCompFormats** returns one of the following callback codes.</span></span>



| <span data-ttu-id="dfb26-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dfb26-115">Return code</span></span>                                                                                              | <span data-ttu-id="dfb26-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dfb26-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfb26-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="dfb26-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="dfb26-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="dfb26-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="dfb26-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="dfb26-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="dfb26-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="dfb26-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="dfb26-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="dfb26-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="dfb26-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="dfb26-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="dfb26-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="dfb26-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="dfb26-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="dfb26-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dfb26-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfb26-125">Remarks</span></span>

<span data-ttu-id="dfb26-126">Дополнительные сведения см. в пакете средств разработки драйверов для Microsoft DirectX Video Acceleration Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="dfb26-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb26-127">Требования</span><span class="sxs-lookup"><span data-stu-id="dfb26-127">Requirements</span></span>



| <span data-ttu-id="dfb26-128">Требование</span><span class="sxs-lookup"><span data-stu-id="dfb26-128">Requirement</span></span> | <span data-ttu-id="dfb26-129">Значение</span><span class="sxs-lookup"><span data-stu-id="dfb26-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb26-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfb26-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb26-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dfb26-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dfb26-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfb26-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb26-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dfb26-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dfb26-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dfb26-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfb26-135"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb26-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb26-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfb26-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb26-137">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="dfb26-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
