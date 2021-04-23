---
description: Приводит к взаимозаменяемости памяти поверхности, связанной с целевой и текущей областями.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Функция Нтгдиддфлип (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895865"
---
# <a name="ntgdiddflip-function"></a><span data-ttu-id="4be25-103">Функция Нтгдиддфлип</span><span class="sxs-lookup"><span data-stu-id="4be25-103">NtGdiDdFlip function</span></span>

<span data-ttu-id="4be25-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4be25-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="4be25-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="4be25-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="4be25-106">Приводит к взаимозаменяемости памяти поверхности, связанной с целевой и текущей областями.</span><span class="sxs-lookup"><span data-stu-id="4be25-106">Causes the surface memory associated with the target and current surfaces to be interchanged.</span></span>

## <a name="syntax"></a><span data-ttu-id="4be25-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4be25-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a><span data-ttu-id="4be25-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4be25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be25-109">*хсурфацекуррент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4be25-109">*hSurfaceCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4be25-110">Маркер [ \_ \_ локальной структуры области DD](https://msdn.microsoft.com/library/ms793861.aspx) , описывающей текущую поверхность.</span><span class="sxs-lookup"><span data-stu-id="4be25-110">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current surface.</span></span>

</dd> <dt>

<span data-ttu-id="4be25-111">*хсурфацетаржет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4be25-111">*hSurfaceTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4be25-112">Маркер [ \_ \_ локальной структуры области DD](https://msdn.microsoft.com/library/ms793861.aspx) , описывающей целевую поверхность, то есть поверхность, в которую драйвер должен перевернуться.</span><span class="sxs-lookup"><span data-stu-id="4be25-112">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the target surface; that is, the surface to which the driver should flip.</span></span>

</dd> <dt>

<span data-ttu-id="4be25-113">*хсурфацекуррентлефт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4be25-113">*hSurfaceCurrentLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4be25-114">Маркер [ \_ \_ локальной структуры области DD](https://msdn.microsoft.com/library/ms793861.aspx) , описывающей текущую левую поверхность.</span><span class="sxs-lookup"><span data-stu-id="4be25-114">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current left surface.</span></span>

</dd> <dt>

<span data-ttu-id="4be25-115">*хсурфацетаржетлефт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4be25-115">*hSurfaceTargetLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4be25-116">Обработана [ \_ \_ локальная структура области DD](https://msdn.microsoft.com/library/ms793861.aspx) , описывающая левую целевую поверхность для отражения.</span><span class="sxs-lookup"><span data-stu-id="4be25-116">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the left target surface to flip to.</span></span>

</dd> <dt>

<span data-ttu-id="4be25-117">*пуфлипдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4be25-117">*puFlipData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4be25-118">Указатель на структуру [DD \_ флипдата](https://msdn.microsoft.com/library/ms794213.aspx) , которая содержит сведения, необходимые для выполнения перелистывания.</span><span class="sxs-lookup"><span data-stu-id="4be25-118">Pointer to a [DD\_FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) structure that contains the information required to perform the flip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4be25-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4be25-119">Return value</span></span>

<span data-ttu-id="4be25-120">**Нтгдиддфлип** возвращает один из следующих кодов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="4be25-120">**NtGdiDdFlip** returns one of the following callback codes.</span></span>



| <span data-ttu-id="4be25-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4be25-121">Return code</span></span>                                                                                              | <span data-ttu-id="4be25-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4be25-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4be25-123"><dt>**\_драйвер ддхал \_ обработан**</dt></span><span class="sxs-lookup"><span data-stu-id="4be25-123"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="4be25-124">Драйвер выполнил операцию и вернул допустимый код возврата для этой операции.</span><span class="sxs-lookup"><span data-stu-id="4be25-124">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="4be25-125">Если этот код имеет значение DD \_ , то DirectDraw или Direct3D продолжает работу с функцией.</span><span class="sxs-lookup"><span data-stu-id="4be25-125">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="4be25-126">В противном случае DirectDraw или Direct3D возвращает код ошибки, предоставленный драйвером, и прерывает функцию.</span><span class="sxs-lookup"><span data-stu-id="4be25-126">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="4be25-127"><dt>**\_драйвер ддхал \_ носандлед**</dt></span><span class="sxs-lookup"><span data-stu-id="4be25-127"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="4be25-128">Драйвер не имеет комментариев к запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="4be25-128">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="4be25-129">Если драйверу требуется реализовать определенный обратный вызов, DirectDraw или Direct3D сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4be25-129">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="4be25-130">В противном случае DirectDraw или Direct3D обрабатывает операцию так, как если бы обратный вызов драйвера не был определен путем выполнения аппаратной реализации DirectDraw или Direct3D, независимой от устройства.</span><span class="sxs-lookup"><span data-stu-id="4be25-130">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4be25-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4be25-131">Requirements</span></span>



| <span data-ttu-id="4be25-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4be25-132">Requirement</span></span> | <span data-ttu-id="4be25-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4be25-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4be25-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4be25-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4be25-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4be25-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4be25-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4be25-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4be25-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4be25-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4be25-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4be25-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4be25-139"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="4be25-139"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4be25-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4be25-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4be25-141">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="4be25-141">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




