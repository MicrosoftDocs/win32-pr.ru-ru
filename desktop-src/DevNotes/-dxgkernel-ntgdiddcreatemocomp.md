---
description: Уведомляет драйвер о том, что программный декодер начнет использовать компенсацию движения с указанным идентификатором GUID.
ms.assetid: c9a55428-7fe6-45dd-987a-d9ab8ae8a1cb
title: Функция Нтгдиддкреатемокомп (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1705b5bf7ac5eddd1ac39e14f3b91b7fd3728cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141407"
---
# <a name="ntgdiddcreatemocomp-function"></a><span data-ttu-id="9572e-103">Функция Нтгдиддкреатемокомп</span><span class="sxs-lookup"><span data-stu-id="9572e-103">NtGdiDdCreateMoComp function</span></span>

<span data-ttu-id="9572e-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9572e-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="9572e-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="9572e-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="9572e-106">Уведомляет драйвер о том, что программный декодер начнет использовать компенсацию движения с указанным идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="9572e-106">Notifies the driver that a software decoder will start using motion compensation with the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="9572e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9572e-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateMoComp(
  _In_    HANDLE               hDirectDraw,
  _Inout_ PDD_CREATEMOCOMPDATA puCreateMoCompData
);
```



## <a name="parameters"></a><span data-ttu-id="9572e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9572e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9572e-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9572e-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9572e-110">Обработчик для ранее созданного объекта режима ядра DirectDraw для устройства, на котором будет использоваться компенсация движения.</span><span class="sxs-lookup"><span data-stu-id="9572e-110">Handle to a previously created DirectDraw kernel-mode object for the device on which motion compensation is to be used.</span></span>

</dd> <dt>

<span data-ttu-id="9572e-111">*пукреатемокомпдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9572e-111">*puCreateMoCompData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9572e-112">Указатель на структуру [**DD \_ креатемокомпдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) , которая содержит сведения, необходимые для начала использования компенсации движения.</span><span class="sxs-lookup"><span data-stu-id="9572e-112">Pointer to a [**DD\_CREATEMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) structure that contains the information required to begin using motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9572e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9572e-113">Return value</span></span>

<span data-ttu-id="9572e-114">**Нтгдиддкреатемокомп** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="9572e-114">**NtGdiDdCreateMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="9572e-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9572e-115">Return code</span></span>                                                                                              | <span data-ttu-id="9572e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9572e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9572e-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="9572e-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="9572e-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="9572e-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="9572e-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="9572e-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="9572e-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="9572e-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="9572e-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="9572e-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="9572e-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="9572e-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="9572e-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9572e-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="9572e-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="9572e-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9572e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9572e-125">Remarks</span></span>

<span data-ttu-id="9572e-126">Дополнительные сведения см. в пакете средств разработки драйверов для Microsoft DirectX Video Acceleration Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="9572e-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="9572e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9572e-127">Requirements</span></span>



| <span data-ttu-id="9572e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9572e-128">Requirement</span></span> | <span data-ttu-id="9572e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9572e-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9572e-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9572e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9572e-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9572e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9572e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9572e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9572e-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9572e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9572e-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9572e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9572e-135"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="9572e-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9572e-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9572e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9572e-137">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="9572e-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
