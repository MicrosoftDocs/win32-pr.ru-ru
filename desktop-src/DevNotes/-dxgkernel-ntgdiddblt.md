---
description: Выполняет перенос битового блока.
ms.assetid: 90cc02af-96af-4913-ae7d-62f39cd6ddd7
title: Функция Нтгдиддблт (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBlt
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 86249a8ff1069bc0875aad3fcca576ef78b9db68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141494"
---
# <a name="ntgdiddblt-function"></a><span data-ttu-id="47639-103">Функция Нтгдиддблт</span><span class="sxs-lookup"><span data-stu-id="47639-103">NtGdiDdBlt function</span></span>

<span data-ttu-id="47639-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="47639-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="47639-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="47639-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="47639-106">Выполняет перенос битового блока.</span><span class="sxs-lookup"><span data-stu-id="47639-106">Performs a bit-block transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="47639-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47639-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdBlt(
  _In_    HANDLE      hSurfaceDest,
  _In_    HANDLE      hSurfaceSrc,
  _Inout_ PDD_BLTDATA puBltData
);
```



## <a name="parameters"></a><span data-ttu-id="47639-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="47639-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47639-109">*хсурфацедест* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47639-109">*hSurfaceDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47639-110">Обработайте [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , описывающую поверхность, на которую Блит.</span><span class="sxs-lookup"><span data-stu-id="47639-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface on which to blit.</span></span>

</dd> <dt>

<span data-ttu-id="47639-111">*хсурфацесрк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47639-111">*hSurfaceSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47639-112">Обрабатывает [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , которая описывает исходную поверхность.</span><span class="sxs-lookup"><span data-stu-id="47639-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the source surface.</span></span>

</dd> <dt>

<span data-ttu-id="47639-113">*публтдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="47639-113">*puBltData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="47639-114">Указатель на структуру [**DD \_ блтдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) , которая содержит сведения, необходимые драйверу для выполнения Блит.</span><span class="sxs-lookup"><span data-stu-id="47639-114">Pointer to a [**DD\_BLTDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) structure that contains the information required for the driver to perform the blit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47639-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47639-115">Return value</span></span>

<span data-ttu-id="47639-116">**Нтгдиддблт** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="47639-116">**NtGdiDdBlt** returns one of the following callback codes.</span></span>



| <span data-ttu-id="47639-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="47639-117">Return code</span></span>                                                                                              | <span data-ttu-id="47639-118">Описание</span><span class="sxs-lookup"><span data-stu-id="47639-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47639-119"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="47639-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="47639-120">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="47639-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="47639-121">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="47639-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="47639-122">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="47639-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="47639-123"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="47639-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="47639-124">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="47639-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="47639-125">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="47639-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="47639-126">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="47639-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="47639-127">Требования</span><span class="sxs-lookup"><span data-stu-id="47639-127">Requirements</span></span>



| <span data-ttu-id="47639-128">Требование</span><span class="sxs-lookup"><span data-stu-id="47639-128">Requirement</span></span> | <span data-ttu-id="47639-129">Значение</span><span class="sxs-lookup"><span data-stu-id="47639-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47639-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47639-130">Minimum supported client</span></span><br/> | <span data-ttu-id="47639-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47639-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="47639-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47639-132">Minimum supported server</span></span><br/> | <span data-ttu-id="47639-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47639-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="47639-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="47639-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="47639-135"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="47639-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47639-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47639-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47639-137">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="47639-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
