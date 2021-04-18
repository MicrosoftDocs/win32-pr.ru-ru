---
title: External. Навигатетаскпанеурл, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Навигатетаскпанеурл, метод
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Навигатетаскпанеурл метод Windows Media Player
- Навигатетаскпанеурл метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Навигатетаскпанеурл
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694499"
---
# <a name="externalnavigatetaskpaneurl-method"></a><span data-ttu-id="7cf28-107">External. Навигатетаскпанеурл, метод</span><span class="sxs-lookup"><span data-stu-id="7cf28-107">External.NavigateTaskPaneURL method</span></span>

> [!Note]  
> <span data-ttu-id="7cf28-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="7cf28-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7cf28-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7cf28-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7cf28-110">Метод **навигатетаскпанеурл** открывает веб-страницу в указанной области задач и изменяет фокус на указанную панель.</span><span class="sxs-lookup"><span data-stu-id="7cf28-110">The **NavigateTaskPaneURL** method opens a webpage in the specified task pane, and changes focus to the specified pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf28-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cf28-111">Syntax</span></span>


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a><span data-ttu-id="7cf28-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cf28-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf28-113">*бстркэйнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cf28-113">*bstrKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf28-114">**Строка** , содержащая имя ключа для Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="7cf28-114">**String** containing the key name for the online store.</span></span> <span data-ttu-id="7cf28-115">(обязательно)</span><span class="sxs-lookup"><span data-stu-id="7cf28-115">(required)</span></span>

</dd> <dt>

<span data-ttu-id="7cf28-116">*бстртаскпане* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cf28-116">*bstrTaskPane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf28-117">**Строка** , содержащая имя области задач, в которой открывается веб-страница.</span><span class="sxs-lookup"><span data-stu-id="7cf28-117">**String** containing the name of the task pane in which the webpage opens.</span></span> <span data-ttu-id="7cf28-118">(обязательно)</span><span class="sxs-lookup"><span data-stu-id="7cf28-118">(required)</span></span>

</dd> <dt>

<span data-ttu-id="7cf28-119">*бстрпарамс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cf28-119">*bstrParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf28-120">**Строка** , содержащая параметры строки запроса для добавления к URL-адресу, указанному элементом **navigate** документа serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="7cf28-120">**String** containing the query string parameters to append to the URL specified by the **Navigate** element of the ServiceInfo document.</span></span> <span data-ttu-id="7cf28-121">(необязательно).</span><span class="sxs-lookup"><span data-stu-id="7cf28-121">(optional)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf28-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cf28-122">Return value</span></span>

<span data-ttu-id="7cf28-123">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7cf28-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cf28-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cf28-124">Remarks</span></span>

<span data-ttu-id="7cf28-125">Переход к панели, не поддерживаемой Вашим Интернет-магазином, может привести к изменению текущего Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="7cf28-125">Navigating to a pane that your online store does not support may cause the current online store to change.</span></span>

<span data-ttu-id="7cf28-126">Значение, указанное для *бстрпарамс* , допустимо только в том случае, если **навигатетаскпанеурл** вызывается из веб-страниц, предоставляемых Интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="7cf28-126">The value specified for *bstrParams* is valid only when **NavigateTaskPaneURL** is called from webpages provided by the online store.</span></span>

<span data-ttu-id="7cf28-127">В следующей таблице перечислены допустимые значения для *бстртаскпане* и связанная область задач для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="7cf28-127">The following table lists of valid values for *bstrTaskPane* and the associated task pane for each.</span></span>



| <span data-ttu-id="7cf28-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7cf28-128">Value</span></span>            | <span data-ttu-id="7cf28-129">Панель задач</span><span class="sxs-lookup"><span data-stu-id="7cf28-129">Task Pane</span></span>                      |
|------------------|--------------------------------|
| <span data-ttu-id="7cf28-130">**ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="7cf28-130">**ServiceTask1**</span></span> | <span data-ttu-id="7cf28-131">Первая область задач оперативного хранилища.</span><span class="sxs-lookup"><span data-stu-id="7cf28-131">First online store task pane.</span></span>  |
| <span data-ttu-id="7cf28-132">**ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="7cf28-132">**ServiceTask2**</span></span> | <span data-ttu-id="7cf28-133">Вторая область задач оперативного магазина.</span><span class="sxs-lookup"><span data-stu-id="7cf28-133">Second online store task pane.</span></span> |
| <span data-ttu-id="7cf28-134">**ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="7cf28-134">**ServiceTask3**</span></span> | <span data-ttu-id="7cf28-135">Третья область задач Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="7cf28-135">Third online store task pane.</span></span>  |



 

<span data-ttu-id="7cf28-136">Код веб-страницы должен указывать значение [External. селектедтаскпане](external-selectedtaskpane.md) при загрузке, чтобы после завершения навигации была выбрана правильная кнопка области задач.</span><span class="sxs-lookup"><span data-stu-id="7cf28-136">Your webpage code should specify a value for [External.SelectedTaskPane](external-selectedtaskpane.md) when loading to ensure that the correct task pane button is highlighted after navigation is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="7cf28-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="7cf28-137">Examples</span></span>

<span data-ttu-id="7cf28-138">В следующем примере кода показано, как **навигатетаскпанеурл** создает URL-адрес веб-страницы, отображаемой для **ServiceTask1**.</span><span class="sxs-lookup"><span data-stu-id="7cf28-138">The following example code shows how **NavigateTaskPaneURL** creates the URL of the webpage to display for **ServiceTask1**.</span></span>

<span data-ttu-id="7cf28-139">Пример элемента **navigate** :</span><span class="sxs-lookup"><span data-stu-id="7cf28-139">Example of the **Navigate** element:</span></span>


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



<span data-ttu-id="7cf28-140">Пример вызова метода **навигатетаскпанеурл** :</span><span class="sxs-lookup"><span data-stu-id="7cf28-140">Example call to the **NavigateTaskPaneURL** method:</span></span>


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



<span data-ttu-id="7cf28-141">Пример итогового URL-адреса, используемого для веб-страницы, отображаемой в **ServiceTask1**:</span><span class="sxs-lookup"><span data-stu-id="7cf28-141">Example of resulting URL used for the webpage displayed in **ServiceTask1**:</span></span>


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a><span data-ttu-id="7cf28-142">Требования</span><span class="sxs-lookup"><span data-stu-id="7cf28-142">Requirements</span></span>



| <span data-ttu-id="7cf28-143">Требование</span><span class="sxs-lookup"><span data-stu-id="7cf28-143">Requirement</span></span> | <span data-ttu-id="7cf28-144">Значение</span><span class="sxs-lookup"><span data-stu-id="7cf28-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf28-145">Версия</span><span class="sxs-lookup"><span data-stu-id="7cf28-145">Version</span></span><br/> | <span data-ttu-id="7cf28-146">Проигрыватель Windows Media 10 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7cf28-146">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="7cf28-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7cf28-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="7cf28-148"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cf28-148"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cf28-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cf28-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf28-150">**Внешний объект для Интернет-магазинов типа 2**</span><span class="sxs-lookup"><span data-stu-id="7cf28-150">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7cf28-151">**External. Селектедтаскпане**</span><span class="sxs-lookup"><span data-stu-id="7cf28-151">**External.SelectedTaskPane**</span></span>](external-selectedtaskpane.md)
</dt> </dl>

 

 





