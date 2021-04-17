---
title: WM/Вмколлектионграупид
description: Атрибут WM/Вмколлектионграупид содержит идентификатор GUID, определяющий группу коллекции.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- Формат Windows Media WM/Вмколлектионграупид
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652007933669db4ed7977474858c7089ca0d577f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411854"
---
# <a name="wmwmcollectiongroupid"></a><span data-ttu-id="1bfa1-104">WM/Вмколлектионграупид</span><span class="sxs-lookup"><span data-stu-id="1bfa1-104">WM/WMCollectionGroupID</span></span>

<span data-ttu-id="1bfa1-105">Атрибут **WM/вмколлектионграупид** содержит идентификатор GUID, определяющий группу коллекции.</span><span class="sxs-lookup"><span data-stu-id="1bfa1-105">The **WM/WMCollectionGroupID** attribute contains a GUID identifying the collection group.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1bfa1-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="1bfa1-106">Global Constant</span></span>

<span data-ttu-id="1bfa1-107">g \_ всзвмвмколлектионграупид</span><span class="sxs-lookup"><span data-stu-id="1bfa1-107">g\_wszWMWMCollectionGroupID</span></span>

## <a name="data-type"></a><span data-ttu-id="1bfa1-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1bfa1-108">Data Type</span></span>

<span data-ttu-id="1bfa1-109">**\_GUID типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1bfa1-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="1bfa1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1bfa1-110">Remarks</span></span>

<span data-ttu-id="1bfa1-111">Содержимое идентифицируется технологиями Windows Media с использованием трех значений: **WM/вмколлектионграупид**, **WM/вмколлектионид** и **WM/вмконтентид**.</span><span class="sxs-lookup"><span data-stu-id="1bfa1-111">Content is identified by Windows Media technologies by using three values: **WM/WMCollectionGroupID**, **WM/WMCollectionID**, and **WM/WMContentID**.</span></span> <span data-ttu-id="1bfa1-112">Эти значения определяют содержимое, коллекцию, к которой он принадлежит, и группу, к которой принадлежит коллекция.</span><span class="sxs-lookup"><span data-stu-id="1bfa1-112">These values identify the content, the collection to which it belongs, and the group to which the collection belongs.</span></span> <span data-ttu-id="1bfa1-113">Все три из этих значений заполняются проигрывателем Windows Media при получении метаданных для содержимого.</span><span class="sxs-lookup"><span data-stu-id="1bfa1-113">All three of these values are populated by Windows Media Player when metadata for the content is retrieved.</span></span> <span data-ttu-id="1bfa1-114">Приложение может записать эти значения и использовать их для поиска содержимого, но не следует изменять их, если они есть.</span><span class="sxs-lookup"><span data-stu-id="1bfa1-114">You can have your application record these values and use them to identify content, but you should not change them if they are present.</span></span>

## <a name="see-also"></a><span data-ttu-id="1bfa1-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bfa1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bfa1-116">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="1bfa1-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




