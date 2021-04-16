---
description: Класс Цимажепалетте управляет палитрами для модулей подготовки видео. Его можно использовать для создания логической палитры из формата видео. Этот класс предназначен для использования с классами Кбасевиндов и Кдравимаже, поэтому он является довольно специализированным.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: Класс Цимажепалетте
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672967"
---
# <a name="cimagepalette-class"></a><span data-ttu-id="3dcc2-105">Класс Цимажепалетте</span><span class="sxs-lookup"><span data-stu-id="3dcc2-105">CImagePalette class</span></span>

<span data-ttu-id="3dcc2-106">`CImagePalette`Класс управляет палитрами для модулей подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-106">The `CImagePalette` class manages palettes for video renderers.</span></span> <span data-ttu-id="3dcc2-107">Его можно использовать для создания логической палитры из формата видео.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-107">It can be used to create a logical palette from a video format.</span></span> <span data-ttu-id="3dcc2-108">Этот класс предназначен для использования с классами [**кбасевиндов**](cbasewindow.md) и [**кдравимаже**](cdrawimage.md) , поэтому он является довольно специализированным.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-108">This class is intended to be used with the [**CBaseWindow**](cbasewindow.md) and [**CDrawImage**](cdrawimage.md) classes, so it is somewhat specialized.</span></span>



| <span data-ttu-id="3dcc2-109">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="3dcc2-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="3dcc2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3dcc2-110">Description</span></span>                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3dcc2-111">**m \_ хпалетте**</span><span class="sxs-lookup"><span data-stu-id="3dcc2-111">**m\_hPalette**</span></span>](cimagepalette-m-hpalette.md)                  | <span data-ttu-id="3dcc2-112">Маркер логической палитры, которой управляет этот объект.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-112">Handle to the logical palette that this object manages.</span></span>                                        |
| [<span data-ttu-id="3dcc2-113">**m \_ пбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="3dcc2-113">**m\_pBaseWindow**</span></span>](cimagepalette-m-pbasewindow.md)            | <span data-ttu-id="3dcc2-114">Указатель на объект **кбасевиндов** , управляющий окном.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-114">Pointer to the **CBaseWindow** object that manages the window.</span></span>                                 |
| [<span data-ttu-id="3dcc2-115">**m \_ пдравимаже**</span><span class="sxs-lookup"><span data-stu-id="3dcc2-115">**m\_pDrawImage**</span></span>](cimagepalette-m-pdrawimage.md)              | <span data-ttu-id="3dcc2-116">Указатель на объект **кдравимаже** , который рисует изображение видео.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-116">Pointer to the **CDrawImage** object that draws the video image.</span></span>                               |
| [<span data-ttu-id="3dcc2-117">**m \_ пфилтер**</span><span class="sxs-lookup"><span data-stu-id="3dcc2-117">**m\_pFilter**</span></span>](cimagepalette-m-pfilter.md)                    | <span data-ttu-id="3dcc2-118">Указатель на фильтр-владелец.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-118">Pointer to the owning filter.</span></span>                                                                  |
| <span data-ttu-id="3dcc2-119">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="3dcc2-119">Public Methods</span></span>                                                   | <span data-ttu-id="3dcc2-120">Описание</span><span class="sxs-lookup"><span data-stu-id="3dcc2-120">Description</span></span>                                                                                    |
| [<span data-ttu-id="3dcc2-121">**Цимажепалетте**</span><span class="sxs-lookup"><span data-stu-id="3dcc2-121">**CImagePalette**</span></span>](cimagepalette-cimagepalette.md)             | <span data-ttu-id="3dcc2-122">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-122">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="3dcc2-123">**копипалетте**</span><span class="sxs-lookup"><span data-stu-id="3dcc2-123">**CopyPalette**</span></span>](cimagepalette-copypalette.md)                 | <span data-ttu-id="3dcc2-124">Копирует палитру из любой структуры **видеоинфо** в любую структуру палеттизед **видеоинфо** .</span><span class="sxs-lookup"><span data-stu-id="3dcc2-124">Copies the palette from any **VIDEOINFO** structure to any palettized **VIDEOINFO** structure.</span></span> |
| [<span data-ttu-id="3dcc2-125">**макеидентитипалетте**</span><span class="sxs-lookup"><span data-stu-id="3dcc2-125">**MakeIdentityPalette**</span></span>](cimagepalette-makeidentitypalette.md) | <span data-ttu-id="3dcc2-126">Пытается сделать палитру, которая сопоставляется непосредственно с палитрой, выбранной в устройстве вывода.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-126">Attempts to make a palette that maps directly to the palette selected in the display device.</span></span>   |
| [<span data-ttu-id="3dcc2-127">**макепалетте**</span><span class="sxs-lookup"><span data-stu-id="3dcc2-127">**MakePalette**</span></span>](cimagepalette-makepalette.md)                 | <span data-ttu-id="3dcc2-128">Создает логическую палитру из таблицы цветов в видеоформате.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-128">Creates a logical palette from the color table in a video format.</span></span>                              |
| [<span data-ttu-id="3dcc2-129">**препарепалетте**</span><span class="sxs-lookup"><span data-stu-id="3dcc2-129">**PreparePalette**</span></span>](cimagepalette-preparepalette.md)           | <span data-ttu-id="3dcc2-130">Настраивает палитру на основе типа носителя из фильтра-владельца.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-130">Sets up a palette, based on a media type from the owning filter.</span></span>                               |
| [<span data-ttu-id="3dcc2-131">**ремовепалетте**</span><span class="sxs-lookup"><span data-stu-id="3dcc2-131">**RemovePalette**</span></span>](cimagepalette-removepalette.md)             | <span data-ttu-id="3dcc2-132">Удаляет существующую логическую палитру.</span><span class="sxs-lookup"><span data-stu-id="3dcc2-132">Deletes the existing logical palette.</span></span>                                                          |



 

 

 



