---
description: Происходит при изменении текущего выделения текста в элементе управления InkEdit или при перемещении точки вставки.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Событие InkEdit. Селчанже (with. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647449"
---
# <a name="inkeditselchange-event"></a><span data-ttu-id="cbfa1-103">Событие InkEdit. Селчанже</span><span class="sxs-lookup"><span data-stu-id="cbfa1-103">InkEdit.SelChange event</span></span>

<span data-ttu-id="cbfa1-104">Происходит при изменении текущего выделения текста в элементе управления [InkEdit](inkedit-control-reference.md) или при перемещении точки вставки.</span><span class="sxs-lookup"><span data-stu-id="cbfa1-104">Occurs when the current selection of text in the [InkEdit](inkedit-control-reference.md) control has changed or the insertion point has moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbfa1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbfa1-105">Syntax</span></span>


```C++
void SelChange();
```



## <a name="parameters"></a><span data-ttu-id="cbfa1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbfa1-106">Parameters</span></span>

<span data-ttu-id="cbfa1-107">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="cbfa1-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbfa1-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbfa1-108">Return value</span></span>

<span data-ttu-id="cbfa1-109">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cbfa1-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbfa1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbfa1-110">Remarks</span></span>

<span data-ttu-id="cbfa1-111">Событие **селчанже** можно использовать для проверки различных свойств, которые предоставляют сведения о текущем выделении (например, [**селболд**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)), что позволяет обновлять кнопки на панели инструментов, например.</span><span class="sxs-lookup"><span data-stu-id="cbfa1-111">You can use the **SelChange** event to check the various properties that give information about the current selection (such as [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) so you can update buttons in a toolbar, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbfa1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="cbfa1-112">Requirements</span></span>



| <span data-ttu-id="cbfa1-113">Требование</span><span class="sxs-lookup"><span data-stu-id="cbfa1-113">Requirement</span></span> | <span data-ttu-id="cbfa1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cbfa1-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbfa1-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbfa1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cbfa1-116">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cbfa1-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cbfa1-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbfa1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cbfa1-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cbfa1-118">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cbfa1-119">Header</span><span class="sxs-lookup"><span data-stu-id="cbfa1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbfa1-120"><dt>«С». h (также требует \_ ввода i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cbfa1-120"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cbfa1-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cbfa1-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="cbfa1-122"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbfa1-122"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cbfa1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbfa1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbfa1-124">InkEdit</span><span class="sxs-lookup"><span data-stu-id="cbfa1-124">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




