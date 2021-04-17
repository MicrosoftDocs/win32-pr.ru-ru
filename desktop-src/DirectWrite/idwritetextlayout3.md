---
title: Интерфейс IDWriteTextLayout3
description: Представляет блок текста после полного анализа и форматирования. | Интерфейс IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Непосредственная запись интерфейса IDWriteTextLayout3
- Непосредственная запись интерфейса IDWriteTextLayout3, описание
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664921"
---
# <a name="idwritetextlayout3-interface"></a><span data-ttu-id="25a3c-106">Интерфейс IDWriteTextLayout3</span><span class="sxs-lookup"><span data-stu-id="25a3c-106">IDWriteTextLayout3 interface</span></span>

<span data-ttu-id="25a3c-107">Представляет блок текста после полного анализа и форматирования.</span><span class="sxs-lookup"><span data-stu-id="25a3c-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="25a3c-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="25a3c-108">Members</span></span>

<span data-ttu-id="25a3c-109">Интерфейс **IDWriteTextLayout3** наследует от [**IDWriteTextLayout2**](idwritetextlayout2.md).</span><span class="sxs-lookup"><span data-stu-id="25a3c-109">The **IDWriteTextLayout3** interface inherits from [**IDWriteTextLayout2**](idwritetextlayout2.md).</span></span> <span data-ttu-id="25a3c-110">**IDWriteTextLayout3** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="25a3c-110">**IDWriteTextLayout3** also has these types of members:</span></span>

-   [<span data-ttu-id="25a3c-111">Методы</span><span class="sxs-lookup"><span data-stu-id="25a3c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="25a3c-112">Методы</span><span class="sxs-lookup"><span data-stu-id="25a3c-112">Methods</span></span>

<span data-ttu-id="25a3c-113">Интерфейс **IDWriteTextLayout3** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="25a3c-113">The **IDWriteTextLayout3** interface has these methods.</span></span>



| <span data-ttu-id="25a3c-114">Метод</span><span class="sxs-lookup"><span data-stu-id="25a3c-114">Method</span></span>                                                          | <span data-ttu-id="25a3c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="25a3c-115">Description</span></span>                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25a3c-116">**жетлинеметрикс**</span><span class="sxs-lookup"><span data-stu-id="25a3c-116">**GetLineMetrics**</span></span>](idwritetextlayout3-getlinemetrics.md)     | <span data-ttu-id="25a3c-117">Извлекает свойства каждой строки.</span><span class="sxs-lookup"><span data-stu-id="25a3c-117">Retrieves properties of each line.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="25a3c-118">**жетлинеспаЦинг**</span><span class="sxs-lookup"><span data-stu-id="25a3c-118">**GetLineSpacing**</span></span>](idwritetextlayout3-getlinespacing.md)     | <span data-ttu-id="25a3c-119">Возвращает сведения о межстрочном промежутке.</span><span class="sxs-lookup"><span data-stu-id="25a3c-119">Gets line spacing information.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="25a3c-120">**инвалидателайаут**</span><span class="sxs-lookup"><span data-stu-id="25a3c-120">**InvalidateLayout**</span></span>](idwritetextlayout3-invalidatelayout.md) | <span data-ttu-id="25a3c-121">Делает макет недействительным, принудительно перемера макета перед вызовом метрик или функций рисования.</span><span class="sxs-lookup"><span data-stu-id="25a3c-121">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="25a3c-122">Это полезно в том случае, если изменяется расположение шрифта, а макет должен быть перерисован или если размер, реализуемый клиентом, Идвритеинлинеобжект изменения.</span><span class="sxs-lookup"><span data-stu-id="25a3c-122">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span> <br/> |
| [<span data-ttu-id="25a3c-123">**сетлинеспаЦинг**</span><span class="sxs-lookup"><span data-stu-id="25a3c-123">**SetLineSpacing**</span></span>](idwritetextlayout3-setlinespacing.md)     | <span data-ttu-id="25a3c-124">Задать Междустрочный зазор.</span><span class="sxs-lookup"><span data-stu-id="25a3c-124">Set line spacing.</span></span><br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="25a3c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="25a3c-125">Requirements</span></span>



| <span data-ttu-id="25a3c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="25a3c-126">Requirement</span></span> | <span data-ttu-id="25a3c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="25a3c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25a3c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25a3c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="25a3c-129">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="25a3c-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="25a3c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25a3c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="25a3c-131">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="25a3c-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="25a3c-132">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="25a3c-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="25a3c-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="25a3c-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="25a3c-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="25a3c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="25a3c-135"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25a3c-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="25a3c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="25a3c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25a3c-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25a3c-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25a3c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25a3c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25a3c-139">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="25a3c-139">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





