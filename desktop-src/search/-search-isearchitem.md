---
description: Предоставляет методы, определяющие взаимодействие между пользовательским интерфейсом и объектами пространства имен поиска, созданными индексатором.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Интерфейс Исеарчитем
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423730"
---
# <a name="isearchitem-interface"></a><span data-ttu-id="c137a-103">Интерфейс Исеарчитем</span><span class="sxs-lookup"><span data-stu-id="c137a-103">ISearchItem interface</span></span>

<span data-ttu-id="c137a-104">Предоставляет методы, определяющие взаимодействие между пользовательским интерфейсом и объектами пространства имен поиска, созданными индексатором.</span><span class="sxs-lookup"><span data-stu-id="c137a-104">Provides methods that define interaction between a user interface (UI) and the Search namespace objects created by the indexer.</span></span>

## <a name="members"></a><span data-ttu-id="c137a-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="c137a-105">Members</span></span>

<span data-ttu-id="c137a-106">Интерфейс **исеарчитем** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c137a-106">The **ISearchItem** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c137a-107">**Исеарчитем** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c137a-107">**ISearchItem** also has these types of members:</span></span>

-   [<span data-ttu-id="c137a-108">Методы</span><span class="sxs-lookup"><span data-stu-id="c137a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c137a-109">Методы</span><span class="sxs-lookup"><span data-stu-id="c137a-109">Methods</span></span>

<span data-ttu-id="c137a-110">Интерфейс **исеарчитем** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c137a-110">The **ISearchItem** interface has these methods.</span></span>



| <span data-ttu-id="c137a-111">Метод</span><span class="sxs-lookup"><span data-stu-id="c137a-111">Method</span></span>                                                         | <span data-ttu-id="c137a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c137a-112">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c137a-113">**жетпарентфолдер**</span><span class="sxs-lookup"><span data-stu-id="c137a-113">**GetParentFolder**</span></span>](-search-isearchitem-getparentfolder.md) | <span data-ttu-id="c137a-114">Возвращает объект **исеарчитем** , если URL-адрес представляет фактический источник данных оболочки (также известный как расширение пространства имен оболочки).</span><span class="sxs-lookup"><span data-stu-id="c137a-114">Gets the **ISearchItem** object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span><br/> |
| <span data-ttu-id="c137a-115">[**жетуиобжектоф**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c137a-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span></span>     | <span data-ttu-id="c137a-116">Возвращает объект пользовательского интерфейса **исеарчитем**.</span><span class="sxs-lookup"><span data-stu-id="c137a-116">Gets the user interface (UI) object of **ISearchItem**.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="c137a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c137a-117">Remarks</span></span>

<span data-ttu-id="c137a-118">[**Исеарчитем:: жетпарентфолдер**](-search-isearchitem-getparentfolder.md) поддерживается только в Windows XP и windows Server 2003 и больше не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="c137a-118">The [**ISearchItem::GetParentFolder**](-search-isearchitem-getparentfolder.md) is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="c137a-119">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс **исеарчитем** и следующие API: интерфейсы [**иитемпревиеверекст**](-search-iitempreviewerext.md), [**Иитемпропертибаг**](iitempropertybag.md)и [**исеарчпротоколуи**](-search-isearchprotocolui.md) , структура [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="c137a-119">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchItem** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="c137a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c137a-120">Requirements</span></span>



| <span data-ttu-id="c137a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c137a-121">Requirement</span></span> | <span data-ttu-id="c137a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c137a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c137a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c137a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c137a-124">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c137a-124">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c137a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c137a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c137a-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c137a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c137a-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c137a-127">Redistributable</span></span><br/>          | <span data-ttu-id="c137a-128">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="c137a-128">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
