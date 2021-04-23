---
description: Нтгдиддделетесурфацеобжект Удаляет ранее созданный объект поверхности режима ядра.
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: Функция Нтгдиддделетесурфацеобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03988b842aacc29915287490508eb9e9d057e907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655662"
---
# <a name="ntgdidddeletesurfaceobject-function"></a><span data-ttu-id="38a3f-103">Функция Нтгдиддделетесурфацеобжект</span><span class="sxs-lookup"><span data-stu-id="38a3f-103">NtGdiDdDeleteSurfaceObject function</span></span>

<span data-ttu-id="38a3f-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="38a3f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="38a3f-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="38a3f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="38a3f-106">**Нтгдиддделетесурфацеобжект** Удаляет ранее созданный объект поверхности режима ядра.</span><span class="sxs-lookup"><span data-stu-id="38a3f-106">**NtGdiDdDeleteSurfaceObject** deletes a previously created kernel-mode surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a3f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38a3f-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="38a3f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="38a3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38a3f-109">*хсурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38a3f-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38a3f-110">Обработчик для ранее созданного объекта поверхности режима ядра.</span><span class="sxs-lookup"><span data-stu-id="38a3f-110">Handle to the previously created kernel-mode surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38a3f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38a3f-111">Return value</span></span>

<span data-ttu-id="38a3f-112">В случае успеха эта функция возвращает **значение true**. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="38a3f-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="38a3f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38a3f-113">Remarks</span></span>

<span data-ttu-id="38a3f-114">В приложениях рекомендуется использовать интерфейсы API DirectDraw и [Direct3D](../direct3d10/d3d10-graphics-reference.md) для создания объектов графических устройств и управления ими.</span><span class="sxs-lookup"><span data-stu-id="38a3f-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="38a3f-115">Эти конструкции являются абстрактным процессом создания устройств в упрощенном и независимом от операционной системе виде.</span><span class="sxs-lookup"><span data-stu-id="38a3f-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="38a3f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="38a3f-116">Requirements</span></span>



| <span data-ttu-id="38a3f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="38a3f-117">Requirement</span></span> | <span data-ttu-id="38a3f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="38a3f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="38a3f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38a3f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="38a3f-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38a3f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="38a3f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38a3f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="38a3f-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38a3f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="38a3f-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="38a3f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="38a3f-124"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="38a3f-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38a3f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38a3f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a3f-126">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="38a3f-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="38a3f-127">**ддделетесурфацеобжект**</span><span class="sxs-lookup"><span data-stu-id="38a3f-127">**DdDeleteSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[<span data-ttu-id="38a3f-128">**нтгдиддкреатесурфацеобжект**</span><span class="sxs-lookup"><span data-stu-id="38a3f-128">**NtGdiDdCreateSurfaceObject**</span></span>](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
