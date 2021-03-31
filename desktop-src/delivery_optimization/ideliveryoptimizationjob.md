---
title: Интерфейс Иделиверйоптимизатионжоб (Deliveryoptimization. h)
description: Используйте интерфейс Иделиверйоптимизатионжоб для скачивания диапазонов файла.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Интерфейс Иделиверйоптимизатионжоб
- Интерфейс Иделиверйоптимизатионжоб, описание
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135882"
---
# <a name="ideliveryoptimizationjob-interface"></a><span data-ttu-id="e8312-105">Интерфейс Иделиверйоптимизатионжоб</span><span class="sxs-lookup"><span data-stu-id="e8312-105">IDeliveryOptimizationJob interface</span></span>

<span data-ttu-id="e8312-106">Используйте интерфейс **иделиверйоптимизатионжоб** для скачивания диапазонов файла.</span><span class="sxs-lookup"><span data-stu-id="e8312-106">Use the **IDeliveryOptimizationJob** interface to download ranges of a file.</span></span>

## <a name="members"></a><span data-ttu-id="e8312-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="e8312-107">Members</span></span>

<span data-ttu-id="e8312-108">Интерфейс **иделиверйоптимизатионжоб** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e8312-108">The **IDeliveryOptimizationJob** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e8312-109">**Иделиверйоптимизатионжоб** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e8312-109">**IDeliveryOptimizationJob** also has these types of members:</span></span>

- [<span data-ttu-id="e8312-110">Методы</span><span class="sxs-lookup"><span data-stu-id="e8312-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e8312-111">Методы</span><span class="sxs-lookup"><span data-stu-id="e8312-111">Methods</span></span>

<span data-ttu-id="e8312-112">Интерфейс **иделиверйоптимизатионжоб** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e8312-112">The **IDeliveryOptimizationJob** interface has these methods.</span></span>



| <span data-ttu-id="e8312-113">Метод</span><span class="sxs-lookup"><span data-stu-id="e8312-113">Method</span></span>                                                                  | <span data-ttu-id="e8312-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e8312-114">Description</span></span>                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8312-115">**аддфилевисранжес**</span><span class="sxs-lookup"><span data-stu-id="e8312-115">**AddFileWithRanges**</span></span>](ideliveryoptimizationjob-addfilewithranges.md) | <span data-ttu-id="e8312-116">Добавляет файл в задание загрузки и задает диапазоны файлов, которые необходимо загрузить.</span><span class="sxs-lookup"><span data-stu-id="e8312-116">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e8312-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e8312-117">Requirements</span></span>



| <span data-ttu-id="e8312-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e8312-118">Requirement</span></span> | <span data-ttu-id="e8312-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e8312-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8312-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8312-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e8312-121">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e8312-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e8312-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8312-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e8312-123">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e8312-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e8312-124">Header</span><span class="sxs-lookup"><span data-stu-id="e8312-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8312-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8312-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8312-126">IDL</span><span class="sxs-lookup"><span data-stu-id="e8312-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8312-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e8312-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e8312-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e8312-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="e8312-129"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8312-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e8312-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e8312-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8312-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8312-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e8312-132">IID</span><span class="sxs-lookup"><span data-stu-id="e8312-132">IID</span></span><br/>                      | <span data-ttu-id="e8312-133">IID_IDeliveryOptimizationJob определяется как EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="e8312-133">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



 

