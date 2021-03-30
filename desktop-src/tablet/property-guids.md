---
description: Распознаватели Майкрософт используют следующие идентификаторы GUID.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: Идентификаторы GUID свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156874"
---
# <a name="property-guids"></a><span data-ttu-id="085d3-103">Идентификаторы GUID свойств</span><span class="sxs-lookup"><span data-stu-id="085d3-103">Property GUIDs</span></span>

<span data-ttu-id="085d3-104">Распознаватели Майкрософт используют следующие идентификаторы GUID.</span><span class="sxs-lookup"><span data-stu-id="085d3-104">The Microsoft recognizers use the following GUIDs.</span></span> <span data-ttu-id="085d3-105">Везде, где это возможно, приложения должны использовать эти идентификаторы GUID.</span><span class="sxs-lookup"><span data-stu-id="085d3-105">Whenever possible, applications should use these GUIDs.</span></span> <span data-ttu-id="085d3-106">Однако предполагается, что другие распознаватели будут использовать дополнительные идентификаторы GUID для свойств, которые не поддерживаются распознавателями Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="085d3-106">However, it is expected and encouraged that other recognizers will use additional GUIDs for properties that are not supported by the Microsoft recognizers.</span></span>

<span data-ttu-id="085d3-107">Все функции свойств были разработаны с учетом того, что список идентификаторов GUID может быть расширен другими распознавателями.</span><span class="sxs-lookup"><span data-stu-id="085d3-107">All property functions have been developed with the understanding that the list of GUIDs may be extended by other recognizers.</span></span> <span data-ttu-id="085d3-108">Эти функции свойств включают:</span><span class="sxs-lookup"><span data-stu-id="085d3-108">These property functions include:</span></span>

-   [<span data-ttu-id="085d3-109">**Функция Жетконтекстпропертилист**</span><span class="sxs-lookup"><span data-stu-id="085d3-109">**GetContextPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [<span data-ttu-id="085d3-110">**Функция Жетконтекстпропертивалуе**</span><span class="sxs-lookup"><span data-stu-id="085d3-110">**GetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [<span data-ttu-id="085d3-111">**Функция Жетресултпропертилист**</span><span class="sxs-lookup"><span data-stu-id="085d3-111">**GetResultPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [<span data-ttu-id="085d3-112">**Функция Сетконтекстпропертивалуе**</span><span class="sxs-lookup"><span data-stu-id="085d3-112">**SetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

<span data-ttu-id="085d3-113">В следующей таблице перечислены идентификаторы GUID свойств планшетных ПК, определенные в мсинкаут. h (устанавливаются в c: \\ Program Files \\ Microsoft Tablet PC Platform SDK по \\ умолчанию).</span><span class="sxs-lookup"><span data-stu-id="085d3-113">The following table lists Tablet PC property GUIDs defined in msinkaut.h (installed in c:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include by default).</span></span>



| <span data-ttu-id="085d3-114">Код GUID</span><span class="sxs-lookup"><span data-stu-id="085d3-114">GUID</span></span>                                                  | <span data-ttu-id="085d3-115">Определение</span><span class="sxs-lookup"><span data-stu-id="085d3-115">Definition</span></span>                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="085d3-116">ИНКРЕКОГНИТИОНПРОПЕРТИ \_ бокснумбер</span><span class="sxs-lookup"><span data-stu-id="085d3-116">INKRECOGNITIONPROPERTY\_BOXNUMBER</span></span><br/>          | <span data-ttu-id="085d3-117">Индекс альтернативного поля распознавателя в Box Mode</span><span class="sxs-lookup"><span data-stu-id="085d3-117">The recognizer alternate box index in box mode</span></span><br/>                                    |
| <span data-ttu-id="085d3-118">ИНКРЕКОГНИТИОНПРОПЕРТИая \_ номер_строки</span><span class="sxs-lookup"><span data-stu-id="085d3-118">INKRECOGNITIONPROPERTY\_LINENUMBER</span></span><br/>         | <span data-ttu-id="085d3-119">Номер строки</span><span class="sxs-lookup"><span data-stu-id="085d3-119">The line number</span></span><br/>                                                                   |
| <span data-ttu-id="085d3-120">\_сегментация инкрекогнитионпроперти</span><span class="sxs-lookup"><span data-stu-id="085d3-120">INKRECOGNITIONPROPERTY\_SEGMENTATION</span></span><br/>       | <span data-ttu-id="085d3-121">Как распознаватель разделяет слова и символы</span><span class="sxs-lookup"><span data-stu-id="085d3-121">How the recognizer segments words and characters</span></span><br/>                                  |
| <span data-ttu-id="085d3-122">ИНКРЕКОГНИТИОНПРОПЕРТИ \_ хотпоинт</span><span class="sxs-lookup"><span data-stu-id="085d3-122">INKRECOGNITIONPROPERTY\_HOTPOINT</span></span><br/>           | <span data-ttu-id="085d3-123">Горячая точка жеста</span><span class="sxs-lookup"><span data-stu-id="085d3-123">The gesture hot point</span></span><br/>                                                             |
| <span data-ttu-id="085d3-124">ИНКРЕКОГНИТИОНПРОПЕРТИ \_ максимумстрокекаунт</span><span class="sxs-lookup"><span data-stu-id="085d3-124">INKRECOGNITIONPROPERTY\_MAXIMUMSTROKECOUNT</span></span><br/> | <span data-ttu-id="085d3-125">Максимальное число штрихов для сегмента</span><span class="sxs-lookup"><span data-stu-id="085d3-125">Maximum number of strokes for a segment</span></span><br/>                                           |
| <span data-ttu-id="085d3-126">ИНКРЕКОГНИТИОНПРОПЕРТИ \_ поинтсперинч</span><span class="sxs-lookup"><span data-stu-id="085d3-126">INKRECOGNITIONPROPERTY\_POINTSPERINCH</span></span><br/>      | <span data-ttu-id="085d3-127">Метрика "баллы за дюйм"</span><span class="sxs-lookup"><span data-stu-id="085d3-127">The points-per-inch metric</span></span><br/>                                                        |
| <span data-ttu-id="085d3-128">ИНКРЕКОГНИТИОНПРОПЕРТИ \_ конфиденцелевел</span><span class="sxs-lookup"><span data-stu-id="085d3-128">INKRECOGNITIONPROPERTY\_CONFIDENCELEVEL</span></span><br/>    | <span data-ttu-id="085d3-129">[**Достоверность \_**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) Перечисление уровней</span><span class="sxs-lookup"><span data-stu-id="085d3-129">[**CONFIDENCE\_LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) enumeration</span></span><br/>                         |
| <span data-ttu-id="085d3-130">ИНКРЕКОГНИТИОНПРОПЕРТИ \_ линеметрикс</span><span class="sxs-lookup"><span data-stu-id="085d3-130">INKRECOGNITIONPROPERTY\_LINEMETRICS</span></span><br/>        | <span data-ttu-id="085d3-131">Сведения для вычисления базовых показателей, заполнение нажатием клавиши или и того, и другого, которые используются в Lattice</span><span class="sxs-lookup"><span data-stu-id="085d3-131">Information for computing baseline, midline, or both, that is used in the lattice</span></span><br/> |



 

 

 




