---
description: Отслеживает дочерние запросы, созданные из родительского запроса.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Интерфейс Ивбемкаусалитякцесс (Вбеминт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: db4c7a76b04b659cd467f7a4a7a9a8c1ba42721f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647525"
---
# <a name="iwbemcausalityaccess-interface"></a><span data-ttu-id="96915-103">Интерфейс Ивбемкаусалитякцесс</span><span class="sxs-lookup"><span data-stu-id="96915-103">IWbemCausalityAccess interface</span></span>

<span data-ttu-id="96915-104">Интерфейс **ивбемкаусалитякцесс** отслеживает дочерние запросы, созданные из родительского запроса.</span><span class="sxs-lookup"><span data-stu-id="96915-104">The **IWbemCausalityAccess** interface keeps track of child requests that are generated from a parent request.</span></span> <span data-ttu-id="96915-105">Объект **ивбемкаусалитякцесс** можно получить с помощью интерфейса запроса (QI) для [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span><span class="sxs-lookup"><span data-stu-id="96915-105">You can obtain an **IWbemCausalityAccess** object by using a query interface (QI) for [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span></span> <span data-ttu-id="96915-106">Каждый запрос определяется глобальным уникальным идентификатором (GUID) и может иметь родительский запрос или может быть запросом Top.</span><span class="sxs-lookup"><span data-stu-id="96915-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="96915-107">GUID — это уникальное 128-разрядное число.</span><span class="sxs-lookup"><span data-stu-id="96915-107">A GUID is a unique 128-bit number.</span></span> <span data-ttu-id="96915-108">Например, 5b2fc63a-8AF4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="96915-108">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

## <a name="members"></a><span data-ttu-id="96915-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="96915-109">Members</span></span>

<span data-ttu-id="96915-110">Интерфейс **ивбемкаусалитякцесс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="96915-110">The **IWbemCausalityAccess** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="96915-111">**Ивбемкаусалитякцесс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="96915-111">**IWbemCausalityAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="96915-112">Методы</span><span class="sxs-lookup"><span data-stu-id="96915-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="96915-113">Методы</span><span class="sxs-lookup"><span data-stu-id="96915-113">Methods</span></span>

<span data-ttu-id="96915-114">Интерфейс **ивбемкаусалитякцесс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="96915-114">The **IWbemCausalityAccess** interface has these methods.</span></span>



| <span data-ttu-id="96915-115">Метод</span><span class="sxs-lookup"><span data-stu-id="96915-115">Method</span></span>                                                    | <span data-ttu-id="96915-116">Описание</span><span class="sxs-lookup"><span data-stu-id="96915-116">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96915-117">**жетрекуестид**</span><span class="sxs-lookup"><span data-stu-id="96915-117">**GetRequestId**</span></span>](iwbemcausalityaccess-getrequestid.md) | <span data-ttu-id="96915-118">Возвращает уникальный идентификатор GUID для запроса.</span><span class="sxs-lookup"><span data-stu-id="96915-118">Returns a unique GUID identifier for a request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="96915-119">**исчилдоф**</span><span class="sxs-lookup"><span data-stu-id="96915-119">**IsChildOf**</span></span>](iwbemcausalityaccess-ischildof.md)       | <span data-ttu-id="96915-120">Определяет, является ли запрос дочерним по отношению к указанному родительскому запросу.</span><span class="sxs-lookup"><span data-stu-id="96915-120">Determines if a request is a child of a specified parent request.</span></span> <span data-ttu-id="96915-121">Родительский запрос может иметь несколько дочерних запросов, каждый из которых определяется уникальным значением идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="96915-121">A parent request can have multiple child requests, each identified by a unique GUID value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="96915-122">Требования</span><span class="sxs-lookup"><span data-stu-id="96915-122">Requirements</span></span>



| <span data-ttu-id="96915-123">Требование</span><span class="sxs-lookup"><span data-stu-id="96915-123">Requirement</span></span> | <span data-ttu-id="96915-124">Значение</span><span class="sxs-lookup"><span data-stu-id="96915-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96915-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96915-125">Minimum supported client</span></span><br/> | <span data-ttu-id="96915-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96915-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96915-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96915-127">Minimum supported server</span></span><br/> | <span data-ttu-id="96915-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96915-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96915-129">Header</span><span class="sxs-lookup"><span data-stu-id="96915-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="96915-130"><dt>Вбеминт. h</dt></span><span class="sxs-lookup"><span data-stu-id="96915-130"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="96915-131">DLL</span><span class="sxs-lookup"><span data-stu-id="96915-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96915-132"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96915-132"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96915-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96915-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96915-134">COM API для WMI</span><span class="sxs-lookup"><span data-stu-id="96915-134">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

