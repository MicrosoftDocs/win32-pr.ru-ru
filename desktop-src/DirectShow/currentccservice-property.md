---
description: Свойство Курренткксервице задает или получает текущую службу закрытого субтитров.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Курренткксервице, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894829"
---
# <a name="currentccservice-property"></a><span data-ttu-id="5b8d1-103">Курренткксервице, свойство</span><span class="sxs-lookup"><span data-stu-id="5b8d1-103">CurrentCCService Property</span></span>

> [!Note]  
> <span data-ttu-id="5b8d1-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5b8d1-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5b8d1-106">`CurrentCCService`Свойство задает или получает текущую службу закрытого субтитров.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-106">The `CurrentCCService` property sets or retrieves the current closed captioning service.</span></span>

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a><span data-ttu-id="5b8d1-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b8d1-107">Return Value</span></span>

<span data-ttu-id="5b8d1-108">Возвращает целочисленное значение, указывающее тип включенной службы субтитров.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-108">Returns an integer value indicating the type of closed captioning service enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b8d1-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b8d1-109">Remarks</span></span>

<span data-ttu-id="5b8d1-110">Возможные значения этого свойства:</span><span class="sxs-lookup"><span data-stu-id="5b8d1-110">The possible values of this property are:</span></span>



| <span data-ttu-id="5b8d1-111">Значение</span><span class="sxs-lookup"><span data-stu-id="5b8d1-111">Value</span></span> | <span data-ttu-id="5b8d1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5b8d1-112">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="5b8d1-113">0x0</span><span class="sxs-lookup"><span data-stu-id="5b8d1-113">0x0</span></span>   | <span data-ttu-id="5b8d1-114">Нет текущей службы.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-114">No current service.</span></span> <span data-ttu-id="5b8d1-115">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-115">This is the default value.</span></span>                       |
| <span data-ttu-id="5b8d1-116">0x1</span><span class="sxs-lookup"><span data-stu-id="5b8d1-116">0x1</span></span>   | <span data-ttu-id="5b8d1-117">Истинное название, первое поле.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-117">True captioning, first field.</span></span> <span data-ttu-id="5b8d1-118">Служба по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-118">Default service.</span></span>                       |
| <span data-ttu-id="5b8d1-119">0x2</span><span class="sxs-lookup"><span data-stu-id="5b8d1-119">0x2</span></span>   | <span data-ttu-id="5b8d1-120">Субтитры для вторичного языка, второе поле.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-120">Captioning for secondary language, second field.</span></span> <span data-ttu-id="5b8d1-121">Обычно не используется.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-121">Generally not used.</span></span> |



 

<span data-ttu-id="5b8d1-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5b8d1-122">This property is read/write.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b8d1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b8d1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b8d1-124">**ккактиве**</span><span class="sxs-lookup"><span data-stu-id="5b8d1-124">**CCActive**</span></span>](ccactive-property.md)
</dt> </dl>

 

 



