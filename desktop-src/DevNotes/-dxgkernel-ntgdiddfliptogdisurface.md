---
description: Уведомляет драйвер о том, что Microsoft DirectDraw переводится на поверхность Windows интерфейс графических устройств (GDI) или с нее.
ms.assetid: e79be33a-24bc-477b-bc67-395fff74309c
title: Функция Нтгдиддфлиптогдисурфаце (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlipToGDISurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7e233bddf72c79507eab1fcefbf3de66460d228e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141490"
---
# <a name="ntgdiddfliptogdisurface-function"></a><span data-ttu-id="3965b-103">Функция Нтгдиддфлиптогдисурфаце</span><span class="sxs-lookup"><span data-stu-id="3965b-103">NtGdiDdFlipToGDISurface function</span></span>

<span data-ttu-id="3965b-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3965b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3965b-105">Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="3965b-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3965b-106">Уведомляет драйвер о том, что Microsoft DirectDraw переводится на поверхность Windows интерфейс графических устройств (GDI) или с нее.</span><span class="sxs-lookup"><span data-stu-id="3965b-106">Notifies the driver when Microsoft DirectDraw is flipping to or from a Windows Graphics Device Interface (GDI) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3965b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3965b-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlipToGDISurface(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_FLIPTOGDISURFACEDATA puFlipToGDISurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="3965b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3965b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3965b-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3965b-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3965b-110">Обработчик для ранее созданного объекта DirectDraw режима ядра.</span><span class="sxs-lookup"><span data-stu-id="3965b-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="3965b-111">*пуфлиптогдисурфацедата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="3965b-111">*puFlipToGDISurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3965b-112">Указатель на структуру [DD \_ флиптогдисурфацедата](https://msdn.microsoft.com/library/ms793922.aspx) , которая содержит сведения об уведомлении.</span><span class="sxs-lookup"><span data-stu-id="3965b-112">Pointer to a [DD\_FLIPTOGDISURFACEDATA](https://msdn.microsoft.com/library/ms793922.aspx) structure that contains the notification information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3965b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3965b-113">Return value</span></span>

<span data-ttu-id="3965b-114">**Нтгдиддфлиптогдисурфаце** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3965b-114">**NtGdiDdFlipToGDISurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="3965b-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3965b-115">Return code</span></span>                                                                                              | <span data-ttu-id="3965b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="3965b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3965b-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="3965b-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="3965b-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="3965b-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="3965b-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="3965b-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="3965b-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="3965b-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="3965b-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="3965b-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="3965b-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="3965b-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="3965b-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3965b-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="3965b-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="3965b-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3965b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3965b-125">Requirements</span></span>



| <span data-ttu-id="3965b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3965b-126">Requirement</span></span> | <span data-ttu-id="3965b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3965b-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3965b-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3965b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3965b-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3965b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3965b-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3965b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3965b-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3965b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3965b-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3965b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3965b-133"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="3965b-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3965b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3965b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3965b-135">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="3965b-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




