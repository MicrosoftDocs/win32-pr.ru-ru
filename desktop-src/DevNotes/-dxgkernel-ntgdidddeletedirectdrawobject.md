---
description: Уничтожает ранее созданный объект устройства Microsoft DirectDraw в режиме ядра.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Функция Нтгдиддделетедиректдравобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 9ac10798f83fe7e1a07a0803dd29cfa9cd8b1c98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140943"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a><span data-ttu-id="dcfe5-103">Функция Нтгдиддделетедиректдравобжект</span><span class="sxs-lookup"><span data-stu-id="dcfe5-103">NtGdiDdDeleteDirectDrawObject function</span></span>

<span data-ttu-id="dcfe5-104">\[Эта функция может быть изменена при каждой редакции операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="dcfe5-105">Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]</span><span class="sxs-lookup"><span data-stu-id="dcfe5-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="dcfe5-106">Уничтожает ранее созданный объект устройства Microsoft DirectDraw в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-106">Destroys a previously created kernel-mode Microsoft DirectDraw device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcfe5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcfe5-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a><span data-ttu-id="dcfe5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcfe5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcfe5-109">*хдиректдравлокал*</span><span class="sxs-lookup"><span data-stu-id="dcfe5-109">*hDirectDrawLocal*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfe5-110">Обработчик объекта устройства DirectDraw режима ядра.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-110">Handle to the kernel-mode DirectDraw device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcfe5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcfe5-111">Return value</span></span>

<span data-ttu-id="dcfe5-112">В случае успеха эта функция возвращает **значение true**. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcfe5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcfe5-113">Remarks</span></span>

<span data-ttu-id="dcfe5-114">В приложениях рекомендуется использовать интерфейсы API DirectDraw и [Direct3D](../direct3d10/d3d10-graphics-reference.md) для создания объектов графических устройств и управления ими.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="dcfe5-115">Эти конструкции являются абстрактным процессом создания устройств в упрощенном и независимом от операционной системе виде.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcfe5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dcfe5-116">Requirements</span></span>



| <span data-ttu-id="dcfe5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dcfe5-117">Requirement</span></span> | <span data-ttu-id="dcfe5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dcfe5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfe5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dcfe5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dcfe5-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dcfe5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dcfe5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dcfe5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dcfe5-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dcfe5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dcfe5-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dcfe5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcfe5-124"><dt>Нтгди. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcfe5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcfe5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcfe5-126">Поддержка клиентов низкого уровня графики</span><span class="sxs-lookup"><span data-stu-id="dcfe5-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="dcfe5-127">**нтгдиддкреатедиректдравобжект**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-127">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[<span data-ttu-id="dcfe5-128">**ддделетедиректдравобжект**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-128">**DdDeleteDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
