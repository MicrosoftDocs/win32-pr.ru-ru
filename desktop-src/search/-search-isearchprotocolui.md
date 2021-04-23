---
description: Предоставляет метод для вызова объектов Исеарчитем.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Интерфейс Исеарчпротоколуи
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701397"
---
# <a name="isearchprotocolui-interface"></a><span data-ttu-id="b6813-103">Интерфейс Исеарчпротоколуи</span><span class="sxs-lookup"><span data-stu-id="b6813-103">ISearchProtocolUI interface</span></span>

<span data-ttu-id="b6813-104">Предоставляет метод для вызова объектов [**исеарчитем**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b6813-104">Provides a method for invoking [**ISearchItem**](-search-isearchitem.md) objects.</span></span> <span data-ttu-id="b6813-105">Методы в этом интерфейсе вызываются узлом протокола при обработке URL-адресов из средства сбора данных.</span><span class="sxs-lookup"><span data-stu-id="b6813-105">Methods in this interface are called by the protocol host when processing URLs from the gatherer.</span></span> <span data-ttu-id="b6813-106">Обработчик протокола реализует протокол для доступа к источнику содержимого в собственном формате, и этот интерфейс реализует пользовательский обработчик протокола для расширения источников данных, которые могут быть проиндексированы.</span><span class="sxs-lookup"><span data-stu-id="b6813-106">The protocol handler implements the protocol for accessing a content source in its native format, and this interface implements a custom protocol handler to expand the data sources that can be indexed.</span></span>

## <a name="members"></a><span data-ttu-id="b6813-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="b6813-107">Members</span></span>

<span data-ttu-id="b6813-108">Интерфейс **исеарчпротоколуи** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b6813-108">The **ISearchProtocolUI** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b6813-109">**Исеарчпротоколуи** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b6813-109">**ISearchProtocolUI** also has these types of members:</span></span>

-   [<span data-ttu-id="b6813-110">Методы</span><span class="sxs-lookup"><span data-stu-id="b6813-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b6813-111">Методы</span><span class="sxs-lookup"><span data-stu-id="b6813-111">Methods</span></span>

<span data-ttu-id="b6813-112">Интерфейс **исеарчпротоколуи** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b6813-112">The **ISearchProtocolUI** interface has these methods.</span></span>



| <span data-ttu-id="b6813-113">Метод</span><span class="sxs-lookup"><span data-stu-id="b6813-113">Method</span></span>                                                                       | <span data-ttu-id="b6813-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b6813-114">Description</span></span>                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6813-115">**жетсеарчитемфорурл**</span><span class="sxs-lookup"><span data-stu-id="b6813-115">**GetSearchItemForUrl**</span></span>](-search-isearchprotocolui-getsearchitemforurl.md) | <span data-ttu-id="b6813-116">Возвращает элемент поиска для указанных данных.</span><span class="sxs-lookup"><span data-stu-id="b6813-116">Gets the search item for the data specified.</span></span> <span data-ttu-id="b6813-117">Этот метод вызывается один раз для каждого URL-адреса, обрабатываемого средством сбора данных, и получает указатель на объект [**исеарчитем**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b6813-117">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b6813-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6813-118">Remarks</span></span>

<span data-ttu-id="b6813-119">Интерфейс **исеарчпротоколуи** поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="b6813-119">The **ISearchProtocolUI** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="b6813-120">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс **исеарчпротоколуи** и следующие API: интерфейсы [**иитемпревиеверекст**](-search-iitempreviewerext.md), [**Иитемпропертибаг**](iitempropertybag.md) и [**исеарчитем**](-search-isearchitem.md) , структура [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="b6813-120">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchProtocolUI** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6813-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b6813-121">Requirements</span></span>



| <span data-ttu-id="b6813-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b6813-122">Requirement</span></span> | <span data-ttu-id="b6813-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b6813-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6813-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6813-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6813-125">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6813-125">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b6813-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6813-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6813-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6813-127">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b6813-128">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b6813-128">Redistributable</span></span><br/>          | <span data-ttu-id="b6813-129">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="b6813-129">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
