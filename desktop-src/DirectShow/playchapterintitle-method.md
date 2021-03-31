---
description: Метод Плайчаптеринтитле воспроизводит указанную главу в указанном заголовке.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Метод Плайчаптеринтитле
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894029"
---
# <a name="playchapterintitle-method"></a><span data-ttu-id="0553f-103">Метод Плайчаптеринтитле</span><span class="sxs-lookup"><span data-stu-id="0553f-103">PlayChapterInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="0553f-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0553f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0553f-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="0553f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0553f-106">`PlayChapterInTitle`Метод воспроизводит указанную главу в указанном заголовке.</span><span class="sxs-lookup"><span data-stu-id="0553f-106">The `PlayChapterInTitle` method plays the specified chapter in the specified title.</span></span>

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a><span data-ttu-id="0553f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0553f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0553f-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ититле*</span><span class="sxs-lookup"><span data-stu-id="0553f-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="0553f-109">Задает заголовок в виде целочисленного значения.</span><span class="sxs-lookup"><span data-stu-id="0553f-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="0553f-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ичаптер*</span><span class="sxs-lookup"><span data-stu-id="0553f-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="0553f-111">Указывает главу как целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="0553f-111">Specifies the chapter as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0553f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0553f-112">Return Value</span></span>

<span data-ttu-id="0553f-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0553f-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0553f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0553f-114">Remarks</span></span>

<span data-ttu-id="0553f-115">Этот метод запускает воспроизведение в указанной главе, а затем переходит в неограниченное время.</span><span class="sxs-lookup"><span data-stu-id="0553f-115">This method starts playback at the specified chapter and then continues playing indefinitely.</span></span> <span data-ttu-id="0553f-116">Если вы хотите воспроизвести только определенную главу, используйте [**плайчаптерсаутостоп**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="0553f-116">If you want to play only a particular chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

 

 



