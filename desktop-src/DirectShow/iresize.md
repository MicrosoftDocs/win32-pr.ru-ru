---
description: 'Интерфейс Иресизе должен поддерживаться любым настраиваемым фильтром изменения размеров видео для служб редактирования DirectShow (DES). Чтобы задать настраиваемый фильтр изменения размера, вызовите метод IRenderEngine2:: Сетресизергуид в подсистеме визуализации.'
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Интерфейс Иресизе (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674973"
---
# <a name="iresize-interface"></a><span data-ttu-id="871e5-104">Интерфейс Иресизе</span><span class="sxs-lookup"><span data-stu-id="871e5-104">IResize interface</span></span>

> [!Note]  
> <span data-ttu-id="871e5-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="871e5-105">\[Deprecated.</span></span> <span data-ttu-id="871e5-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="871e5-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="871e5-107">`IResize`Интерфейс должен поддерживаться любым настраиваемым фильтром изменения размеров видео для служб редактирования DirectShow (DES).</span><span class="sxs-lookup"><span data-stu-id="871e5-107">The `IResize` interface must be supported by any custom video resizer filter for DirectShow Editing Services (DES).</span></span> <span data-ttu-id="871e5-108">Чтобы задать настраиваемый фильтр изменения размера, вызовите метод [**IRenderEngine2:: сетресизергуид**](irenderengine2-setresizerguid.md) в подсистеме визуализации.</span><span class="sxs-lookup"><span data-stu-id="871e5-108">To set a custom resizer filter, call the [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) method on the render engine.</span></span>

## <a name="members"></a><span data-ttu-id="871e5-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="871e5-109">Members</span></span>

<span data-ttu-id="871e5-110">Интерфейс **иресизе** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="871e5-110">The **IResize** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="871e5-111">**Иресизе** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="871e5-111">**IResize** also has these types of members:</span></span>

-   [<span data-ttu-id="871e5-112">Методы</span><span class="sxs-lookup"><span data-stu-id="871e5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="871e5-113">Методы</span><span class="sxs-lookup"><span data-stu-id="871e5-113">Methods</span></span>

<span data-ttu-id="871e5-114">Интерфейс **иресизе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="871e5-114">The **IResize** interface has these methods.</span></span>



| <span data-ttu-id="871e5-115">Метод</span><span class="sxs-lookup"><span data-stu-id="871e5-115">Method</span></span>                                          | <span data-ttu-id="871e5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="871e5-116">Description</span></span>                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="871e5-117">**получить \_ инпутсизе**</span><span class="sxs-lookup"><span data-stu-id="871e5-117">**get\_InputSize**</span></span>](iresize-get-inputsize.md) | <span data-ttu-id="871e5-118">Возвращает текущий размер входных данных фильтра изменения размера.</span><span class="sxs-lookup"><span data-stu-id="871e5-118">Returns the resizer filter's current input size.</span></span><br/>  |
| [<span data-ttu-id="871e5-119">**получить \_ mediaType**</span><span class="sxs-lookup"><span data-stu-id="871e5-119">**get\_MediaType**</span></span>](iresize-get-mediatype.md) | <span data-ttu-id="871e5-120">Возвращает тип выходного носителя фильтра изменения.</span><span class="sxs-lookup"><span data-stu-id="871e5-120">Returns the resizer filter's output media type.</span></span><br/>   |
| [<span data-ttu-id="871e5-121">**получить \_ Размер**</span><span class="sxs-lookup"><span data-stu-id="871e5-121">**get\_Size**</span></span>](iresize-get-size.md)           | <span data-ttu-id="871e5-122">Возвращает текущий размер выходных данных и режим Stretch.</span><span class="sxs-lookup"><span data-stu-id="871e5-122">Returns the current output size and stretch mode.</span></span><br/> |
| [<span data-ttu-id="871e5-123">**разместить \_ mediaType**</span><span class="sxs-lookup"><span data-stu-id="871e5-123">**put\_MediaType**</span></span>](iresize-put-mediatype.md) | <span data-ttu-id="871e5-124">Задает тип выходного носителя.</span><span class="sxs-lookup"><span data-stu-id="871e5-124">Sets the output media type.</span></span><br/>                       |
| [<span data-ttu-id="871e5-125">**\_размер размещения**</span><span class="sxs-lookup"><span data-stu-id="871e5-125">**put\_Size**</span></span>](iresize-put-size.md)           | <span data-ttu-id="871e5-126">Задает размер выходных данных и режим Stretch.</span><span class="sxs-lookup"><span data-stu-id="871e5-126">Sets the output size and stretch mode.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="871e5-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="871e5-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="871e5-128">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="871e5-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="871e5-129">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="871e5-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="871e5-130">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="871e5-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="871e5-131">Требования</span><span class="sxs-lookup"><span data-stu-id="871e5-131">Requirements</span></span>



| <span data-ttu-id="871e5-132">Требование</span><span class="sxs-lookup"><span data-stu-id="871e5-132">Requirement</span></span> | <span data-ttu-id="871e5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="871e5-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="871e5-134">Версия</span><span class="sxs-lookup"><span data-stu-id="871e5-134">Version</span></span><br/> | <span data-ttu-id="871e5-135">DirectX 9,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="871e5-135">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="871e5-136">Header</span><span class="sxs-lookup"><span data-stu-id="871e5-136">Header</span></span><br/>  | <dl> <span data-ttu-id="871e5-137"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="871e5-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="871e5-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="871e5-138">Library</span></span><br/> | <dl> <span data-ttu-id="871e5-139"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="871e5-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="871e5-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="871e5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="871e5-141">Предоставление пользовательского изменения размера видео</span><span class="sxs-lookup"><span data-stu-id="871e5-141">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
