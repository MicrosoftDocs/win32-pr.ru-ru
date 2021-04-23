---
description: Интерфейс Итаттрибутелист предоставляет методы для получения и установки неинтерпретируемых атрибутов.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Интерфейс Итаттрибутелист (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689347"
---
# <a name="itattributelist-interface"></a><span data-ttu-id="5c72b-103">Интерфейс Итаттрибутелист</span><span class="sxs-lookup"><span data-stu-id="5c72b-103">ITAttributeList interface</span></span>

<span data-ttu-id="5c72b-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="5c72b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5c72b-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="5c72b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5c72b-106">Интерфейс **итаттрибутелист** предоставляет методы для получения и установки неинтерпретируемых атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5c72b-106">The **ITAttributeList** interface supplies methods for getting and setting of uninterpreted attributes.</span></span> <span data-ttu-id="5c72b-107">По положению строк атрибута в пакете протокола дескрипторов сеанса (см. RFC 2327), методы предполагают, что все строки атрибутов существуют непосредственно перед тем, как были указаны атрибуты носителя, и после всех общих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5c72b-107">Regarding the position of the attribute strings in a Session Descriptor Protocol (SDP, see RFC 2327) packet, the methods assume that all attribute strings exist just before the media attributes are specified and after all the common attributes.</span></span> <span data-ttu-id="5c72b-108">Интерфейс **итаттрибутелист** создается путем вызова **QueryInterface** в [**итдиректорйобжект**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="5c72b-108">The **ITAttributeList** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="5c72b-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="5c72b-109">Members</span></span>

<span data-ttu-id="5c72b-110">Интерфейс **итаттрибутелист** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="5c72b-110">The **ITAttributeList** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5c72b-111">**Итаттрибутелист** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5c72b-111">**ITAttributeList** also has these types of members:</span></span>

-   [<span data-ttu-id="5c72b-112">Методы</span><span class="sxs-lookup"><span data-stu-id="5c72b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5c72b-113">Методы</span><span class="sxs-lookup"><span data-stu-id="5c72b-113">Methods</span></span>

<span data-ttu-id="5c72b-114">Интерфейс **итаттрибутелист** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5c72b-114">The **ITAttributeList** interface has these methods.</span></span>



| <span data-ttu-id="5c72b-115">Метод</span><span class="sxs-lookup"><span data-stu-id="5c72b-115">Method</span></span>                                                          | <span data-ttu-id="5c72b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5c72b-116">Description</span></span>                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="5c72b-117">**Включить**</span><span class="sxs-lookup"><span data-stu-id="5c72b-117">**Add**</span></span>](itattributelist-add.md)                              | <span data-ttu-id="5c72b-118">Добавляет атрибут по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="5c72b-118">Adds the attribute at the specified index.</span></span><br/>   |
| [<span data-ttu-id="5c72b-119">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="5c72b-119">**Delete**</span></span>](itattributelist-delete.md)                        | <span data-ttu-id="5c72b-120">Удаляет атрибут по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="5c72b-120">Deletes the attribute at the specified index</span></span><br/> |
| [<span data-ttu-id="5c72b-121">**получить \_ аттрибутелист**</span><span class="sxs-lookup"><span data-stu-id="5c72b-121">**get\_AttributeList**</span></span>](itattributelist-get-attributelist.md) | <span data-ttu-id="5c72b-122">Возвращает список атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5c72b-122">Gets the list of attributes.</span></span><br/>                 |
| [<span data-ttu-id="5c72b-123">**получить \_ число**</span><span class="sxs-lookup"><span data-stu-id="5c72b-123">**get\_Count**</span></span>](itattributelist-get-count.md)                 | <span data-ttu-id="5c72b-124">Возвращает количество атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5c72b-124">Gets the number of attributes.</span></span><br/>               |
| [<span data-ttu-id="5c72b-125">**получить \_ элемент**</span><span class="sxs-lookup"><span data-stu-id="5c72b-125">**get\_Item**</span></span>](itattributelist-get-item.md)                   | <span data-ttu-id="5c72b-126">Возвращает атрибут, заданный индексом.</span><span class="sxs-lookup"><span data-stu-id="5c72b-126">Gets the attribute specified by the index.</span></span><br/>   |
| [<span data-ttu-id="5c72b-127">**разместить \_ аттрибутелист**</span><span class="sxs-lookup"><span data-stu-id="5c72b-127">**put\_AttributeList**</span></span>](itattributelist-put-attributelist.md) | <span data-ttu-id="5c72b-128">Задает список атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5c72b-128">Sets the list of attributes.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="5c72b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5c72b-129">Requirements</span></span>



| <span data-ttu-id="5c72b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5c72b-130">Requirement</span></span> | <span data-ttu-id="5c72b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5c72b-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c72b-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="5c72b-132">TAPI version</span></span><br/> | <span data-ttu-id="5c72b-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5c72b-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5c72b-134">Header</span><span class="sxs-lookup"><span data-stu-id="5c72b-134">Header</span></span><br/>       | <dl> <span data-ttu-id="5c72b-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c72b-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c72b-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5c72b-136">Library</span></span><br/>      | <dl> <span data-ttu-id="5c72b-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c72b-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5c72b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5c72b-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="5c72b-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c72b-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

