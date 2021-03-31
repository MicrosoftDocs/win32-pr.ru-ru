---
description: Свойство Тоталтитлетиме извлекает общее время воспроизведения для текущего заголовка.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Тоталтитлетиме, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910407"
---
# <a name="totaltitletime-property"></a><span data-ttu-id="24c26-103">Тоталтитлетиме, свойство</span><span class="sxs-lookup"><span data-stu-id="24c26-103">TotalTitleTime Property</span></span>

> [!Note]  
> <span data-ttu-id="24c26-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="24c26-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="24c26-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="24c26-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="24c26-106">`TotalTitleTime`Свойство получает общее время воспроизведения для текущего заголовка.</span><span class="sxs-lookup"><span data-stu-id="24c26-106">The `TotalTitleTime` property retrieves the total playback time for the current title.</span></span>

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a><span data-ttu-id="24c26-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24c26-107">Return Value</span></span>

<span data-ttu-id="24c26-108">Возвращает общее время воспроизведения текущего заголовка в виде строки в формате "чч: мм: СС: FF".</span><span class="sxs-lookup"><span data-stu-id="24c26-108">Returns the total playing time of the current title as a String in the format "hh:mm:ss:ff".</span></span>

## <a name="remarks"></a><span data-ttu-id="24c26-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24c26-109">Remarks</span></span>

<span data-ttu-id="24c26-110">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24c26-110">This property is read-only with no default value.</span></span> <span data-ttu-id="24c26-111">Возвращаемая строка будет содержать 11 символов в формате "чч: мм: СС: FF" (часы, минуты, секунды, кадры).</span><span class="sxs-lookup"><span data-stu-id="24c26-111">The returned string will be 11 characters long in the format "hh:mm:ss:ff" (hours, minutes, seconds, frames).</span></span>

## <a name="see-also"></a><span data-ttu-id="24c26-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24c26-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c26-113">**плайаттиме**</span><span class="sxs-lookup"><span data-stu-id="24c26-113">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="24c26-114">**плайаттимеинтитле**</span><span class="sxs-lookup"><span data-stu-id="24c26-114">**PlayAtTimeInTitle**</span></span>](playattimeintitle-method.md)
</dt> </dl>

 

 



