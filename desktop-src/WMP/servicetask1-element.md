---
title: ServiceTask1, элемент
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Элемент ServiceTask1 представляет первую область задач оперативного хранилища.
ms.assetid: 39b149ae-ea67-4fba-812b-15a97044fcd8
keywords:
- Проигрыватель Windows Media, элемент ServiceTask1
topic_type:
- apiref
api_name:
- ServiceTask1 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ca83f5f7935e8d1dfd376f569bd61f68d7e93bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648735"
---
# <a name="servicetask1-element"></a><span data-ttu-id="9ce53-106">ServiceTask1, элемент</span><span class="sxs-lookup"><span data-stu-id="9ce53-106">ServiceTask1 Element</span></span>

> [!Note]  
> <span data-ttu-id="9ce53-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="9ce53-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9ce53-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9ce53-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9ce53-109">Элемент **ServiceTask1** представляет первую область задач оперативного хранилища.</span><span class="sxs-lookup"><span data-stu-id="9ce53-109">The **ServiceTask1** element represents the first online store task pane.</span></span>

``` syntax
<ServiceTask1
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="9ce53-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9ce53-110">Attributes</span></span>



| <span data-ttu-id="9ce53-111">Термин</span><span class="sxs-lookup"><span data-stu-id="9ce53-111">Term</span></span>                                                                                                                             | <span data-ttu-id="9ce53-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9ce53-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="9ce53-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL-адрес** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="9ce53-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="9ce53-114">URL-адрес веб-страницы, отображаемой проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9ce53-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="9ce53-115">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9ce53-115">Parent/Child Elements</span></span>



| <span data-ttu-id="9ce53-116">Иерархия</span><span class="sxs-lookup"><span data-stu-id="9ce53-116">Hierarchy</span></span>       | <span data-ttu-id="9ce53-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="9ce53-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="9ce53-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9ce53-118">Parent elements</span></span> | <span data-ttu-id="9ce53-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="9ce53-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="9ce53-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9ce53-120">Child elements</span></span>  | <span data-ttu-id="9ce53-121">**ButtonText**, **буттонтип**</span><span class="sxs-lookup"><span data-stu-id="9ce53-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9ce53-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ce53-122">Remarks</span></span>

<span data-ttu-id="9ce53-123">**ServiceTask1** считается основной областью задач для привлечения к коммерческой деятельности.</span><span class="sxs-lookup"><span data-stu-id="9ce53-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="9ce53-124">Это область задач, которая отображается, когда пользователь выбирает приобретать музыку.</span><span class="sxs-lookup"><span data-stu-id="9ce53-124">It is the task pane that displays when the user chooses to purchase music.</span></span>

> [!Note]  
> <span data-ttu-id="9ce53-125">Проигрыватель Windows Media 10 содержит три области задач, в которых Интернет-магазин может отображать свои веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="9ce53-125">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="9ce53-126">Интернет-магазин может использовать одну, две или все три области задач.</span><span class="sxs-lookup"><span data-stu-id="9ce53-126">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="9ce53-127">Проигрыватель Windows Media 11 имеет только одну область задач, представленную **ServiceTask1**, которую пользователь может просматривать, перейдя на вкладку **Интернет-магазины** .</span><span class="sxs-lookup"><span data-stu-id="9ce53-127">Windows Media Player 11 has only one task pane, represented by **ServiceTask1**, which the user can view by clicking on the **Online Stores** tab.</span></span>

 

<span data-ttu-id="9ce53-128">Области задач Интернет-магазина используют один экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="9ce53-128">Online store task panes share a single browser instance.</span></span> <span data-ttu-id="9ce53-129">Это означает, что не следует писать код скрипта на веб-странице, которая будет продолжать выполняться, когда пользователь перейдет из текущей задачи службы.</span><span class="sxs-lookup"><span data-stu-id="9ce53-129">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="9ce53-130">Когда пользователь переключает области задач, проигрыватель Windows Media сохраняет URL-адреса и файлы cookie сеанса.</span><span class="sxs-lookup"><span data-stu-id="9ce53-130">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="9ce53-131">Когда пользователь переключается обратно в область задач, проигрыватель восстанавливает URL-адрес и файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="9ce53-131">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="9ce53-132">Если пользователь выбирает использование другого Интернет-магазина, данные URL и сеанса очищаются.</span><span class="sxs-lookup"><span data-stu-id="9ce53-132">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="9ce53-133">В следующей таблице приведены параметры, отправленные с помощью запроса URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="9ce53-133">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="9ce53-134">Другие могут присутствовать в целях совместимости с прежними версиями.</span><span class="sxs-lookup"><span data-stu-id="9ce53-134">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="9ce53-135">Имя</span><span class="sxs-lookup"><span data-stu-id="9ce53-135">Name</span></span>         | <span data-ttu-id="9ce53-136">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce53-136">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce53-137">*графическом*</span><span class="sxs-lookup"><span data-stu-id="9ce53-137">*geoid*</span></span>      | <span data-ttu-id="9ce53-138">Идентификатор географического расположения Windows.</span><span class="sxs-lookup"><span data-stu-id="9ce53-138">Windows geographical location ID.</span></span> <span data-ttu-id="9ce53-139">Идентификатор расположения задается пользователем в области **Расположение** в разделе региональные и языковые параметры панели управления.</span><span class="sxs-lookup"><span data-stu-id="9ce53-139">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="9ce53-140">*locale*</span><span class="sxs-lookup"><span data-stu-id="9ce53-140">*locale*</span></span>     | <span data-ttu-id="9ce53-141">Идентификатор локали проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9ce53-141">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="9ce53-142">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="9ce53-142">*userlocale*</span></span> | <span data-ttu-id="9ce53-143">Идентификатор локали Windows.</span><span class="sxs-lookup"><span data-stu-id="9ce53-143">Windows locale ID.</span></span> <span data-ttu-id="9ce53-144">Языковой стандарт задается пользователем в области **стандарты и форматы** языковых и региональных параметров на панели управления.</span><span class="sxs-lookup"><span data-stu-id="9ce53-144">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="9ce53-145">*version*</span><span class="sxs-lookup"><span data-stu-id="9ce53-145">*version*</span></span>    | <span data-ttu-id="9ce53-146">Номер версии проигрывателя Windows Media в следующем формате: 10.0. x. xxxx или 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="9ce53-146">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="9ce53-147">Требования</span><span class="sxs-lookup"><span data-stu-id="9ce53-147">Requirements</span></span>



| <span data-ttu-id="9ce53-148">Требование</span><span class="sxs-lookup"><span data-stu-id="9ce53-148">Requirement</span></span> | <span data-ttu-id="9ce53-149">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce53-149">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="9ce53-150">Версия</span><span class="sxs-lookup"><span data-stu-id="9ce53-150">Version</span></span><br/> | <span data-ttu-id="9ce53-151">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9ce53-151">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ce53-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ce53-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce53-153">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="9ce53-153">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="9ce53-154">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="9ce53-154">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="9ce53-155">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="9ce53-155">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





