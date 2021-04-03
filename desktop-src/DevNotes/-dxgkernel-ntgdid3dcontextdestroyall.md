---
description: Запрашивает объем свободной памяти в куче памяти, управляемой драйвером.
ms.assetid: d7f8792b-a515-4e70-9474-6a3474b6612b
title: Функция NtGdiD3DContextDestroyAll (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroyAll
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 8bb42c902555568ebe7a26656cd188e9c8e40213
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895685"
---
# <a name="ntgdid3dcontextdestroyall-function"></a><span data-ttu-id="67df3-103">Функция NtGdiD3DContextDestroyAll</span><span class="sxs-lookup"><span data-stu-id="67df3-103">NtGdiD3DContextDestroyAll function</span></span>

<span data-ttu-id="67df3-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="67df3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="67df3-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="67df3-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="67df3-106">Запрашивает объем свободной памяти в куче памяти, управляемой драйвером.</span><span class="sxs-lookup"><span data-stu-id="67df3-106">Queries the amount of free memory in the driver-managed memory heap.</span></span>

## <a name="syntax"></a><span data-ttu-id="67df3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67df3-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroyAll(void);
```



## <a name="parameters"></a><span data-ttu-id="67df3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="67df3-108">Parameters</span></span>

<span data-ttu-id="67df3-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="67df3-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67df3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67df3-110">Return value</span></span>

<span data-ttu-id="67df3-111">**NtGdiD3DContextDestroyAll** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="67df3-111">**NtGdiD3DContextDestroyAll** returns one of the following callback codes.</span></span>



| <span data-ttu-id="67df3-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="67df3-112">Return code</span></span>                                                                                              | <span data-ttu-id="67df3-113">Описание</span><span class="sxs-lookup"><span data-stu-id="67df3-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="67df3-114"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="67df3-114"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="67df3-115">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="67df3-115">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="67df3-116">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="67df3-116">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="67df3-117">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="67df3-117">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="67df3-118"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="67df3-118"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="67df3-119">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="67df3-119">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="67df3-120">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="67df3-120">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="67df3-121">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="67df3-121">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="67df3-122">Требования</span><span class="sxs-lookup"><span data-stu-id="67df3-122">Requirements</span></span>



| <span data-ttu-id="67df3-123">Требование</span><span class="sxs-lookup"><span data-stu-id="67df3-123">Requirement</span></span> | <span data-ttu-id="67df3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="67df3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67df3-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67df3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="67df3-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="67df3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="67df3-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67df3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="67df3-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="67df3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="67df3-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="67df3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="67df3-130"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="67df3-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67df3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67df3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67df3-132">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="67df3-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




