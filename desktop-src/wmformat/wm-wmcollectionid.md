---
title: WM/Вмколлектионид
description: Атрибут WM/Вмколлектионид содержит идентификатор GUID, определяющий коллекцию.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- Формат Windows Media WM/Вмколлектионид
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d2ffe9ca827b19b4ce403b2e2929dea64ae684
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411855"
---
# <a name="wmwmcollectionid"></a><span data-ttu-id="b473c-104">WM/Вмколлектионид</span><span class="sxs-lookup"><span data-stu-id="b473c-104">WM/WMCollectionID</span></span>

<span data-ttu-id="b473c-105">Атрибут **WM/вмколлектионид** содержит идентификатор GUID, определяющий коллекцию.</span><span class="sxs-lookup"><span data-stu-id="b473c-105">The **WM/WMCollectionID** attribute contains a GUID identifying the collection.</span></span>

## <a name="global-constant"></a><span data-ttu-id="b473c-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="b473c-106">Global Constant</span></span>

<span data-ttu-id="b473c-107">g \_ всзвмвмколлектионид</span><span class="sxs-lookup"><span data-stu-id="b473c-107">g\_wszWMWMCollectionID</span></span>

## <a name="data-type"></a><span data-ttu-id="b473c-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b473c-108">Data Type</span></span>

<span data-ttu-id="b473c-109">**\_GUID типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="b473c-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b473c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b473c-110">Remarks</span></span>

<span data-ttu-id="b473c-111">Содержимое идентифицируется технологиями Windows Media с использованием трех значений: **WM/вмколлектионграупид**, **WM/вмколлектионид** и **WM/вмконтентид**.</span><span class="sxs-lookup"><span data-stu-id="b473c-111">Content is identified by Windows Media technologies by using three values: **WM/WMCollectionGroupID**, **WM/WMCollectionID**, and **WM/WMContentID**.</span></span> <span data-ttu-id="b473c-112">Эти значения определяют содержимое, коллекцию, к которой он принадлежит, и группу, к которой принадлежит коллекция.</span><span class="sxs-lookup"><span data-stu-id="b473c-112">These values identify the content, the collection to which it belongs, and the group to which the collection belongs.</span></span> <span data-ttu-id="b473c-113">Все три из этих значений заполняются проигрывателем Windows Media при получении метаданных для содержимого.</span><span class="sxs-lookup"><span data-stu-id="b473c-113">All three of these values are populated by Windows Media Player when metadata for the content is retrieved.</span></span> <span data-ttu-id="b473c-114">Приложение может записать эти значения и использовать их для поиска содержимого, но не следует изменять их, если они есть.</span><span class="sxs-lookup"><span data-stu-id="b473c-114">You can have your application record these values and use them to identify content, but you should not change them if they are present.</span></span>

## <a name="see-also"></a><span data-ttu-id="b473c-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b473c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b473c-116">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="b473c-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




