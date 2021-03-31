---
title: Функции сборщика событий Windows
description: В следующем списке кратко описаны функции, которые используются в сборщике событий Windows.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328299"
---
# <a name="windows-event-collector-functions"></a><span data-ttu-id="91f67-103">Функции сборщика событий Windows</span><span class="sxs-lookup"><span data-stu-id="91f67-103">Windows Event Collector Functions</span></span>

<span data-ttu-id="91f67-104">В следующем списке кратко описаны функции, которые используются в сборщике событий Windows.</span><span class="sxs-lookup"><span data-stu-id="91f67-104">The following list briefly describes the functions that are used in Windows Event Collector.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="91f67-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="91f67-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="91f67-106">**екклосе**</span><span class="sxs-lookup"><span data-stu-id="91f67-106">**EcClose**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

<span data-ttu-id="91f67-107">Закрывает маркер, полученный от других функций сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="91f67-107">Closes a handle received from other Event Collector functions.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-108">**екделетесубскриптион**</span><span class="sxs-lookup"><span data-stu-id="91f67-108">**EcDeleteSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

<span data-ttu-id="91f67-109">Удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="91f67-109">Deletes an existing subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-110">**еценумнекстсубскриптион**</span><span class="sxs-lookup"><span data-stu-id="91f67-110">**EcEnumNextSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

<span data-ttu-id="91f67-111">Возобновляет перечисление подписок, зарегистрированных на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="91f67-111">Continues the enumeration of the subscriptions registered on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-112">**екжетобжектаррайпроперти**</span><span class="sxs-lookup"><span data-stu-id="91f67-112">**EcGetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="91f67-113">Извлекает значения свойств для источников событий подписки.</span><span class="sxs-lookup"><span data-stu-id="91f67-113">Retrieves property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-114">**екжетобжектаррайсизе**</span><span class="sxs-lookup"><span data-stu-id="91f67-114">**EcGetObjectArraySize**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

<span data-ttu-id="91f67-115">Возвращает количество индексов массива значений свойств для источников событий подписки.</span><span class="sxs-lookup"><span data-stu-id="91f67-115">Retrieves the number of indexes of the array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-116">**екжетсубскриптионпроперти**</span><span class="sxs-lookup"><span data-stu-id="91f67-116">**EcGetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="91f67-117">Извлекает значение свойства из объекта подписки.</span><span class="sxs-lookup"><span data-stu-id="91f67-117">Retrieves a property value from a subscription object.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-118">**екжетсубскриптионрунтиместатус**</span><span class="sxs-lookup"><span data-stu-id="91f67-118">**EcGetSubscriptionRunTimeStatus**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

<span data-ttu-id="91f67-119">Извлекает сведения о состоянии времени выполнения для источника события подписки или самой подписки.</span><span class="sxs-lookup"><span data-stu-id="91f67-119">Retrieves the run time status information for an event source of a subscription or the subscription itself.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-120">**еЦинсертобжектаррайелемент**</span><span class="sxs-lookup"><span data-stu-id="91f67-120">**EcInsertObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

<span data-ttu-id="91f67-121">Вставляет пустой объект в массив значений свойств для источников событий подписки.</span><span class="sxs-lookup"><span data-stu-id="91f67-121">Inserts an empty object into an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-122">**екопенсубскриптионенум**</span><span class="sxs-lookup"><span data-stu-id="91f67-122">**EcOpenSubscriptionEnum**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

<span data-ttu-id="91f67-123">Создает перечислитель подписки для перечисления всех зарегистрированных подписок на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="91f67-123">Creates a subscription enumerator to enumerate all registered subscriptions on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-124">**екопенсубскриптион**</span><span class="sxs-lookup"><span data-stu-id="91f67-124">**EcOpenSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

<span data-ttu-id="91f67-125">Открывает существующую подписку или создает новую.</span><span class="sxs-lookup"><span data-stu-id="91f67-125">Opens an existing subscription or creates a new subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-126">**ексавесубскриптион**</span><span class="sxs-lookup"><span data-stu-id="91f67-126">**EcSaveSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

<span data-ttu-id="91f67-127">Сохраняет сведения о конфигурации подписки.</span><span class="sxs-lookup"><span data-stu-id="91f67-127">Saves subscription configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-128">**ексетобжектаррайпроперти**</span><span class="sxs-lookup"><span data-stu-id="91f67-128">**EcSetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="91f67-129">Задает значение свойства в массиве значений свойств для источников событий подписки.</span><span class="sxs-lookup"><span data-stu-id="91f67-129">Sets a property value in an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-130">**ексетсубскриптионпроперти**</span><span class="sxs-lookup"><span data-stu-id="91f67-130">**EcSetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="91f67-131">Устанавливает новые значения или обновляет существующие значения подписки.</span><span class="sxs-lookup"><span data-stu-id="91f67-131">Sets new values or updates existing values of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-132">**екремовеобжектаррайелемент**</span><span class="sxs-lookup"><span data-stu-id="91f67-132">**EcRemoveObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

<span data-ttu-id="91f67-133">Удаляет элемент из массива объектов, который содержит значения свойств для источников событий подписки.</span><span class="sxs-lookup"><span data-stu-id="91f67-133">Removes an element from an array of objects that contain property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="91f67-134">**екретрисубскриптион**</span><span class="sxs-lookup"><span data-stu-id="91f67-134">**EcRetrySubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

<span data-ttu-id="91f67-135">Повторяет попытку подключения к источнику событий подписки, которая не подключена.</span><span class="sxs-lookup"><span data-stu-id="91f67-135">Retries connecting to the event source of a subscription that is not connected.</span></span>

</dd> </dl>

 

 




