---
description: Присоединяет два представления поверхности режима ядра.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Функция Нтгдиддаттачсурфаце (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655741"
---
# <a name="ntgdiddattachsurface-function"></a><span data-ttu-id="8d7fd-103">Функция Нтгдиддаттачсурфаце</span><span class="sxs-lookup"><span data-stu-id="8d7fd-103">NtGdiDdAttachSurface function</span></span>

<span data-ttu-id="8d7fd-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="8d7fd-105">Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="8d7fd-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="8d7fd-106">Присоединяет два представления поверхности режима ядра.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-106">Attaches two kernel-mode surface representations.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d7fd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d7fd-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a><span data-ttu-id="8d7fd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d7fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d7fd-109">*хсурфацефром* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d7fd-109">*hSurfaceFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d7fd-110">Указатель на объект поверхности режима ядра, который будет начальной точкой нового вложения.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-110">Handle to kernel-mode surface object that will be the start point of the new attachment.</span></span>

</dd> <dt>

<span data-ttu-id="8d7fd-111">*хсурфацето* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d7fd-111">*hSurfaceTo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d7fd-112">Обработайте объект поверхности режима ядра, который будет конечной точкой нового вложения.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-112">Handle to kernel-mode surface object that will be the end point of the new attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d7fd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d7fd-113">Return value</span></span>

<span data-ttu-id="8d7fd-114">**Нтгдиддаттачсурфаце** возвращает одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="8d7fd-114">**NtGdiDdAttachSurface** returns one of the following:</span></span>



| <span data-ttu-id="8d7fd-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8d7fd-115">Return code</span></span>                                                                          | <span data-ttu-id="8d7fd-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8d7fd-116">Description</span></span>                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="8d7fd-117"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7fd-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="8d7fd-118">Вызов функции прошел.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-118">The function call succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="8d7fd-119"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7fd-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="8d7fd-120">Сбой вызова функции.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-120">The function call failed.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="8d7fd-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d7fd-121">Remarks</span></span>

<span data-ttu-id="8d7fd-122">Полное описание вложений Surface см. в пакете SDK и пакете средств разработки драйверов (DDK) для DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-122">See the DirectDraw  software development kit (SDK) and Driver Development Kit (DDK) for a full description of surface attachments.</span></span>

> [!Note]  
> <span data-ttu-id="8d7fd-123">Как и в случае с другими вложениями в контактах, полученное вложение является односторонней стороной.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-123">As with other surface attachments, the resulting attachment is one-way.</span></span> <span data-ttu-id="8d7fd-124">После вызова этой функции *хсурфацето* не будет присоединен к *хсурфацефром*.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-124">After this function is called, *hSurfaceTo* will not be attached to *hSurfaceFrom*.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8d7fd-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8d7fd-125">Requirements</span></span>



| <span data-ttu-id="8d7fd-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8d7fd-126">Requirement</span></span> | <span data-ttu-id="8d7fd-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8d7fd-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8d7fd-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d7fd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8d7fd-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d7fd-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8d7fd-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d7fd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8d7fd-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d7fd-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8d7fd-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8d7fd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d7fd-133"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d7fd-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d7fd-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d7fd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d7fd-135">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="8d7fd-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




