---
description: Запрашивает состояние последней операции отрисовки на указанную поверхность.
ms.assetid: bc7f8f84-119e-4c09-87f5-6b122e9f9821
title: Функция Нтгдиддкуеримокомпстатус (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryMoCompStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7795602e29d565022d532a0ebd51be1c4249a02e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539134"
---
# <a name="ntgdiddquerymocompstatus-function"></a><span data-ttu-id="9c628-103">Функция Нтгдиддкуеримокомпстатус</span><span class="sxs-lookup"><span data-stu-id="9c628-103">NtGdiDdQueryMoCompStatus function</span></span>

<span data-ttu-id="9c628-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9c628-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="9c628-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="9c628-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="9c628-106">Запрашивает состояние последней операции отрисовки на указанную поверхность.</span><span class="sxs-lookup"><span data-stu-id="9c628-106">Queries the status of the most recent rendering operation to the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c628-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c628-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdQueryMoCompStatus(
  _In_    HANDLE                    hMoComp,
  _Inout_ PDD_QUERYMOCOMPSTATUSDATA puQueryMoCompStatusData
);
```



## <a name="parameters"></a><span data-ttu-id="9c628-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c628-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c628-109">*хмокомп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c628-109">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c628-110">Указатель на [**\_ \_ локальную структуру DD мотионкомп**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) , содержащую описание запрошенной компенсации движения.</span><span class="sxs-lookup"><span data-stu-id="9c628-110">Pointer to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation being requested.</span></span>

</dd> <dt>

<span data-ttu-id="9c628-111">*пукуеримокомпстатусдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9c628-111">*puQueryMoCompStatusData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c628-112">Указатель на структуру [**DD \_ куеримокомпстатусдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_querymocompstatusdata) , которая содержит сведения, необходимые для запроса состояния.</span><span class="sxs-lookup"><span data-stu-id="9c628-112">Pointer to a [**DD\_QUERYMOCOMPSTATUSDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_querymocompstatusdata) structure that contains the information needed to query the status.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c628-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c628-113">Return value</span></span>

<span data-ttu-id="9c628-114">**Нтгдиддкуеримокомпстатус** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="9c628-114">**NtGdiDdQueryMoCompStatus** returns one of the following callback codes.</span></span>



| <span data-ttu-id="9c628-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9c628-115">Return code</span></span>                                                                                              | <span data-ttu-id="9c628-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9c628-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c628-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="9c628-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="9c628-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="9c628-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="9c628-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="9c628-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="9c628-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="9c628-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="9c628-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="9c628-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="9c628-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="9c628-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="9c628-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9c628-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="9c628-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="9c628-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c628-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c628-125">Remarks</span></span>

<span data-ttu-id="9c628-126">Дополнительные сведения см. в пакете средств разработки драйверов для Microsoft DirectX Video Acceleration Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="9c628-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c628-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9c628-127">Requirements</span></span>



| <span data-ttu-id="9c628-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9c628-128">Requirement</span></span> | <span data-ttu-id="9c628-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9c628-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c628-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c628-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9c628-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c628-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9c628-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c628-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9c628-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c628-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c628-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9c628-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c628-135"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c628-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c628-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c628-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c628-137">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="9c628-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
