---
description: Интерфейс IRenderEngine2 позволяет приложению заменить применяемый по умолчанию фильтр изменения размера видео, используемый службами редактирования DirectShow (DES). Базовый механизм визуализации и модуль интеллектуального просмотра поддерживают этот интерфейс.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Интерфейс IRenderEngine2 (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679841"
---
# <a name="irenderengine2-interface"></a><span data-ttu-id="2b335-104">Интерфейс IRenderEngine2</span><span class="sxs-lookup"><span data-stu-id="2b335-104">IRenderEngine2 interface</span></span>

> [!Note]  
> <span data-ttu-id="2b335-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2b335-105">\[Deprecated.</span></span> <span data-ttu-id="2b335-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2b335-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2b335-107">`IRenderEngine2`Интерфейс позволяет приложению заменить применяемый по умолчанию фильтр изменения размера видео, используемый службами редактирования DirectShow (DES).</span><span class="sxs-lookup"><span data-stu-id="2b335-107">The `IRenderEngine2` interface enables the application to replace the default video resizing filter used by DirectShow Editing Services (DES).</span></span> <span data-ttu-id="2b335-108">[Базовый механизм визуализации](basic-render-engine.md) и [модуль интеллектуального просмотра](smart-render-engine.md) поддерживают этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2b335-108">The [Basic Render Engine](basic-render-engine.md) and the [Smart Render Engine](smart-render-engine.md) both support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="2b335-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="2b335-109">Members</span></span>

<span data-ttu-id="2b335-110">Интерфейс **IRenderEngine2** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2b335-110">The **IRenderEngine2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2b335-111">**IRenderEngine2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2b335-111">**IRenderEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="2b335-112">Методы</span><span class="sxs-lookup"><span data-stu-id="2b335-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2b335-113">Методы</span><span class="sxs-lookup"><span data-stu-id="2b335-113">Methods</span></span>

<span data-ttu-id="2b335-114">Интерфейс **IRenderEngine2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2b335-114">The **IRenderEngine2** interface has these methods.</span></span>



| <span data-ttu-id="2b335-115">Метод</span><span class="sxs-lookup"><span data-stu-id="2b335-115">Method</span></span>                                                  | <span data-ttu-id="2b335-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2b335-116">Description</span></span>                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b335-117">**сетресизергуид**</span><span class="sxs-lookup"><span data-stu-id="2b335-117">**SetResizerGUID**</span></span>](irenderengine2-setresizerguid.md) | <span data-ttu-id="2b335-118">Указывает идентификатор CLSID пользовательского фильтра изменения размера, предоставленного приложением.</span><span class="sxs-lookup"><span data-stu-id="2b335-118">Specifies the CLSID of a custom resizing filter provided by the application.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b335-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b335-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2b335-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="2b335-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2b335-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b335-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2b335-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2b335-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2b335-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2b335-123">Requirements</span></span>



| <span data-ttu-id="2b335-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2b335-124">Requirement</span></span> | <span data-ttu-id="2b335-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2b335-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b335-126">Версия</span><span class="sxs-lookup"><span data-stu-id="2b335-126">Version</span></span><br/> | <span data-ttu-id="2b335-127">DirectX 9,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2b335-127">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="2b335-128">Header</span><span class="sxs-lookup"><span data-stu-id="2b335-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2b335-129"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b335-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2b335-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b335-130">Library</span></span><br/> | <dl> <span data-ttu-id="2b335-131"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b335-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b335-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b335-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b335-133">Предоставление пользовательского изменения размера видео</span><span class="sxs-lookup"><span data-stu-id="2b335-133">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
