---
description: Метод Плайчаптерсаутостоп запускает воспроизведение в указанной главе по заданному названию и указанному количеству глав.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Метод Плайчаптерсаутостоп
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262365"
---
# <a name="playchaptersautostop-method"></a><span data-ttu-id="0524e-103">Метод Плайчаптерсаутостоп</span><span class="sxs-lookup"><span data-stu-id="0524e-103">PlayChaptersAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="0524e-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0524e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0524e-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="0524e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0524e-106">`PlayChaptersAutoStop`Метод запускает воспроизведение в указанной главе по заданному названию и указанному количеству глав.</span><span class="sxs-lookup"><span data-stu-id="0524e-106">The `PlayChaptersAutoStop` method starts playback at the specified chapter in the specified title and for the number of chapters specified.</span></span>

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a><span data-ttu-id="0524e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0524e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0524e-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ититле*</span><span class="sxs-lookup"><span data-stu-id="0524e-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="0524e-109">Задает заголовок в виде целочисленного значения.</span><span class="sxs-lookup"><span data-stu-id="0524e-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="0524e-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ичаптер*</span><span class="sxs-lookup"><span data-stu-id="0524e-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="0524e-111">Задает начальную главу как целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="0524e-111">Specifies the start chapter as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="0524e-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*ичаптеркаунт*</span><span class="sxs-lookup"><span data-stu-id="0524e-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span></span>
</dt> <dd>

<span data-ttu-id="0524e-113">Указывает количество глав для воспроизведения в виде целочисленного значения.</span><span class="sxs-lookup"><span data-stu-id="0524e-113">Specifies the number of chapters to play as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0524e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0524e-114">Return Value</span></span>

<span data-ttu-id="0524e-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0524e-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0524e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0524e-116">Remarks</span></span>

<span data-ttu-id="0524e-117">При воспроизведении последней главы этот метод приводит к тому, что в приложение отправляется уведомление о событии [**\_ \_ \_ автозавершения в разделе с DVD-диска EC**](ec-dvd-chapter-autostop.md) .</span><span class="sxs-lookup"><span data-stu-id="0524e-117">When the last chapter has played, this method causes an [**EC\_DVD\_CHAPTER\_AUTOSTOP**](ec-dvd-chapter-autostop.md) event notification to be sent to the application.</span></span>

 

 



