---
title: Элемент Довнлоадстатус (Мсфидс. h)
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | Элемент Довнлоадстатус (Мсфидс. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Проигрыватель Windows Media, элемент Довнлоадстатус
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695162"
---
# <a name="downloadstatus-element"></a><span data-ttu-id="b858d-105">Довнлоадстатус, элемент</span><span class="sxs-lookup"><span data-stu-id="b858d-105">DownloadStatus Element</span></span>

> [!Note]  
> <span data-ttu-id="b858d-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="b858d-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b858d-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b858d-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b858d-108">Элемент **довнлоадстатус** указывает URL-адрес, который проигрыватель Windows Media отображает как ссылку, чтобы разрешить пользователям просматривать состояние скачивания.</span><span class="sxs-lookup"><span data-stu-id="b858d-108">The **DownloadStatus** element specifies a URL the Windows Media Player displays as a link to enable users to view download status.</span></span>

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="b858d-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b858d-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="b858d-110"><span id="URL"></span><span id="url"></span>URL-адрес</span><span class="sxs-lookup"><span data-stu-id="b858d-110"><span id="URL"></span><span id="url"></span>URL</span></span>
</dt> <dd>

<span data-ttu-id="b858d-111">URL-адрес веб-страницы, отображаемой Интернет-магазином для отображения состояния скачивания пользователю.</span><span class="sxs-lookup"><span data-stu-id="b858d-111">URL for the webpage that the online store displays to show download status to the user.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="b858d-112">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b858d-112">Parent/Child Elements</span></span>



| <span data-ttu-id="b858d-113">Иерархия</span><span class="sxs-lookup"><span data-stu-id="b858d-113">Hierarchy</span></span>       | <span data-ttu-id="b858d-114">Элемент</span><span class="sxs-lookup"><span data-stu-id="b858d-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="b858d-115">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b858d-115">Parent elements</span></span> | <span data-ttu-id="b858d-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b858d-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="b858d-117">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b858d-117">Child elements</span></span>  | <span data-ttu-id="b858d-118">Нет</span><span class="sxs-lookup"><span data-stu-id="b858d-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="b858d-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="b858d-119">Remarks</span></span>

<span data-ttu-id="b858d-120">Проигрыватель Windows Media отображает сообщение для пользователей, когда выполняется скачивание.</span><span class="sxs-lookup"><span data-stu-id="b858d-120">Windows Media Player displays a message to users when a download is in progress.</span></span> <span data-ttu-id="b858d-121">Если текущие активные службы определяют URL-адрес состояния загрузки, пользователь может щелкнуть текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="b858d-121">If the current active services defines a download status URL, the user can click the message text.</span></span> <span data-ttu-id="b858d-122">Когда пользователь щелкает сообщение, проигрыватель переходит по URL-адресу, указанному в элементе **довнлоадстатус** , чтобы текущий активный магазин мог предоставить сведения о выполняемых скачиваниях.</span><span class="sxs-lookup"><span data-stu-id="b858d-122">When the user clicks the message, the Player navigates to the URL specified by the **DownloadStatus** element so the current active store can provide details about downloads in progress.</span></span>

## <a name="requirements"></a><span data-ttu-id="b858d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b858d-123">Requirements</span></span>



| <span data-ttu-id="b858d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b858d-124">Requirement</span></span> | <span data-ttu-id="b858d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b858d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b858d-126">Версия</span><span class="sxs-lookup"><span data-stu-id="b858d-126">Version</span></span><br/> | <span data-ttu-id="b858d-127">Проигрыватель Windows Media 10 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b858d-127">Windows Media Player 10 or later</span></span><br/>                                          |
| <span data-ttu-id="b858d-128">Header</span><span class="sxs-lookup"><span data-stu-id="b858d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b858d-129"><dt>Мсфидс. h</dt></span><span class="sxs-lookup"><span data-stu-id="b858d-129"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b858d-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b858d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b858d-131">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="b858d-131">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="b858d-132">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="b858d-132">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="b858d-133">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b858d-133">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





