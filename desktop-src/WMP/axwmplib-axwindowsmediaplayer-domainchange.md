---
title: Событие Домаинчанже объекта Аксвиндовсмедиаплайер
description: Событие Домаинчанже возникает при смене домена DVD. | Событие Домаинчанже объекта Аксвиндовсмедиаплайер
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Событие Домаинчанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698922"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="fae23-105">Событие Домаинчанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="fae23-105">DomainChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="fae23-106">Событие Домаинчанже возникает при смене домена DVD.</span><span class="sxs-lookup"><span data-stu-id="fae23-106">The DomainChange event occurs when the DVD domain changes.</span></span>

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a><span data-ttu-id="fae23-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="fae23-107">Event Data</span></span>

<span data-ttu-id="fae23-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ домаинчанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="fae23-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEventHandler**.</span></span> <span data-ttu-id="fae23-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ домаинчанжеевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="fae23-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="fae23-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="fae23-110">Property</span></span>  | <span data-ttu-id="fae23-111">Описание</span><span class="sxs-lookup"><span data-stu-id="fae23-111">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae23-112">стрдомаин</span><span class="sxs-lookup"><span data-stu-id="fae23-112">strDomain</span></span> | <span data-ttu-id="fae23-113">System. Стрингиндикатес новый домен.</span><span class="sxs-lookup"><span data-stu-id="fae23-113">System.StringIndicates the new domain.</span></span> <span data-ttu-id="fae23-114">Возможные значения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="fae23-114">For possible values, see the Remarks section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fae23-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fae23-115">Remarks</span></span>

<span data-ttu-id="fae23-116">В следующей таблице приведены возможные значения для свойства Стрдомаин.</span><span class="sxs-lookup"><span data-stu-id="fae23-116">The following table shows the possible values for the strDomain property.</span></span>



| <span data-ttu-id="fae23-117">Строка</span><span class="sxs-lookup"><span data-stu-id="fae23-117">String</span></span>            | <span data-ttu-id="fae23-118">Описание</span><span class="sxs-lookup"><span data-stu-id="fae23-118">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="fae23-119">фирстплай</span><span class="sxs-lookup"><span data-stu-id="fae23-119">firstPlay</span></span>         | <span data-ttu-id="fae23-120">Выполнение инициализации DVD-диска по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fae23-120">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="fae23-121">видеоманажермену</span><span class="sxs-lookup"><span data-stu-id="fae23-121">videoManagerMenu</span></span>  | <span data-ttu-id="fae23-122">Отображение меню для всего диска. Также называется корневым меню или Топмену.</span><span class="sxs-lookup"><span data-stu-id="fae23-122">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="fae23-123">видеотитлесетмену</span><span class="sxs-lookup"><span data-stu-id="fae23-123">videoTitleSetMenu</span></span> | <span data-ttu-id="fae23-124">Отображение меню для текущего набора заголовков.</span><span class="sxs-lookup"><span data-stu-id="fae23-124">Displaying menus for current title set.</span></span> <span data-ttu-id="fae23-125">Также называется Титлемену.</span><span class="sxs-lookup"><span data-stu-id="fae23-125">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="fae23-126">title</span><span class="sxs-lookup"><span data-stu-id="fae23-126">title</span></span>             | <span data-ttu-id="fae23-127">Отображение текущего заголовка.</span><span class="sxs-lookup"><span data-stu-id="fae23-127">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="fae23-128">stop</span><span class="sxs-lookup"><span data-stu-id="fae23-128">stop</span></span>              | <span data-ttu-id="fae23-129">Навигатор DVD находится в области DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="fae23-129">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

## <a name="requirements"></a><span data-ttu-id="fae23-130">Требования</span><span class="sxs-lookup"><span data-stu-id="fae23-130">Requirements</span></span>



| <span data-ttu-id="fae23-131">Требование</span><span class="sxs-lookup"><span data-stu-id="fae23-131">Requirement</span></span> | <span data-ttu-id="fae23-132">Значение</span><span class="sxs-lookup"><span data-stu-id="fae23-132">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae23-133">Версия</span><span class="sxs-lookup"><span data-stu-id="fae23-133">Version</span></span><br/>   | <span data-ttu-id="fae23-134">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fae23-134">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="fae23-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fae23-135">Namespace</span></span><br/> | <span data-ttu-id="fae23-136">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="fae23-136">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="fae23-137">Сборка</span><span class="sxs-lookup"><span data-stu-id="fae23-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fae23-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fae23-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fae23-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fae23-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae23-140">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="fae23-140">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fae23-141">**Интерфейс ИВМПДВД (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="fae23-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





