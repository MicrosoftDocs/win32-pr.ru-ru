---
title: Довнлоадманажер. Жетдовнлоадколлектион, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Жетдовнлоадколлектион извлекает указанную коллекцию загрузки.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- Жетдовнлоадколлектион метод Windows Media Player
- Жетдовнлоадколлектион метод Windows Media Player, класс Довнлоадманажер
- Класс Довнлоадманажер Windows Media Player, метод Жетдовнлоадколлектион
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694753"
---
# <a name="downloadmanagergetdownloadcollection-method"></a><span data-ttu-id="99760-108">Довнлоадманажер. Жетдовнлоадколлектион, метод</span><span class="sxs-lookup"><span data-stu-id="99760-108">DownloadManager.getDownloadCollection method</span></span>

> [!Note]  
> <span data-ttu-id="99760-109">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="99760-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="99760-110">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="99760-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="99760-111">Метод **жетдовнлоадколлектион** извлекает указанную коллекцию загрузки.</span><span class="sxs-lookup"><span data-stu-id="99760-111">The **getDownloadCollection** method retrieves the specified download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="99760-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99760-112">Syntax</span></span>


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a><span data-ttu-id="99760-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="99760-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99760-114">*CollectionID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99760-114">*collectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99760-115">**Number** (**длинное** значение), определяющее идентификатор загружаемой коллекции, которую требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="99760-115">**Number** (**long**) specifying the ID of the download collection to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99760-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99760-116">Return value</span></span>

<span data-ttu-id="99760-117">Этот метод возвращает объект **довнлоадколлектион** .</span><span class="sxs-lookup"><span data-stu-id="99760-117">This method returns a **DownloadCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="99760-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99760-118">Remarks</span></span>

<span data-ttu-id="99760-119">Сначала необходимо вызвать *довнлоадманажер*. **креатедовнлоадколлектион** , чтобы создать новую коллекцию и получить ее значение идентификатора.</span><span class="sxs-lookup"><span data-stu-id="99760-119">You must first call *DownloadManager*.**createDownloadCollection** to create a new collection and retrieve its ID value.</span></span>

<span data-ttu-id="99760-120">Существующая коллекция загрузки может содержать элементы, помеченные как отмененные.</span><span class="sxs-lookup"><span data-stu-id="99760-120">An existing download collection may contain items that have been marked as cancelled.</span></span>

<span data-ttu-id="99760-121">Элементы загрузки в режиме реального времени, которые не были завершены в предыдущем сеансе, не извлекаются в составе коллекции.</span><span class="sxs-lookup"><span data-stu-id="99760-121">Real-time download items not completed in a prior session are not retrieved as part of the collection.</span></span> <span data-ttu-id="99760-122">Фоновые загрузки, которые были выполнены до текущего сеанса, остаются в коллекции загрузки до тех пор, пока не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="99760-122">Background downloads that were completed prior to the current session remain in the download collection until removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="99760-123">Требования</span><span class="sxs-lookup"><span data-stu-id="99760-123">Requirements</span></span>



| <span data-ttu-id="99760-124">Требование</span><span class="sxs-lookup"><span data-stu-id="99760-124">Requirement</span></span> | <span data-ttu-id="99760-125">Значение</span><span class="sxs-lookup"><span data-stu-id="99760-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="99760-126">Версия</span><span class="sxs-lookup"><span data-stu-id="99760-126">Version</span></span><br/> | <span data-ttu-id="99760-127">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="99760-127">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="99760-128">DLL</span><span class="sxs-lookup"><span data-stu-id="99760-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="99760-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99760-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99760-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99760-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99760-131">**Объект Довнлоадманажер**</span><span class="sxs-lookup"><span data-stu-id="99760-131">**DownloadManager Object**</span></span>](downloadmanager-object.md)
</dt> <dt>

[<span data-ttu-id="99760-132">**Довнлоадманажер. креатедовнлоадколлектион**</span><span class="sxs-lookup"><span data-stu-id="99760-132">**DownloadManager. createDownloadCollection**</span></span>](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="99760-133">**Объект Довнлоадколлектион**</span><span class="sxs-lookup"><span data-stu-id="99760-133">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





