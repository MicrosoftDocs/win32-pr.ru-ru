---
title: Интерфейс IDWriteTextFormat2
description: Описывает свойства шрифта и абзаца, используемые для форматирования текста, а также сведения о языковых стандартах. | Интерфейс IDWriteTextFormat2
ms.assetid: 4396d2b0-240f-ee8b-1d21-c4294fb29b51
keywords:
- Непосредственная запись интерфейса IDWriteTextFormat2
- Непосредственная запись интерфейса IDWriteTextFormat2, описание
topic_type:
- apiref
api_name:
- IDWriteTextFormat2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06abf78095953f684ed6ec3fd241c699b2b37db4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664917"
---
# <a name="idwritetextformat2-interface"></a><span data-ttu-id="fb114-106">Интерфейс IDWriteTextFormat2</span><span class="sxs-lookup"><span data-stu-id="fb114-106">IDWriteTextFormat2 interface</span></span>

<span data-ttu-id="fb114-107">Описывает свойства шрифта и абзаца, используемые для форматирования текста, а также сведения о языковых стандартах.</span><span class="sxs-lookup"><span data-stu-id="fb114-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span>

## <a name="members"></a><span data-ttu-id="fb114-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="fb114-108">Members</span></span>

<span data-ttu-id="fb114-109">Интерфейс **IDWriteTextFormat2** наследует от [**IDWriteTextFormat1**](idwritetextformat1.md).</span><span class="sxs-lookup"><span data-stu-id="fb114-109">The **IDWriteTextFormat2** interface inherits from [**IDWriteTextFormat1**](idwritetextformat1.md).</span></span> <span data-ttu-id="fb114-110">**IDWriteTextFormat2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fb114-110">**IDWriteTextFormat2** also has these types of members:</span></span>

-   [<span data-ttu-id="fb114-111">Методы</span><span class="sxs-lookup"><span data-stu-id="fb114-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fb114-112">Методы</span><span class="sxs-lookup"><span data-stu-id="fb114-112">Methods</span></span>

<span data-ttu-id="fb114-113">Интерфейс **IDWriteTextFormat2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="fb114-113">The **IDWriteTextFormat2** interface has these methods.</span></span>



| <span data-ttu-id="fb114-114">Метод</span><span class="sxs-lookup"><span data-stu-id="fb114-114">Method</span></span>                                                      | <span data-ttu-id="fb114-115">Описание</span><span class="sxs-lookup"><span data-stu-id="fb114-115">Description</span></span>                                                                      |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="fb114-116">**жетлинеспаЦинг**</span><span class="sxs-lookup"><span data-stu-id="fb114-116">**GetLineSpacing**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat2-getlinespacing) | <span data-ttu-id="fb114-117">Возвращает набор корректировок междустрочного интервала для абзаца из нескольких строк.</span><span class="sxs-lookup"><span data-stu-id="fb114-117">Gets the line spacing adjustment set for a multiline text paragraph.</span></span> <br/> |
| [<span data-ttu-id="fb114-118">**сетлинеспаЦинг**</span><span class="sxs-lookup"><span data-stu-id="fb114-118">**SetLineSpacing**</span></span>](idwritetextformat2-setlinespacing.md) | <span data-ttu-id="fb114-119">Задать Междустрочный зазор.</span><span class="sxs-lookup"><span data-stu-id="fb114-119">Set line spacing.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="fb114-120">Требования</span><span class="sxs-lookup"><span data-stu-id="fb114-120">Requirements</span></span>



| <span data-ttu-id="fb114-121">Требование</span><span class="sxs-lookup"><span data-stu-id="fb114-121">Requirement</span></span> | <span data-ttu-id="fb114-122">Значение</span><span class="sxs-lookup"><span data-stu-id="fb114-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb114-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb114-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fb114-124">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="fb114-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="fb114-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb114-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fb114-126">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="fb114-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="fb114-127">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="fb114-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="fb114-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="fb114-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="fb114-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fb114-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb114-130"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb114-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fb114-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fb114-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb114-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb114-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb114-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb114-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb114-134">**IDWriteTextFormat1**</span><span class="sxs-lookup"><span data-stu-id="fb114-134">**IDWriteTextFormat1**</span></span>](idwritetextformat1.md)
</dt> </dl>

 

