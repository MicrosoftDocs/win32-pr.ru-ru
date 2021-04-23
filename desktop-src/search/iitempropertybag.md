---
description: Определяет методы для получения сведений о свойствах элемента поиска. Этот интерфейс поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Интерфейс Иитемпропертибаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144032"
---
# <a name="iitempropertybag-interface"></a><span data-ttu-id="aaf54-104">Интерфейс Иитемпропертибаг</span><span class="sxs-lookup"><span data-stu-id="aaf54-104">IItemPropertyBag interface</span></span>

<span data-ttu-id="aaf54-105">Определяет методы для получения сведений о свойствах элемента поиска.</span><span class="sxs-lookup"><span data-stu-id="aaf54-105">Defines methods to obtain information about the properties of a search item.</span></span> <span data-ttu-id="aaf54-106">Этот интерфейс поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="aaf54-106">This interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="aaf54-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="aaf54-107">Members</span></span>

<span data-ttu-id="aaf54-108">Интерфейс **иитемпропертибаг** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aaf54-108">The **IItemPropertyBag** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aaf54-109">**Иитемпропертибаг** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="aaf54-109">**IItemPropertyBag** also has these types of members:</span></span>

-   [<span data-ttu-id="aaf54-110">Методы</span><span class="sxs-lookup"><span data-stu-id="aaf54-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aaf54-111">Методы</span><span class="sxs-lookup"><span data-stu-id="aaf54-111">Methods</span></span>

<span data-ttu-id="aaf54-112">Интерфейс **иитемпропертибаг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="aaf54-112">The **IItemPropertyBag** interface has these methods.</span></span>



| <span data-ttu-id="aaf54-113">Метод</span><span class="sxs-lookup"><span data-stu-id="aaf54-113">Method</span></span>                                                      | <span data-ttu-id="aaf54-114">Описание</span><span class="sxs-lookup"><span data-stu-id="aaf54-114">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf54-115">[**каунтпропертиес**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aaf54-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span></span> | <span data-ttu-id="aaf54-116">Возвращает количество свойств в контейнере свойств.</span><span class="sxs-lookup"><span data-stu-id="aaf54-116">Gets a count of the number of properties in the property bag.</span></span><br/>                     |
| [<span data-ttu-id="aaf54-117">**GetPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="aaf54-117">**GetPropertyInfo**</span></span>](iitempropertybag-getpropertyinfo.md) | <span data-ttu-id="aaf54-118">Возвращает сведения, необходимые для чтения или сохранения свойств в контейнере свойств.</span><span class="sxs-lookup"><span data-stu-id="aaf54-118">Gets the information required to read or save the properties in the property bag.</span></span><br/> |
| [<span data-ttu-id="aaf54-119">**Просмотр**</span><span class="sxs-lookup"><span data-stu-id="aaf54-119">**Read**</span></span>](iitempropertybag-read.md)                       | <span data-ttu-id="aaf54-120">Вызывает считывание одного или нескольких свойств из контейнера свойств.</span><span class="sxs-lookup"><span data-stu-id="aaf54-120">Causes one or more properties to be read from the property bag.</span></span><br/>                   |
| [<span data-ttu-id="aaf54-121">**Будет**</span><span class="sxs-lookup"><span data-stu-id="aaf54-121">**Write**</span></span>](iitempropertybag-write.md)                     | <span data-ttu-id="aaf54-122">Вызывает сохранение одного или нескольких свойств в контейнере свойств.</span><span class="sxs-lookup"><span data-stu-id="aaf54-122">Causes one or more properties to be saved into the property bag.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="aaf54-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aaf54-123">Remarks</span></span>

<span data-ttu-id="aaf54-124">Интерфейс **иитемпропертибаг** поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="aaf54-124">The **IItemPropertyBag** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="aaf54-125">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс **иитемпропертибаг** и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпревиеверекст**](-search-iitempreviewerext.md) и [**исеарчитем**](-search-isearchitem.md) , структуры [**линкинфо**](-search-linkinfo.md) и [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="aaf54-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPropertyBag** interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaf54-126">Требования</span><span class="sxs-lookup"><span data-stu-id="aaf54-126">Requirements</span></span>



| <span data-ttu-id="aaf54-127">Требование</span><span class="sxs-lookup"><span data-stu-id="aaf54-127">Requirement</span></span> | <span data-ttu-id="aaf54-128">Значение</span><span class="sxs-lookup"><span data-stu-id="aaf54-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aaf54-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aaf54-129">Minimum supported client</span></span><br/> | <span data-ttu-id="aaf54-130">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="aaf54-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="aaf54-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aaf54-131">Minimum supported server</span></span><br/> | <span data-ttu-id="aaf54-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aaf54-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="aaf54-133">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="aaf54-133">Redistributable</span></span><br/>          | <span data-ttu-id="aaf54-134">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="aaf54-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
