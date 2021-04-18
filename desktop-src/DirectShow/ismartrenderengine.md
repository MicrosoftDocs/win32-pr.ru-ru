---
description: Интерфейс Исмартрендеренгине предоставляет методы, поддерживающие интеллектуальное повторное сжатие в службах редактирования DirectShow (DES). Модуль интеллектуального просмотра предоставляет этот интерфейс.
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Интерфейс Исмартрендеренгине (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675378"
---
# <a name="ismartrenderengine-interface"></a><span data-ttu-id="084d7-104">Интерфейс Исмартрендеренгине</span><span class="sxs-lookup"><span data-stu-id="084d7-104">ISmartRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="084d7-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="084d7-105">\[Deprecated.</span></span> <span data-ttu-id="084d7-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="084d7-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="084d7-107">`ISmartRenderEngine`Интерфейс предоставляет методы, поддерживающие интеллектуальное повторное сжатие в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="084d7-107">The `ISmartRenderEngine` interface provides methods that support smart recompression in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="084d7-108">Модуль интеллектуального просмотра предоставляет этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="084d7-108">The smart render engine exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="084d7-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="084d7-109">Members</span></span>

<span data-ttu-id="084d7-110">Интерфейс **исмартрендеренгине** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="084d7-110">The **ISmartRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="084d7-111">**Исмартрендеренгине** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="084d7-111">**ISmartRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="084d7-112">Методы</span><span class="sxs-lookup"><span data-stu-id="084d7-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="084d7-113">Методы</span><span class="sxs-lookup"><span data-stu-id="084d7-113">Methods</span></span>

<span data-ttu-id="084d7-114">Интерфейс **исмартрендеренгине** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="084d7-114">The **ISmartRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="084d7-115">Метод</span><span class="sxs-lookup"><span data-stu-id="084d7-115">Method</span></span>                                                                | <span data-ttu-id="084d7-116">Описание</span><span class="sxs-lookup"><span data-stu-id="084d7-116">Description</span></span>                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="084d7-117">**жетграупкомпрессор**</span><span class="sxs-lookup"><span data-stu-id="084d7-117">**GetGroupCompressor**</span></span>](ismartrenderengine-getgroupcompressor.md)   | <span data-ttu-id="084d7-118">Извлекает фильтр сжатия для указанной группы.</span><span class="sxs-lookup"><span data-stu-id="084d7-118">Retrieves the compression filter for the specified group.</span></span><br/>                 |
| [<span data-ttu-id="084d7-119">**сетфиндкомпрессоркб**</span><span class="sxs-lookup"><span data-stu-id="084d7-119">**SetFindCompressorCB**</span></span>](ismartrenderengine-setfindcompressorcb.md) | <span data-ttu-id="084d7-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="084d7-120">Not implemented.</span></span><br/>                                                          |
| [<span data-ttu-id="084d7-121">**сетграупкомпрессор**</span><span class="sxs-lookup"><span data-stu-id="084d7-121">**SetGroupCompressor**</span></span>](ismartrenderengine-setgroupcompressor.md)   | <span data-ttu-id="084d7-122">Задает фильтр сжатия, используемый при подготовке к просмотру указанной группы.</span><span class="sxs-lookup"><span data-stu-id="084d7-122">Specifies a compression filter to use when rendering the specified group.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="084d7-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="084d7-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="084d7-124">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="084d7-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="084d7-125">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="084d7-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="084d7-126">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="084d7-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="084d7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="084d7-127">Requirements</span></span>



| <span data-ttu-id="084d7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="084d7-128">Requirement</span></span> | <span data-ttu-id="084d7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="084d7-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="084d7-130">Header</span><span class="sxs-lookup"><span data-stu-id="084d7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="084d7-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="084d7-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="084d7-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="084d7-132">Library</span></span><br/> | <dl> <span data-ttu-id="084d7-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="084d7-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="084d7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="084d7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="084d7-135">Подготовка проекта</span><span class="sxs-lookup"><span data-stu-id="084d7-135">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
