---
description: Повторно включает объект устройства режима ядра Microsoft DirectDraw после переключения режима.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Функция Нтгдиддринабледиректдравобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142202"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a><span data-ttu-id="230e7-103">Функция Нтгдиддринабледиректдравобжект</span><span class="sxs-lookup"><span data-stu-id="230e7-103">NtGdiDdReenableDirectDrawObject function</span></span>

<span data-ttu-id="230e7-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="230e7-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="230e7-105">Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="230e7-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="230e7-106">Повторно включает объект устройства режима ядра Microsoft DirectDraw после переключения режима.</span><span class="sxs-lookup"><span data-stu-id="230e7-106">Re-enables a Microsoft DirectDraw kernel-mode device object after a mode switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="230e7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="230e7-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a><span data-ttu-id="230e7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="230e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="230e7-109">*хдиректдравлокал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="230e7-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230e7-110">Объект DirectDraw, который необходимо включить заново.</span><span class="sxs-lookup"><span data-stu-id="230e7-110">DirectDraw object that needs to be re-enabled.</span></span>

</dd> <dt>

<span data-ttu-id="230e7-111">*пубневмоде* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="230e7-111">*pubNewMode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="230e7-112">Указатель на логическое значение, которое будет заполнено значением, которое указывает, изменился ли режим экрана.</span><span class="sxs-lookup"><span data-stu-id="230e7-112">Pointer to a BOOL that will be filled with a value that represents whether the display mode changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="230e7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="230e7-113">Return value</span></span>

<span data-ttu-id="230e7-114">В случае успеха (устройство может быть повторно включено) Эта функция возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="230e7-114">If successful (the device can be re-enabled), this function returns **TRUE**.</span></span> <span data-ttu-id="230e7-115">В противном случае (например, драйвер экрана был изменен), он возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="230e7-115">Otherwise (for example, the display driver was changed), it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="230e7-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="230e7-116">Remarks</span></span>

<span data-ttu-id="230e7-117">После повторного включения объекта можно повторно запросить возможности устройства с помощью вызова [**нтгдиддкуеридиректдравобжект**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span><span class="sxs-lookup"><span data-stu-id="230e7-117">Once the object has been re-enabled, the capabilities for the device can be re-queried via a call to [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span></span>

<span data-ttu-id="230e7-118">В приложениях рекомендуется использовать API DirectDraw или [Direct3D](../direct3d10/d3d10-graphics-reference.md) версии 8, который автоматизирует и абстрагирует этот процесс независимо от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="230e7-118">Applications are advised to use the DirectDraw or [Direct3D](../direct3d10/d3d10-graphics-reference.md) version 8 APIs, which automate and abstract this process in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="230e7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="230e7-119">Requirements</span></span>



| <span data-ttu-id="230e7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="230e7-120">Requirement</span></span> | <span data-ttu-id="230e7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="230e7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="230e7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="230e7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="230e7-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="230e7-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="230e7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="230e7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="230e7-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="230e7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="230e7-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="230e7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="230e7-127"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="230e7-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="230e7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="230e7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230e7-129">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="230e7-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="230e7-130">**ддринабледиректдравобжект**</span><span class="sxs-lookup"><span data-stu-id="230e7-130">**DdReenableDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
