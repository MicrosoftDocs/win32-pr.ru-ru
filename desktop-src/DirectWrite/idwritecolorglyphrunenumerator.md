---
title: Интерфейс Идвритеколорглифруненумератор
description: Этот интерфейс позволяет приложению выполнять перечисление по цвету глифа цвета.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Непосредственная запись интерфейса Идвритеколорглифруненумератор
- Непосредственная запись интерфейса Идвритеколорглифруненумератор, описание
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802830"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a><span data-ttu-id="6f6ee-105">Интерфейс Идвритеколорглифруненумератор</span><span class="sxs-lookup"><span data-stu-id="6f6ee-105">IDWriteColorGlyphRunEnumerator interface</span></span>

<span data-ttu-id="6f6ee-106">Этот интерфейс позволяет приложению выполнять перечисление по цвету глифа цвета.</span><span class="sxs-lookup"><span data-stu-id="6f6ee-106">This interface allows the application to enumerate through the color glyph runs.</span></span> <span data-ttu-id="6f6ee-107">Перечислитель перечисляет слои в обратном порядке для соответствующего слоя.</span><span class="sxs-lookup"><span data-stu-id="6f6ee-107">The enumerator enumerates the layers in a back to front order for appropriate layering.</span></span>

## <a name="members"></a><span data-ttu-id="6f6ee-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="6f6ee-108">Members</span></span>

<span data-ttu-id="6f6ee-109">Интерфейс **идвритеколорглифруненумератор** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6f6ee-109">The **IDWriteColorGlyphRunEnumerator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6f6ee-110">**Идвритеколорглифруненумератор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6f6ee-110">**IDWriteColorGlyphRunEnumerator** also has these types of members:</span></span>

-   [<span data-ttu-id="6f6ee-111">Методы</span><span class="sxs-lookup"><span data-stu-id="6f6ee-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6f6ee-112">Методы</span><span class="sxs-lookup"><span data-stu-id="6f6ee-112">Methods</span></span>

<span data-ttu-id="6f6ee-113">Интерфейс **идвритеколорглифруненумератор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6f6ee-113">The **IDWriteColorGlyphRunEnumerator** interface has these methods.</span></span>



| <span data-ttu-id="6f6ee-114">Метод</span><span class="sxs-lookup"><span data-stu-id="6f6ee-114">Method</span></span>                                                                | <span data-ttu-id="6f6ee-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6f6ee-115">Description</span></span>                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="6f6ee-116">**жеткуррентрун**</span><span class="sxs-lookup"><span data-stu-id="6f6ee-116">**GetCurrentRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | <span data-ttu-id="6f6ee-117">Возвращает текущее выполнение глифа в перечислителе.</span><span class="sxs-lookup"><span data-stu-id="6f6ee-117">Returns the current glyph run of the enumerator.</span></span><br/> |
| [<span data-ttu-id="6f6ee-118">**MoveNext**</span><span class="sxs-lookup"><span data-stu-id="6f6ee-118">**MoveNext**</span></span>](idwritecolorglyphrunenumerator-movenext.md)           | <span data-ttu-id="6f6ee-119">Переход к следующему глифу выполняется в перечислителе.</span><span class="sxs-lookup"><span data-stu-id="6f6ee-119">Move to the next glyph run in the enumerator.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="6f6ee-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6f6ee-120">Requirements</span></span>



| <span data-ttu-id="6f6ee-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6f6ee-121">Requirement</span></span> | <span data-ttu-id="6f6ee-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6f6ee-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f6ee-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f6ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6f6ee-124">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="6f6ee-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="6f6ee-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f6ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6f6ee-126">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="6f6ee-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="6f6ee-127">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="6f6ee-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="6f6ee-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="6f6ee-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="6f6ee-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f6ee-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f6ee-130"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f6ee-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6f6ee-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6f6ee-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f6ee-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f6ee-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

