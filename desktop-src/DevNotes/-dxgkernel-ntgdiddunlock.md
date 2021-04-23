---
description: Освобождает блокировку, удерживаемую на указанной поверхности.
ms.assetid: d9d3178b-aadd-4c33-8044-8e6362f9fefe
title: Функция Нтгдиддунлокк (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnlock
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 3472dc32cc503b83c12bcc17cdbd0d14b89b0de4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495906"
---
# <a name="ntgdiddunlock-function"></a><span data-ttu-id="7dd96-103">Функция Нтгдиддунлокк</span><span class="sxs-lookup"><span data-stu-id="7dd96-103">NtGdiDdUnlock function</span></span>

<span data-ttu-id="7dd96-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7dd96-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="7dd96-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="7dd96-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="7dd96-106">Освобождает блокировку, удерживаемую на указанной поверхности.</span><span class="sxs-lookup"><span data-stu-id="7dd96-106">Releases the lock held on the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd96-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dd96-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUnlock(
  _In_    HANDLE         hSurface,
  _Inout_ PDD_UNLOCKDATA puUnlockData
);
```



## <a name="parameters"></a><span data-ttu-id="7dd96-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7dd96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dd96-109">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7dd96-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd96-110">Обработайте [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , описывающую область, которая должна быть разблокирована.</span><span class="sxs-lookup"><span data-stu-id="7dd96-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface to be unlocked.</span></span>

</dd> <dt>

<span data-ttu-id="7dd96-111">*пуунлоккдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7dd96-111">*puUnlockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd96-112">Указатель на структуру [**DD \_ унлоккдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) , которая содержит сведения, необходимые для выполнения блокировки.</span><span class="sxs-lookup"><span data-stu-id="7dd96-112">Pointer to a [**DD\_UNLOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) structure that contains the information required to perform the lock release.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dd96-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7dd96-113">Return value</span></span>

<span data-ttu-id="7dd96-114">**Нтгдиддунлокк** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7dd96-114">**NtGdiDdUnlock** returns one of the following callback codes.</span></span>



| <span data-ttu-id="7dd96-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7dd96-115">Return code</span></span>                                                                                              | <span data-ttu-id="7dd96-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7dd96-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7dd96-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd96-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="7dd96-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="7dd96-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="7dd96-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="7dd96-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="7dd96-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="7dd96-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="7dd96-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd96-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="7dd96-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="7dd96-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="7dd96-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7dd96-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="7dd96-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="7dd96-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7dd96-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7dd96-125">Requirements</span></span>



| <span data-ttu-id="7dd96-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7dd96-126">Requirement</span></span> | <span data-ttu-id="7dd96-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7dd96-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd96-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dd96-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7dd96-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7dd96-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7dd96-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dd96-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7dd96-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7dd96-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7dd96-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7dd96-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dd96-133"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dd96-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dd96-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7dd96-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd96-135">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="7dd96-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
