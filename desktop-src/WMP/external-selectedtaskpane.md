---
title: External. Селектедтаскпане
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство Селектедтаскпане указывает или получает текущую выбранную область задач.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- Внешний Селектедтаскпане проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694482"
---
# <a name="externalselectedtaskpane"></a><span data-ttu-id="03a18-106">External. Селектедтаскпане</span><span class="sxs-lookup"><span data-stu-id="03a18-106">External.SelectedTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="03a18-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="03a18-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="03a18-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="03a18-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="03a18-109">Свойство **селектедтаскпане** указывает или получает текущую выбранную область задач.</span><span class="sxs-lookup"><span data-stu-id="03a18-109">The **SelectedTaskPane** property specifies or retrieves the currently selected task pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a18-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03a18-110">Syntax</span></span>

<span data-ttu-id="03a18-111">Window. external. Селектедтаскпане = *сервицетаск*</span><span class="sxs-lookup"><span data-stu-id="03a18-111">window.external.SelectedTaskPane = *servicetask*</span></span>

## <a name="possible-values"></a><span data-ttu-id="03a18-112">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="03a18-112">Possible Values</span></span>

<span data-ttu-id="03a18-113">Это свойство является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="03a18-113">This property is a read/write **String**.</span></span> <span data-ttu-id="03a18-114">Возможные значения: "ServiceTask1", "ServiceTask2" и "ServiceTask3".</span><span class="sxs-lookup"><span data-stu-id="03a18-114">Possible values are "ServiceTask1", "ServiceTask2", and "ServiceTask3".</span></span>

## <a name="remarks"></a><span data-ttu-id="03a18-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03a18-115">Remarks</span></span>

<span data-ttu-id="03a18-116">Указание значения для этого свойства подсвечивает кнопку для этой панели.</span><span class="sxs-lookup"><span data-stu-id="03a18-116">Specifying a value for this property highlights the button for that pane.</span></span> <span data-ttu-id="03a18-117">Указанная область задач не активна.</span><span class="sxs-lookup"><span data-stu-id="03a18-117">It does not make the specified task pane active.</span></span> <span data-ttu-id="03a18-118">Необходимо указать значение этого свойства, чтобы задать текущую кнопку области задач для веб-страницы при загрузке страницы, чтобы убедиться, что активна правильная кнопка области задач.</span><span class="sxs-lookup"><span data-stu-id="03a18-118">You should specify a value for this property to set the current task pane button for your webpage when the page loads to ensure that the correct task pane button is active.</span></span>

<span data-ttu-id="03a18-119">Чтобы сделать конкретную область задач активной, используйте метод **навигатетаскпанеурл** .</span><span class="sxs-lookup"><span data-stu-id="03a18-119">To make a particular task pane the active one, use the **NavigateTaskPaneURL** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="03a18-120">Требования</span><span class="sxs-lookup"><span data-stu-id="03a18-120">Requirements</span></span>



| <span data-ttu-id="03a18-121">Требование</span><span class="sxs-lookup"><span data-stu-id="03a18-121">Requirement</span></span> | <span data-ttu-id="03a18-122">Значение</span><span class="sxs-lookup"><span data-stu-id="03a18-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03a18-123">Версия</span><span class="sxs-lookup"><span data-stu-id="03a18-123">Version</span></span><br/> | <span data-ttu-id="03a18-124">Проигрыватель Windows Media 10 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="03a18-124">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="03a18-125">DLL</span><span class="sxs-lookup"><span data-stu-id="03a18-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="03a18-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03a18-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a18-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03a18-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a18-128">**Внешний объект для Интернет-магазинов типа 2**</span><span class="sxs-lookup"><span data-stu-id="03a18-128">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="03a18-129">**External. Навигатетаскпанеурл**</span><span class="sxs-lookup"><span data-stu-id="03a18-129">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





