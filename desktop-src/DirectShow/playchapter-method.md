---
description: Метод Плайчаптер запускает воспроизведение из указанной главы в текущем заголовке.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Метод Плайчаптер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682177"
---
# <a name="playchapter-method"></a><span data-ttu-id="e2e6a-103">Метод Плайчаптер</span><span class="sxs-lookup"><span data-stu-id="e2e6a-103">PlayChapter Method</span></span>

> [!Note]  
> <span data-ttu-id="e2e6a-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e2e6a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e2e6a-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="e2e6a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e2e6a-106">`PlayChapter`Метод запускает воспроизведение из указанной главы в текущем заголовке.</span><span class="sxs-lookup"><span data-stu-id="e2e6a-106">The `PlayChapter` method starts playback from the specified chapter within the current title.</span></span>

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a><span data-ttu-id="e2e6a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2e6a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e6a-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ичаптер*</span><span class="sxs-lookup"><span data-stu-id="e2e6a-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="e2e6a-109">Указывает индекс главы в текущем заголовке как целое число.</span><span class="sxs-lookup"><span data-stu-id="e2e6a-109">Specifies the chapter index in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e6a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2e6a-110">Return Value</span></span>

<span data-ttu-id="e2e6a-111">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="e2e6a-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2e6a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2e6a-112">Remarks</span></span>

<span data-ttu-id="e2e6a-113">По достижении конца указанной главы этот метод продолжит играть в последующие главы, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="e2e6a-113">When the end of the specified chapter is reached, this method continues playing subsequent chapters, if any exist.</span></span> <span data-ttu-id="e2e6a-114">Если вы хотите воспроизвести только указанную главу, используйте [**плайчаптерсаутостоп**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="e2e6a-114">If you want to play only a specified chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e2e6a-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2e6a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e6a-116">**плайчаптеринтитле**</span><span class="sxs-lookup"><span data-stu-id="e2e6a-116">**PlayChapterInTitle**</span></span>](playchapterintitle-method.md)
</dt> </dl>

 

 



