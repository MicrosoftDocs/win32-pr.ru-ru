---
description: Используется обеими средами выполнения Microsoft DirectDraw и Microsoft Direct3D для получения сведений из драйвера о текущем состоянии.
ms.assetid: a7697e0c-9485-4a9c-b211-67ce07dc3604
title: Функция NtGdiD3DGetDriverState (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DGetDriverState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: c88f2fde4d848aac5ecae3c60aef77d4c6b783cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655665"
---
# <a name="ntgdid3dgetdriverstate-function"></a><span data-ttu-id="0766a-103">Функция NtGdiD3DGetDriverState</span><span class="sxs-lookup"><span data-stu-id="0766a-103">NtGdiD3DGetDriverState function</span></span>

<span data-ttu-id="0766a-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0766a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="0766a-105">Вместо этого используйте DirectDraw и Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="0766a-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="0766a-106">Используется обеими средами выполнения Microsoft DirectDraw и Microsoft Direct3D для получения сведений из драйвера о текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="0766a-106">Used by both the Microsoft DirectDraw and Microsoft Direct3D runtimes to obtain information from the driver about its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="0766a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0766a-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DGetDriverState(
  _Inout_ PDD_GETDRIVERSTATEDATA pdata
);
```



## <a name="parameters"></a><span data-ttu-id="0766a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0766a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0766a-109">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0766a-109">*pdata* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0766a-110">Указатель на структуру [**DD \_ жетдриверстатедата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) , описывающую состояние драйвера.</span><span class="sxs-lookup"><span data-stu-id="0766a-110">Pointer to a [**DD\_GETDRIVERSTATEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) structure that describes the state of the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0766a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0766a-111">Return value</span></span>

<span data-ttu-id="0766a-112">**NtGdiD3DGetDriverState** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0766a-112">**NtGdiD3DGetDriverState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="0766a-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0766a-113">Return code</span></span>                                                                                              | <span data-ttu-id="0766a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0766a-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0766a-115"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="0766a-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="0766a-116">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="0766a-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="0766a-117">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="0766a-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="0766a-118">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="0766a-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="0766a-119"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="0766a-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="0766a-120">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="0766a-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="0766a-121">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0766a-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="0766a-122">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="0766a-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0766a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0766a-123">Requirements</span></span>



| <span data-ttu-id="0766a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0766a-124">Requirement</span></span> | <span data-ttu-id="0766a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0766a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0766a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0766a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0766a-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0766a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0766a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0766a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0766a-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0766a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0766a-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0766a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0766a-131"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="0766a-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0766a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0766a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0766a-133">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="0766a-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
