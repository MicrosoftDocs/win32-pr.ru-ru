---
description: Уведомляет драйвер о том, что этот объект компенсации движения больше не будет использоваться. Теперь драйверу необходимо выполнить необходимую очистку.
ms.assetid: 1d86a564-efe1-4971-99ec-2c9a6aa59c89
title: Функция Нтгдидддестроймокомп (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: b7bc5915fe43bd4d48495b2b1beda8ee38f05fe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895682"
---
# <a name="ntgdidddestroymocomp-function"></a><span data-ttu-id="c1fc9-104">Функция Нтгдидддестроймокомп</span><span class="sxs-lookup"><span data-stu-id="c1fc9-104">NtGdiDdDestroyMoComp function</span></span>

<span data-ttu-id="c1fc9-105">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="c1fc9-106">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="c1fc9-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="c1fc9-107">Уведомляет драйвер о том, что этот объект компенсации движения больше не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-107">Notifies the driver that this motion compensation object will no longer be used.</span></span> <span data-ttu-id="c1fc9-108">Теперь драйверу необходимо выполнить необходимую очистку.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-108">The driver now needs to perform any necessary cleanup.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1fc9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1fc9-109">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyMoComp(
  _In_    HANDLE                hMoComp,
  _Inout_ PDD_DESTROYMOCOMPDATA puBeginFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="c1fc9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1fc9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1fc9-111">*хмокомп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1fc9-111">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fc9-112">Обработайте [**\_ \_ локальную структуру DD мотионкомп**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) , которая содержит описание объекта компенсации движения, который необходимо уничтожить.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-112">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation object to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="c1fc9-113">*пубегинфрамедата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c1fc9-113">*puBeginFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fc9-114">Указатель на структуру [**DD \_ дестроймокомпдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) , которая содержит сведения, необходимые для завершения движения.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-114">Pointer to a [**DD\_DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) structure that contains the information needed to finish motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1fc9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1fc9-115">Return value</span></span>

<span data-ttu-id="c1fc9-116">**Нтгдидддестроймокомп** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-116">**NtGdiDdDestroyMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="c1fc9-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c1fc9-117">Return code</span></span>                                                                                              | <span data-ttu-id="c1fc9-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c1fc9-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1fc9-119"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="c1fc9-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="c1fc9-120">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="c1fc9-121">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="c1fc9-122">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="c1fc9-123"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="c1fc9-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="c1fc9-124">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="c1fc9-125">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="c1fc9-126">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="c1fc9-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c1fc9-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1fc9-127">Remarks</span></span>

<span data-ttu-id="c1fc9-128">Дополнительные сведения см. в пакете средств разработки драйверов для Microsoft DirectX Video Acceleration Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="c1fc9-128">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1fc9-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c1fc9-129">Requirements</span></span>



| <span data-ttu-id="c1fc9-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c1fc9-130">Requirement</span></span> | <span data-ttu-id="c1fc9-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c1fc9-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fc9-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1fc9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c1fc9-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1fc9-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c1fc9-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1fc9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c1fc9-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1fc9-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c1fc9-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c1fc9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1fc9-137"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1fc9-137"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1fc9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1fc9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1fc9-139">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="c1fc9-139">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
