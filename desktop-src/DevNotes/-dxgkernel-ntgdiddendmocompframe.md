---
description: Завершает декодированный кадр.
ms.assetid: 476f8bcc-2a93-430e-bda5-33102e36a35a
title: Функция Нтгдиддендмокомпфраме (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdEndMoCompFrame
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 50f56faa724f88e16ef10b46342d8dd53afaf497
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807397"
---
# <a name="ntgdiddendmocompframe-function"></a><span data-ttu-id="413cd-103">Функция Нтгдиддендмокомпфраме</span><span class="sxs-lookup"><span data-stu-id="413cd-103">NtGdiDdEndMoCompFrame function</span></span>

<span data-ttu-id="413cd-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="413cd-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="413cd-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="413cd-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="413cd-106">Завершает декодированный кадр.</span><span class="sxs-lookup"><span data-stu-id="413cd-106">Completes a decoded frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="413cd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="413cd-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdEndMoCompFrame(
  _In_    HANDLE                 hMoComp,
  _Inout_ PDD_ENDMOCOMPFRAMEDATA puEndFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="413cd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="413cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="413cd-109">*хмокомп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="413cd-109">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413cd-110">Обработайте [ \_ \_ локальную структуру DD мотионкомп](https://msdn.microsoft.com/library/ms794211.aspx) , которая содержит описание запрошенной компенсации движения.</span><span class="sxs-lookup"><span data-stu-id="413cd-110">Handle to a [DD\_MOTIONCOMP\_LOCAL](https://msdn.microsoft.com/library/ms794211.aspx) structure that contains a description of the motion compensation being requested.</span></span>

</dd> <dt>

<span data-ttu-id="413cd-111">*пуендфрамедата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="413cd-111">*puEndFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="413cd-112">Указатель на структуру [DD \_ ендмокомпфрамедата](https://msdn.microsoft.com/library/ms793897.aspx) , которая содержит сведения, необходимые для завершения декодированного кадра.</span><span class="sxs-lookup"><span data-stu-id="413cd-112">Pointer to a [DD\_ENDMOCOMPFRAMEDATA](https://msdn.microsoft.com/library/ms793897.aspx) structure that contains the information needed to complete the decoded frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="413cd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="413cd-113">Return value</span></span>

<span data-ttu-id="413cd-114">**Нтгдиддендмокомпфраме** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="413cd-114">**NtGdiDdEndMoCompFrame** returns one of the following callback codes.</span></span>



| <span data-ttu-id="413cd-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="413cd-115">Return code</span></span>                                                                                              | <span data-ttu-id="413cd-116">Описание</span><span class="sxs-lookup"><span data-stu-id="413cd-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="413cd-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="413cd-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="413cd-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="413cd-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="413cd-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="413cd-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="413cd-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="413cd-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="413cd-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="413cd-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="413cd-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="413cd-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="413cd-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="413cd-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="413cd-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="413cd-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="413cd-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="413cd-125">Remarks</span></span>

<span data-ttu-id="413cd-126">Дополнительные сведения см. в пакете средств разработки драйверов для Microsoft DirectX Video Acceleration Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="413cd-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="413cd-127">Требования</span><span class="sxs-lookup"><span data-stu-id="413cd-127">Requirements</span></span>



| <span data-ttu-id="413cd-128">Требование</span><span class="sxs-lookup"><span data-stu-id="413cd-128">Requirement</span></span> | <span data-ttu-id="413cd-129">Значение</span><span class="sxs-lookup"><span data-stu-id="413cd-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="413cd-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="413cd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="413cd-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="413cd-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="413cd-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="413cd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="413cd-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="413cd-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="413cd-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="413cd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="413cd-135"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="413cd-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="413cd-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="413cd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="413cd-137">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="413cd-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




