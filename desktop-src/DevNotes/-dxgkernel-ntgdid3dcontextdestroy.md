---
description: Удаляет указанный контекст.
ms.assetid: ac113178-bdb6-4601-940d-6b00b339904d
title: Функция NtGdiD3DContextDestroy (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroy
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 19799c3895072011dd104deec18664d1ffc52b9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538879"
---
# <a name="ntgdid3dcontextdestroy-function"></a><span data-ttu-id="8bf05-103">Функция NtGdiD3DContextDestroy</span><span class="sxs-lookup"><span data-stu-id="8bf05-103">NtGdiD3DContextDestroy function</span></span>

<span data-ttu-id="8bf05-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8bf05-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="8bf05-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="8bf05-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="8bf05-106">Удаляет указанный контекст.</span><span class="sxs-lookup"><span data-stu-id="8bf05-106">Deletes the specified context.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf05-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bf05-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroy(
  _In_ LPD3DNTHAL_CONTEXTDESTROYDATA pContextDestroyData
);
```



## <a name="parameters"></a><span data-ttu-id="8bf05-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bf05-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf05-109">*пконтекстдестройдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8bf05-109">*pContextDestroyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bf05-110">Указатель на структуру [**\_ контекстдестройдата D3DNTHAL**](/windows-hardware/drivers/ddi/) , которая содержит сведения, необходимые драйверу для уничтожения контекста.</span><span class="sxs-lookup"><span data-stu-id="8bf05-110">Pointer to a [**D3DNTHAL\_CONTEXTDESTROYDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to destroy the context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf05-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bf05-111">Return value</span></span>

<span data-ttu-id="8bf05-112">**NtGdiD3DContextDestroy** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8bf05-112">**NtGdiD3DContextDestroy** returns one of the following callback codes.</span></span>



| <span data-ttu-id="8bf05-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8bf05-113">Return code</span></span>                                                                                              | <span data-ttu-id="8bf05-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8bf05-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8bf05-115"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf05-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="8bf05-116">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="8bf05-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="8bf05-117">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="8bf05-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="8bf05-118">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="8bf05-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="8bf05-119"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf05-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="8bf05-120">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="8bf05-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="8bf05-121">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8bf05-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="8bf05-122">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="8bf05-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8bf05-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8bf05-123">Requirements</span></span>



| <span data-ttu-id="8bf05-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8bf05-124">Requirement</span></span> | <span data-ttu-id="8bf05-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf05-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf05-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bf05-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf05-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8bf05-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8bf05-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bf05-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf05-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8bf05-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8bf05-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8bf05-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf05-131"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf05-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf05-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bf05-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf05-133">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="8bf05-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
