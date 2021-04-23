---
description: Интерфейс Икспин предоставляет метод для получения средних, поддерживаемых ПИН-кодом в фильтре режима ядра. Икспин содержит дополнительные методы, Кроме показанных здесь, но они не поддерживаются для DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Интерфейс Икспин (Кспрокси. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673022"
---
# <a name="ikspin-interface"></a><span data-ttu-id="95081-104">Интерфейс Икспин</span><span class="sxs-lookup"><span data-stu-id="95081-104">IKsPin interface</span></span>

<span data-ttu-id="95081-105">`IKsPin`Интерфейс предоставляет метод для получения средних, поддерживаемых ПИН-кодом в фильтре режима ядра.</span><span class="sxs-lookup"><span data-stu-id="95081-105">The `IKsPin` interface provides a method to retrieve the mediums supported by a pin on a kernel-mode filter.</span></span> <span data-ttu-id="95081-106">`IKsPin` содержит дополнительные методы, Помимо показанных здесь, но они не поддерживаются для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="95081-106">`IKsPin` has additional methods besides the one shown here, but they are not supported for DirectShow.</span></span>

## <a name="members"></a><span data-ttu-id="95081-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="95081-107">Members</span></span>

<span data-ttu-id="95081-108">Интерфейс **икспин** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="95081-108">The **IKsPin** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="95081-109">**Икспин** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="95081-109">**IKsPin** also has these types of members:</span></span>

-   [<span data-ttu-id="95081-110">Методы</span><span class="sxs-lookup"><span data-stu-id="95081-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="95081-111">Методы</span><span class="sxs-lookup"><span data-stu-id="95081-111">Methods</span></span>

<span data-ttu-id="95081-112">Интерфейс **икспин** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="95081-112">The **IKsPin** interface has these methods.</span></span>



| <span data-ttu-id="95081-113">Метод</span><span class="sxs-lookup"><span data-stu-id="95081-113">Method</span></span>                                          | <span data-ttu-id="95081-114">Описание</span><span class="sxs-lookup"><span data-stu-id="95081-114">Description</span></span>                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="95081-115">**кскуеримедиумс**</span><span class="sxs-lookup"><span data-stu-id="95081-115">**KsQueryMediums**</span></span>](ikspin-ksquerymediums.md) | <span data-ttu-id="95081-116">Извлекает средние, поддерживаемые ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="95081-116">Retrieves the mediums supported by a pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95081-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95081-117">Remarks</span></span>

<span data-ttu-id="95081-118">Перед Кспрокси. h необходимо включить KS. h.</span><span class="sxs-lookup"><span data-stu-id="95081-118">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="95081-119">Требования</span><span class="sxs-lookup"><span data-stu-id="95081-119">Requirements</span></span>



| <span data-ttu-id="95081-120">Требование</span><span class="sxs-lookup"><span data-stu-id="95081-120">Requirement</span></span> | <span data-ttu-id="95081-121">Значение</span><span class="sxs-lookup"><span data-stu-id="95081-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95081-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95081-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95081-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="95081-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="95081-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95081-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95081-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="95081-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95081-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="95081-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="95081-127"><dt>Кспрокси. h</dt></span><span class="sxs-lookup"><span data-stu-id="95081-127"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="95081-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95081-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="95081-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95081-129"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
