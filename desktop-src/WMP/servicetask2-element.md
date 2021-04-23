---
title: ServiceTask2, элемент
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Элемент ServiceTask2 представляет вторую область задач оперативного хранилища.
ms.assetid: f920ef25-efca-47c8-bcbc-2cb34593e879
keywords:
- Проигрыватель Windows Media, элемент ServiceTask2
topic_type:
- apiref
api_name:
- ServiceTask2 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36052dabc1be7f2925f5185239faa602b8633fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649086"
---
# <a name="servicetask2-element"></a><span data-ttu-id="f9364-106">ServiceTask2, элемент</span><span class="sxs-lookup"><span data-stu-id="f9364-106">ServiceTask2 Element</span></span>

> [!Note]  
> <span data-ttu-id="f9364-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="f9364-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f9364-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f9364-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f9364-109">Элемент **ServiceTask2** представляет вторую область задач оперативного хранилища.</span><span class="sxs-lookup"><span data-stu-id="f9364-109">The **ServiceTask2** element represents the second online store task pane.</span></span>

``` syntax
<ServiceTask2
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="f9364-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f9364-110">Attributes</span></span>



| <span data-ttu-id="f9364-111">Термин</span><span class="sxs-lookup"><span data-stu-id="f9364-111">Term</span></span>                                                                                                                             | <span data-ttu-id="f9364-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f9364-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="f9364-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL-адрес** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="f9364-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="f9364-114">URL-адрес веб-страницы, отображаемой проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9364-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="f9364-115">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f9364-115">Parent/Child Elements</span></span>



| <span data-ttu-id="f9364-116">Иерархия</span><span class="sxs-lookup"><span data-stu-id="f9364-116">Hierarchy</span></span>       | <span data-ttu-id="f9364-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="f9364-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="f9364-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f9364-118">Parent elements</span></span> | <span data-ttu-id="f9364-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="f9364-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="f9364-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f9364-120">Child elements</span></span>  | <span data-ttu-id="f9364-121">**ButtonText**, **буттонтип**</span><span class="sxs-lookup"><span data-stu-id="f9364-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f9364-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9364-122">Remarks</span></span>

<span data-ttu-id="f9364-123">**ServiceTask1** считается основной областью задач для привлечения к коммерческой деятельности.</span><span class="sxs-lookup"><span data-stu-id="f9364-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="f9364-124">Это область задач, которая отображается, когда пользователь выбирает приобретать музыку.</span><span class="sxs-lookup"><span data-stu-id="f9364-124">It is the task pane that displays when the user chooses to purchase music.</span></span> <span data-ttu-id="f9364-125">Используйте **ServiceTask2** для других действий в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="f9364-125">Use **ServiceTask2** for other online store activity.</span></span>

> [!Note]  
> <span data-ttu-id="f9364-126">Проигрыватель Windows Media 10 содержит три области задач, в которых Интернет-магазин может отображать свои веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="f9364-126">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="f9364-127">Интернет-магазин может использовать одну, две или все три области задач.</span><span class="sxs-lookup"><span data-stu-id="f9364-127">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="f9364-128">Проигрыватель Windows Media 11 имеет только одну область задач, которую пользователь может просматривать, щелкнув вкладку **Интернет-магазины** . проигрыватель Windows Media 11 игнорирует элементы **ServiceTask2** и **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="f9364-128">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="f9364-129">Области задач в Интернет-магазинах используют один экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="f9364-129">Online stores task panes share a single browser instance.</span></span> <span data-ttu-id="f9364-130">Это означает, что не следует писать код скрипта на веб-странице, которая будет продолжать выполняться, когда пользователь перейдет из текущей задачи службы.</span><span class="sxs-lookup"><span data-stu-id="f9364-130">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="f9364-131">Когда пользователь переключает области задач, проигрыватель Windows Media сохраняет URL-адреса и файлы cookie сеанса.</span><span class="sxs-lookup"><span data-stu-id="f9364-131">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="f9364-132">Когда пользователь переключается обратно в область задач, проигрыватель восстанавливает URL-адрес и файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="f9364-132">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="f9364-133">Если пользователь выбирает использование другого Интернет-магазина, данные URL и сеанса очищаются.</span><span class="sxs-lookup"><span data-stu-id="f9364-133">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="f9364-134">В следующей таблице приведены параметры, отправленные с помощью запроса URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f9364-134">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="f9364-135">Другие могут присутствовать в целях совместимости с прежними версиями.</span><span class="sxs-lookup"><span data-stu-id="f9364-135">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="f9364-136">Имя</span><span class="sxs-lookup"><span data-stu-id="f9364-136">Name</span></span>         | <span data-ttu-id="f9364-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f9364-137">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9364-138">*графическом*</span><span class="sxs-lookup"><span data-stu-id="f9364-138">*geoid*</span></span>      | <span data-ttu-id="f9364-139">Идентификатор географического расположения Windows.</span><span class="sxs-lookup"><span data-stu-id="f9364-139">Windows geographical location ID.</span></span> <span data-ttu-id="f9364-140">Идентификатор расположения задается пользователем в области **Расположение** в разделе региональные и языковые параметры панели управления.</span><span class="sxs-lookup"><span data-stu-id="f9364-140">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="f9364-141">*locale*</span><span class="sxs-lookup"><span data-stu-id="f9364-141">*locale*</span></span>     | <span data-ttu-id="f9364-142">Идентификатор локали проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9364-142">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="f9364-143">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="f9364-143">*userlocale*</span></span> | <span data-ttu-id="f9364-144">Идентификатор локали Windows.</span><span class="sxs-lookup"><span data-stu-id="f9364-144">Windows locale ID.</span></span> <span data-ttu-id="f9364-145">Языковой стандарт задается пользователем в области **стандарты и форматы** языковых и региональных параметров на панели управления.</span><span class="sxs-lookup"><span data-stu-id="f9364-145">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="f9364-146">*version*</span><span class="sxs-lookup"><span data-stu-id="f9364-146">*version*</span></span>    | <span data-ttu-id="f9364-147">Номер версии проигрывателя Windows Media в следующем формате: 10.0. x. xxxx или 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="f9364-147">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="f9364-148">Требования</span><span class="sxs-lookup"><span data-stu-id="f9364-148">Requirements</span></span>



| <span data-ttu-id="f9364-149">Требование</span><span class="sxs-lookup"><span data-stu-id="f9364-149">Requirement</span></span> | <span data-ttu-id="f9364-150">Значение</span><span class="sxs-lookup"><span data-stu-id="f9364-150">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="f9364-151">Версия</span><span class="sxs-lookup"><span data-stu-id="f9364-151">Version</span></span><br/> | <span data-ttu-id="f9364-152">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f9364-152">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9364-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9364-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9364-154">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="f9364-154">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="f9364-155">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="f9364-155">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="f9364-156">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="f9364-156">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





