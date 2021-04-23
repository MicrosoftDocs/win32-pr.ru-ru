---
description: Предоставляет методы для предоставления параметров браузера. Интерфейс Иитемпревиеверекст поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Интерфейс Иитемпревиеверекст
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990969"
---
# <a name="iitempreviewerext-interface"></a><span data-ttu-id="0a664-104">Интерфейс Иитемпревиеверекст</span><span class="sxs-lookup"><span data-stu-id="0a664-104">IItemPreviewerExt interface</span></span>

<span data-ttu-id="0a664-105">Предоставляет методы для предоставления параметров браузера.</span><span class="sxs-lookup"><span data-stu-id="0a664-105">Provides methods for supplying browser settings.</span></span> <span data-ttu-id="0a664-106">Интерфейс **иитемпревиеверекст** поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="0a664-106">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="0a664-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="0a664-107">Members</span></span>

<span data-ttu-id="0a664-108">Интерфейс **иитемпревиеверекст** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0a664-108">The **IItemPreviewerExt** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0a664-109">**Иитемпревиеверекст** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0a664-109">**IItemPreviewerExt** also has these types of members:</span></span>

-   [<span data-ttu-id="0a664-110">Методы</span><span class="sxs-lookup"><span data-stu-id="0a664-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0a664-111">Методы</span><span class="sxs-lookup"><span data-stu-id="0a664-111">Methods</span></span>

<span data-ttu-id="0a664-112">Интерфейс **иитемпревиеверекст** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0a664-112">The **IItemPreviewerExt** interface has these methods.</span></span>



| <span data-ttu-id="0a664-113">Метод</span><span class="sxs-lookup"><span data-stu-id="0a664-113">Method</span></span>                                                                               | <span data-ttu-id="0a664-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0a664-114">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a664-115">**жетлинкедконтент**</span><span class="sxs-lookup"><span data-stu-id="0a664-115">**GetLinkedContent**</span></span>](-search-iitempreviewerext-getlinkedcontent.md)               | <span data-ttu-id="0a664-116">Допускает расширение к расширенному содержимому для свойства.</span><span class="sxs-lookup"><span data-stu-id="0a664-116">Permits the extension to rich content for a property.</span></span> <br/>                            |
| [<span data-ttu-id="0a664-117">**жетрелатедпарт**</span><span class="sxs-lookup"><span data-stu-id="0a664-117">**GetRelatedPart**</span></span>](-search-iitempreviewerext-getrelatedpart.md)                   | <span data-ttu-id="0a664-118">Возвращает связанную часть тела для внедрения в выходной поток MHTML.</span><span class="sxs-lookup"><span data-stu-id="0a664-118">Gets a related body part for embedding into the output MHTML stream.</span></span><br/>              |
| [<span data-ttu-id="0a664-119">**процесстрансформкомманд**</span><span class="sxs-lookup"><span data-stu-id="0a664-119">**ProcessTransformCommand**</span></span>](-search-iitempreviewerext-processtransformcommand.md) | <span data-ttu-id="0a664-120">Разрешает обработку команды преобразования, обнаруженной в шаблоне предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="0a664-120">Permits processing of a transformation command encountered in a preview template.</span></span><br/> |
| [<span data-ttu-id="0a664-121">**сугжестбровсерполици**</span><span class="sxs-lookup"><span data-stu-id="0a664-121">**SuggestBrowserPolicy**</span></span>](-search-iitempreviewerext-suggestbrowserpolicy.md)       | <span data-ttu-id="0a664-122">Предлагает политику безопасности, применяемую к браузеру.</span><span class="sxs-lookup"><span data-stu-id="0a664-122">Suggests the security policy to be applied to the browser.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="0a664-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a664-123">Remarks</span></span>

<span data-ttu-id="0a664-124">Интерфейс **иитемпревиеверекст** поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="0a664-124">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="0a664-125">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс **иитемпревиеверекст** и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпропертибаг**](iitempropertybag.md) и [**исеарчитем**](-search-isearchitem.md) , структура [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="0a664-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPreviewerExt** interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a664-126">Требования</span><span class="sxs-lookup"><span data-stu-id="0a664-126">Requirements</span></span>



| <span data-ttu-id="0a664-127">Требование</span><span class="sxs-lookup"><span data-stu-id="0a664-127">Requirement</span></span> | <span data-ttu-id="0a664-128">Значение</span><span class="sxs-lookup"><span data-stu-id="0a664-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a664-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a664-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0a664-130">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a664-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0a664-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a664-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0a664-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a664-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0a664-133">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0a664-133">Redistributable</span></span><br/>          | <span data-ttu-id="0a664-134">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="0a664-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
