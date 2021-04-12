---
description: Начинает декодировать новый кадр.
ms.assetid: da2c231d-89a9-4fd9-99b5-f7c1309c26e0
title: Функция Нтгдиддбегинмокомпфраме (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBeginMoCompFrame
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 45c359092d1a161aae7671c437fdb9683a2a8eb9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538543"
---
# <a name="ntgdiddbeginmocompframe-function"></a><span data-ttu-id="4c0c0-103">Функция Нтгдиддбегинмокомпфраме</span><span class="sxs-lookup"><span data-stu-id="4c0c0-103">NtGdiDdBeginMoCompFrame function</span></span>

<span data-ttu-id="4c0c0-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="4c0c0-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="4c0c0-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="4c0c0-106">Начинает декодировать новый кадр.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-106">Starts decoding a new frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c0c0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c0c0-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdBeginMoCompFrame(
  _In_    HANDLE                   hMoComp,
  _Inout_ PDD_BEGINMOCOMPFRAMEDATA puBeginFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="4c0c0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c0c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c0c0-109">*хмокомп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c0c0-109">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c0c0-110">Обработайте [**\_ \_ локальную структуру DD мотионкомп**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) , которая содержит описание запрошенной компенсации движения.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-110">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation being requested.</span></span>

</dd> <dt>

<span data-ttu-id="4c0c0-111">*пубегинфрамедата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4c0c0-111">*puBeginFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c0c0-112">Указатель на структуру [**DD \_ бегинмокомпфрамедата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_beginmocompframedata) , которая содержит сведения, необходимые для начала декодирования нового кадра.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-112">Pointer to a [**DD\_BEGINMOCOMPFRAMEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_beginmocompframedata) structure that contains the information needed to start decoding a new frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c0c0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c0c0-113">Return value</span></span>

<span data-ttu-id="4c0c0-114">**Нтгдиддбегинмокомпфраме** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-114">**NtGdiDdBeginMoCompFrame** returns one of the following callback codes.</span></span>



| <span data-ttu-id="4c0c0-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4c0c0-115">Return code</span></span>                                                                                              | <span data-ttu-id="4c0c0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4c0c0-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c0c0-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="4c0c0-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="4c0c0-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="4c0c0-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="4c0c0-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="4c0c0-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="4c0c0-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="4c0c0-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="4c0c0-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="4c0c0-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="4c0c0-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4c0c0-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c0c0-125">Remarks</span></span>

<span data-ttu-id="4c0c0-126">Дополнительные сведения см. в пакете средств разработки драйверов для Microsoft DirectX Video Acceleration Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="4c0c0-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c0c0-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4c0c0-127">Requirements</span></span>



| <span data-ttu-id="4c0c0-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4c0c0-128">Requirement</span></span> | <span data-ttu-id="4c0c0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4c0c0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c0c0-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c0c0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4c0c0-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4c0c0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4c0c0-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c0c0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4c0c0-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4c0c0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4c0c0-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4c0c0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c0c0-135"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c0c0-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c0c0-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c0c0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c0c0-137">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="4c0c0-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
