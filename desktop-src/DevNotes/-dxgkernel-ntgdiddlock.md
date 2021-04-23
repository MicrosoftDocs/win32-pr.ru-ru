---
description: Блокирует указанную область памяти поверхности и предоставляет допустимый указатель на блок памяти, связанный с поверхностью.
ms.assetid: 02810576-73d8-431d-ab41-3244dcff311f
title: Функция Нтгдиддлокк (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLock
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 3ddf40ae992b6b463886396ba026ec08293bb027
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495933"
---
# <a name="ntgdiddlock-function"></a><span data-ttu-id="cc27f-103">Функция Нтгдиддлокк</span><span class="sxs-lookup"><span data-stu-id="cc27f-103">NtGdiDdLock function</span></span>

<span data-ttu-id="cc27f-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cc27f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="cc27f-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="cc27f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="cc27f-106">Блокирует указанную область памяти поверхности и предоставляет допустимый указатель на блок памяти, связанный с поверхностью.</span><span class="sxs-lookup"><span data-stu-id="cc27f-106">Locks a specified area of surface memory and provides a valid pointer to a block of memory associated with a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc27f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc27f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdLock(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData,
  _In_    HDC          hdcClip
);
```



## <a name="parameters"></a><span data-ttu-id="cc27f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc27f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc27f-109">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc27f-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc27f-110">Обрабатывает [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , которая описывает поверхность, связанную с областью памяти, которая должна быть заблокирована.</span><span class="sxs-lookup"><span data-stu-id="cc27f-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface associated with the memory region to be locked down.</span></span>

</dd> <dt>

<span data-ttu-id="cc27f-111">*пулоккдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cc27f-111">*puLockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc27f-112">Указатель на структуру [**DD \_ локкдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) , которая содержит сведения, необходимые для выполнения блокировки.</span><span class="sxs-lookup"><span data-stu-id="cc27f-112">Pointer to a [**DD\_LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) structure that contains the information required to perform the lockdown.</span></span>

</dd> <dt>

<span data-ttu-id="cc27f-113">*хдкклип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc27f-113">*hdcClip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc27f-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="cc27f-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc27f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc27f-115">Return value</span></span>

<span data-ttu-id="cc27f-116">**Нтгдиддлокк** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="cc27f-116">**NtGdiDdLock** returns one of the following callback codes.</span></span>



| <span data-ttu-id="cc27f-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cc27f-117">Return code</span></span>                                                                                              | <span data-ttu-id="cc27f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="cc27f-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc27f-119"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="cc27f-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="cc27f-120">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="cc27f-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="cc27f-121">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="cc27f-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="cc27f-122">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="cc27f-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="cc27f-123"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="cc27f-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="cc27f-124">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="cc27f-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="cc27f-125">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cc27f-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="cc27f-126">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="cc27f-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cc27f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="cc27f-127">Requirements</span></span>



| <span data-ttu-id="cc27f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="cc27f-128">Requirement</span></span> | <span data-ttu-id="cc27f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="cc27f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cc27f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc27f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cc27f-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cc27f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cc27f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc27f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cc27f-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cc27f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cc27f-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cc27f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc27f-135"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc27f-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc27f-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc27f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc27f-137">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="cc27f-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
