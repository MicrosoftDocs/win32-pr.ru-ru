---
description: Уведомляет драйвер о переключении приложения Microsoft DirectDraw в монопольный режим или из него.
ms.assetid: f2b63d90-7ede-479f-a2fd-ae9870c4d7b9
title: Функция Нтгдиддсетексклусивемоде (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetExclusiveMode
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1d2420f4ae093b4bfc3f68871daefd5c20da308e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655661"
---
# <a name="ntgdiddsetexclusivemode-function"></a><span data-ttu-id="7a5e2-103">Функция Нтгдиддсетексклусивемоде</span><span class="sxs-lookup"><span data-stu-id="7a5e2-103">NtGdiDdSetExclusiveMode function</span></span>

<span data-ttu-id="7a5e2-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="7a5e2-105">Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="7a5e2-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="7a5e2-106">Уведомляет драйвер о переключении приложения Microsoft DirectDraw в монопольный режим или из него.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-106">Notifies the driver when a Microsoft DirectDraw application is switching to or from exclusive mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5e2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a5e2-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetExclusiveMode(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_SETEXCLUSIVEMODEDATA puSetExclusiveModeData
);
```



## <a name="parameters"></a><span data-ttu-id="7a5e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a5e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5e2-109">*хдиректдрав* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a5e2-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5e2-110">Обработчик для ранее созданного объекта DirectDraw режима ядра.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="7a5e2-111">*пусетексклусивемодедата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7a5e2-111">*puSetExclusiveModeData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5e2-112">Указатель на структуру [**DD \_ сетексклусивемодедата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) , которая содержит сведения об уведомлении.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-112">Pointer to a [**DD\_SETEXCLUSIVEMODEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) structure that contains the notification information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5e2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a5e2-113">Return value</span></span>

<span data-ttu-id="7a5e2-114">**Нтгдиддсетексклусивемоде** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-114">**NtGdiDdSetExclusiveMode** returns one of the following callback codes.</span></span>



| <span data-ttu-id="7a5e2-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7a5e2-115">Return code</span></span>                                                                                              | <span data-ttu-id="7a5e2-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7a5e2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a5e2-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="7a5e2-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="7a5e2-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="7a5e2-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="7a5e2-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="7a5e2-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="7a5e2-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="7a5e2-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="7a5e2-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="7a5e2-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="7a5e2-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7a5e2-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7a5e2-125">Requirements</span></span>



| <span data-ttu-id="7a5e2-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7a5e2-126">Requirement</span></span> | <span data-ttu-id="7a5e2-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7a5e2-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5e2-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a5e2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5e2-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a5e2-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7a5e2-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a5e2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5e2-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a5e2-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7a5e2-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7a5e2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a5e2-133"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a5e2-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a5e2-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a5e2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5e2-135">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="7a5e2-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
