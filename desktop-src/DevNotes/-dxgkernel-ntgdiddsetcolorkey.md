---
description: Задает значение ключа цвета для указанной поверхности.
ms.assetid: 052dba97-c047-4ef7-a908-2a66ade3af10
title: Функция Нтгдиддсетколоркэй (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetColorKey
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7d6186df13ee88ca3de4f123381c012548b1cd85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538405"
---
# <a name="ntgdiddsetcolorkey-function"></a><span data-ttu-id="dc1c0-103">Функция Нтгдиддсетколоркэй</span><span class="sxs-lookup"><span data-stu-id="dc1c0-103">NtGdiDdSetColorKey function</span></span>

<span data-ttu-id="dc1c0-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="dc1c0-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="dc1c0-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="dc1c0-106">Задает значение ключа цвета для указанной поверхности.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-106">Sets the color key value for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1c0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc1c0-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetColorKey(
  _In_    HANDLE              hSurface,
  _Inout_ PDD_SETCOLORKEYDATA puSetColorKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="dc1c0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc1c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc1c0-109">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc1c0-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc1c0-110">Указатель на [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , описывающую поверхность, с которой должен быть связан цветовой ключ.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-110">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface with which the color key is to be associated.</span></span>

</dd> <dt>

<span data-ttu-id="dc1c0-111">*пусетколоркэйдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dc1c0-111">*puSetColorKeyData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc1c0-112">Указатель на структуру [**DD \_ сетколоркэйдата**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) , которая содержит сведения, необходимые для установки ключа цвета для указанной поверхности.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-112">Pointer to a [**DD\_SETCOLORKEYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) structure that contains the information required to set the color key for the specified surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc1c0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc1c0-113">Return value</span></span>

<span data-ttu-id="dc1c0-114">**Нтгдиддсетколоркэй** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-114">**NtGdiDdSetColorKey** returns one of the following callback codes.</span></span>



| <span data-ttu-id="dc1c0-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dc1c0-115">Return code</span></span>                                                                                              | <span data-ttu-id="dc1c0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dc1c0-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc1c0-117"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c0-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="dc1c0-118">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="dc1c0-119">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="dc1c0-120">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="dc1c0-121"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c0-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="dc1c0-122">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="dc1c0-123">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="dc1c0-124">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="dc1c0-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dc1c0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dc1c0-125">Requirements</span></span>



| <span data-ttu-id="dc1c0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dc1c0-126">Requirement</span></span> | <span data-ttu-id="dc1c0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dc1c0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc1c0-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc1c0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dc1c0-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dc1c0-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dc1c0-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc1c0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dc1c0-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dc1c0-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dc1c0-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dc1c0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc1c0-133"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c0-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc1c0-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc1c0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc1c0-135">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="dc1c0-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
