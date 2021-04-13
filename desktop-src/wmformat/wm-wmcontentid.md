---
title: WM/Вмконтентид
description: Атрибут WM/Вмконтентид содержит идентификатор GUID, определяющий содержимое.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Формат Windows Media WM/Вмконтентид
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411853"
---
# <a name="wmwmcontentid"></a><span data-ttu-id="494bd-104">WM/Вмконтентид</span><span class="sxs-lookup"><span data-stu-id="494bd-104">WM/WMContentID</span></span>

<span data-ttu-id="494bd-105">Атрибут **WM/вмконтентид** содержит идентификатор GUID, определяющий содержимое.</span><span class="sxs-lookup"><span data-stu-id="494bd-105">The **WM/WMContentID** attribute contains a GUID identifying the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="494bd-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="494bd-106">Global Constant</span></span>

<span data-ttu-id="494bd-107">g \_ всзвмвмконтентид</span><span class="sxs-lookup"><span data-stu-id="494bd-107">g\_wszWMWMContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="494bd-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="494bd-108">Data Type</span></span>

<span data-ttu-id="494bd-109">**\_GUID типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="494bd-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="494bd-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="494bd-110">Remarks</span></span>

<span data-ttu-id="494bd-111">Содержимое идентифицируется технологиями Windows Media с использованием трех значений: **WM/вмколлектионграупид**, **WM/вмколлектионид** и **WM/вмконтентид**.</span><span class="sxs-lookup"><span data-stu-id="494bd-111">Content is identified by Windows Media technologies by using three values: **WM/WMCollectionGroupID**, **WM/WMCollectionID**, and **WM/WMContentID**.</span></span> <span data-ttu-id="494bd-112">Эти значения определяют содержимое, коллекцию, к которой он принадлежит, и группу, к которой принадлежит коллекция.</span><span class="sxs-lookup"><span data-stu-id="494bd-112">These values identify the content, the collection to which it belongs, and the group to which the collection belongs.</span></span> <span data-ttu-id="494bd-113">Все три из этих значений заполняются проигрывателем Windows Media при получении метаданных для содержимого.</span><span class="sxs-lookup"><span data-stu-id="494bd-113">All three of these values are populated by Windows Media Player when metadata for the content is retrieved.</span></span> <span data-ttu-id="494bd-114">Приложение может записать эти значения и использовать их для поиска содержимого, но не следует изменять их, если они есть.</span><span class="sxs-lookup"><span data-stu-id="494bd-114">You can have your application record these values and use them to identify content, but you should not change them if they are present.</span></span>

## <a name="see-also"></a><span data-ttu-id="494bd-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="494bd-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="494bd-116">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="494bd-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




