---
title: Типы данных сборщика событий Windows (Евколл. h)
description: Типы данных для сборщика событий Windows используются как типы переменных объектов подписки на события, типы параметров функций и типы возвращаемых функций.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691759"
---
# <a name="windows-event-collector-data-types"></a><span data-ttu-id="c112d-105">Типы данных сборщика событий Windows</span><span class="sxs-lookup"><span data-stu-id="c112d-105">Windows Event Collector Data Types</span></span>

<span data-ttu-id="c112d-106">Типы данных для сборщика событий Windows используются как типы переменных объектов подписки на события, типы параметров функций и типы возвращаемых функций.</span><span class="sxs-lookup"><span data-stu-id="c112d-106">The data types for the Windows Event Collector are used as event subscription object variable types, function parameter types, and function return types.</span></span>


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="c112d-107">**\_маркер EC**</span><span class="sxs-lookup"><span data-stu-id="c112d-107">**EC\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="c112d-108">Обработчик для объекта подписки.</span><span class="sxs-lookup"><span data-stu-id="c112d-108">Handle to a subscription object.</span></span> <span data-ttu-id="c112d-109">Используется для представления подписки сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="c112d-109">Used to represent an event collector subscription.</span></span>

</dd> <dt>

<span data-ttu-id="c112d-110">**\_ \_ \_ маркер свойства массива объектов \_ EC**</span><span class="sxs-lookup"><span data-stu-id="c112d-110">**EC\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="c112d-111">Обработайте массив значений свойств для источников событий подписки.</span><span class="sxs-lookup"><span data-stu-id="c112d-111">Handle to an array of property values for the event sources of a subscription.</span></span> <span data-ttu-id="c112d-112">Этот маркер массива возвращается методом [**екжетсубскриптионпроперти**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) , когда значение **ексубскриптионевентсаурцес** передается в параметр *PropertyId* .</span><span class="sxs-lookup"><span data-stu-id="c112d-112">The array handle is returned by the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) method when the **EcSubscriptionEventSources** value is passed into the *PropertyId* parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c112d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c112d-113">Requirements</span></span>



| <span data-ttu-id="c112d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c112d-114">Requirement</span></span> | <span data-ttu-id="c112d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c112d-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c112d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c112d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c112d-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c112d-117">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="c112d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c112d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c112d-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c112d-119">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="c112d-120">Header</span><span class="sxs-lookup"><span data-stu-id="c112d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c112d-121"><dt>Евколл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c112d-121"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





