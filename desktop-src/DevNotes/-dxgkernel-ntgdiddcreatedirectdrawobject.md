---
description: Создает представление объекта Microsoft DirectDraw на стороне ядра.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: Функция Нтгдиддкреатедиректдравобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140947"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a><span data-ttu-id="69d2a-103">Функция Нтгдиддкреатедиректдравобжект</span><span class="sxs-lookup"><span data-stu-id="69d2a-103">NtGdiDdCreateDirectDrawObject function</span></span>

<span data-ttu-id="69d2a-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="69d2a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="69d2a-105">Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="69d2a-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="69d2a-106">Создает представление объекта Microsoft DirectDraw на стороне ядра.</span><span class="sxs-lookup"><span data-stu-id="69d2a-106">Creates a kernel-side representation of the Microsoft DirectDraw object.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d2a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69d2a-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a><span data-ttu-id="69d2a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="69d2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d2a-109">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69d2a-109">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d2a-110">Любое устройство показа контроллеров домена, для которого должен быть создан объект DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="69d2a-110">Any DC display device for which the DirectDraw object should be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d2a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69d2a-111">Return value</span></span>

<span data-ttu-id="69d2a-112">В случае успеха эта функция возвращает маркер в представление объекта режима ядра; в противном случае возвращается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="69d2a-112">If successful, this function returns a handle to the kernel-mode object representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="69d2a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69d2a-113">Remarks</span></span>

<span data-ttu-id="69d2a-114">В приложениях рекомендуется использовать интерфейсы API DirectDraw и [Direct3D](../direct3d10/d3d10-graphics-reference.md) для создания объектов графических устройств и управления ими.</span><span class="sxs-lookup"><span data-stu-id="69d2a-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="69d2a-115">Эти конструкции являются абстрактным процессом создания устройств в упрощенном и независимом от операционной системе виде.</span><span class="sxs-lookup"><span data-stu-id="69d2a-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d2a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="69d2a-116">Requirements</span></span>



| <span data-ttu-id="69d2a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="69d2a-117">Requirement</span></span> | <span data-ttu-id="69d2a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="69d2a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69d2a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69d2a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="69d2a-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="69d2a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="69d2a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69d2a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="69d2a-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="69d2a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="69d2a-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="69d2a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="69d2a-124"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="69d2a-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69d2a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69d2a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d2a-126">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="69d2a-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="69d2a-127">**ддкреатедиректдравобжект**</span><span class="sxs-lookup"><span data-stu-id="69d2a-127">**DdCreateDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
