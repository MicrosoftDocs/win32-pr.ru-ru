---
description: Элементы для получения образа Windows (WIA) 2,0 группируются в категории, определяющие, как обрабатывается или используется IWiaItem2.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: Идентификаторы GUID категории элементов WIA 2,0 (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711076"
---
# <a name="wia-20-item-category-guids"></a><span data-ttu-id="3f18f-103">Идентификаторы GUID категории элементов WIA 2,0</span><span class="sxs-lookup"><span data-stu-id="3f18f-103">WIA 2.0 Item Category GUIDs</span></span>

<span data-ttu-id="3f18f-104">Элементы для получения образа Windows (WIA) 2,0 группируются в категории, определяющие, как обрабатывается или используется [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3f18f-104">Windows Image Acquisition (WIA) 2.0 items are grouped into categories that define how a [**IWiaItem2**](-wia-iwiaitem2.md) is to be treated or used.</span></span> <span data-ttu-id="3f18f-105">Например, если элемент представляет устройство подачи, то приложение должно содержать необходимые свойства устройства подачи документов и действовать как устройство подачи документов.</span><span class="sxs-lookup"><span data-stu-id="3f18f-105">For example, if the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="3f18f-106">Если элемент представляет готовый файл, то приложение WIA 2,0 должно обрабатывать его таким образом, предполагая, что данные статичны и расположены на устройстве.</span><span class="sxs-lookup"><span data-stu-id="3f18f-106">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="3f18f-107">(Правила для каждого элемента будут определены в отдельных документах спецификации.) Каждая категория имеет константу типа GUID.</span><span class="sxs-lookup"><span data-stu-id="3f18f-107">(The rules for each item will be defined in their individual specification documents.) Each category has a GUID type constant.</span></span>



| <span data-ttu-id="3f18f-108">Константа</span><span class="sxs-lookup"><span data-stu-id="3f18f-108">Constant</span></span>                                                                                                                                                                                               | <span data-ttu-id="3f18f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3f18f-109">Description</span></span>                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <span data-ttu-id="3f18f-110"><dt>**\_Автоматическая категория \_ WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="3f18f-110"><dt>**WIA\_CATEGORY\_AUTO**</dt></span></span> </dl>                             | <span data-ttu-id="3f18f-111">Элемент, представляющий параметры автоматической настройки для устройства со сканером WIA 2,0, поддерживающего автоматическую настройку сканирования.</span><span class="sxs-lookup"><span data-stu-id="3f18f-111">An item that represents the automatic configuration settings for a WIA 2.0 scanner device that supports auto-configured scanning.</span></span><br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <span data-ttu-id="3f18f-112"><dt>**\_податчик категории WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f18f-112"><dt>**WIA\_CATEGORY\_FEEDER**</dt></span></span> </dl>                       | <span data-ttu-id="3f18f-113">Элемент веб-канала, который является программируемым источником данных и соответствует стандартным правилам и наборам свойств, необходимым для поддержки податчиков документов.</span><span class="sxs-lookup"><span data-stu-id="3f18f-113">A feeder item that is a programmable data source and follows the standard rules and property sets required to support document feeders.</span></span><br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <span data-ttu-id="3f18f-114"><dt>**\_ \_ обратный подачи категории WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f18f-114"><dt>**WIA\_CATEGORY\_FEEDER\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="3f18f-115">Программируемый источник данных, описывающий источник данных обратной стороны для дуплексного элемента податчика.</span><span class="sxs-lookup"><span data-stu-id="3f18f-115">A programmable data source describing the back side data source of a duplex base feeder item.</span></span><br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <span data-ttu-id="3f18f-116"><dt>**\_ \_ Передняя сторона подачи категории \_ WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="3f18f-116"><dt>**WIA\_CATEGORY\_FEEDER\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="3f18f-117">Программируемый источник данных, описывающий источник данных переднего плана для дуплексного элемента податчика.</span><span class="sxs-lookup"><span data-stu-id="3f18f-117">A programmable data source describing the front side data source of a duplex base feeder item.</span></span><br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <span data-ttu-id="3f18f-118"><dt>**\_пленка для категории WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f18f-118"><dt>**WIA\_CATEGORY\_FILM**</dt></span></span> </dl>                             | <span data-ttu-id="3f18f-119">Элемент пленки, который является программируемым источником данных и соответствует стандартным правилам и наборам свойств, необходимым для поддержки единиц сканирования пленки.</span><span class="sxs-lookup"><span data-stu-id="3f18f-119">A film item that is a programmable data source and follows the standard rules and property sets required to support film scanning units.</span></span><br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <span data-ttu-id="3f18f-120"><dt>**файл, в котором \_ Категория WIA \_ завершена \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f18f-120"><dt>**WIA\_CATEGORY\_FINISHED\_FILE**</dt></span></span> </dl> | <span data-ttu-id="3f18f-121">Элемент, который не является программируемым источником данных или элементом, предоставляющим данные в формате готового файла, или элемент папки, содержащий элементы формата "завершено".</span><span class="sxs-lookup"><span data-stu-id="3f18f-121">An item that is not a programmable data source, or an item that provides data in a finished file format, or a folder item that contains finished file format items.</span></span><br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <span data-ttu-id="3f18f-122"><dt>**\_стекло категории \_ WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="3f18f-122"><dt>**WIA\_CATEGORY\_FLATBED**</dt></span></span> </dl>                    | <span data-ttu-id="3f18f-123">Планшетный элемент, который является программируемым источником данных и соответствует стандартным правилам и наборам свойств, необходимым для поддержки сканирования в Платен.</span><span class="sxs-lookup"><span data-stu-id="3f18f-123">A flatbed item that is a programmable data source and follows the standard rules and property sets required to support flatbed platen scanning.</span></span><br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <span data-ttu-id="3f18f-124"><dt>**\_Папка категории \_ WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="3f18f-124"><dt>**WIA\_CATEGORY\_FOLDER**</dt></span></span> </dl>                       | <span data-ttu-id="3f18f-125">Элемент хранилища папок (не программируемый источник данных), содержащий другие элементы папки или готовые файлы или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="3f18f-125">A folder storage item (not a programmable data source) containing other folder items or finished files or both.</span></span><br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <span data-ttu-id="3f18f-126"><dt>**\_корень категории \_ WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="3f18f-126"><dt>**WIA\_CATEGORY\_ROOT**</dt></span></span> </dl>                             | <span data-ttu-id="3f18f-127">Корневой элемент для устройства.</span><span class="sxs-lookup"><span data-stu-id="3f18f-127">The root item for the device.</span></span> <br/>                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="3f18f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="3f18f-128">Requirements</span></span>



| <span data-ttu-id="3f18f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="3f18f-129">Requirement</span></span> | <span data-ttu-id="3f18f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="3f18f-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3f18f-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f18f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3f18f-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f18f-132">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3f18f-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f18f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3f18f-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f18f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3f18f-135">Header</span><span class="sxs-lookup"><span data-stu-id="3f18f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f18f-136"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f18f-136"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




