---
description: Свойство Двдадм. Дисаблескринсавер включает или выключает экранную заставку.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Дисаблескринсавер, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894158"
---
# <a name="disablescreensaver-property"></a><span data-ttu-id="f21e6-103">Дисаблескринсавер, свойство</span><span class="sxs-lookup"><span data-stu-id="f21e6-103">DisableScreenSaver Property</span></span>

> [!Note]  
> <span data-ttu-id="f21e6-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f21e6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f21e6-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f21e6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f21e6-106">`DVDAdm.DisableScreenSaver`Свойство включает или выключает экранную заставку.</span><span class="sxs-lookup"><span data-stu-id="f21e6-106">The `DVDAdm.DisableScreenSaver` property turns the system screen saver on or off.</span></span>

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a><span data-ttu-id="f21e6-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f21e6-107">Return Value</span></span>

<span data-ttu-id="f21e6-108">Возвращает логическое значение, указывающее, отключены ли параметры экранной заставки для приложения проигрывателя DVD. значение true означает, что параметры отключены.</span><span class="sxs-lookup"><span data-stu-id="f21e6-108">Returns a Boolean value indicating whether the system's screen saver settings are disabled for the DVD player application; true means the settings are disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="f21e6-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f21e6-109">Remarks</span></span>

<span data-ttu-id="f21e6-110">Это свойство доступно для чтения и записи со значением по умолчанию true.</span><span class="sxs-lookup"><span data-stu-id="f21e6-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="f21e6-111">При просмотре DVD-Videoного диска пользователь обычно не использует мышь или клавиатуру в течение продолжительного периода времени.</span><span class="sxs-lookup"><span data-stu-id="f21e6-111">When viewing a DVD-Video disc, a user typically does not use the mouse or keyboard for extended periods of time.</span></span> <span data-ttu-id="f21e6-112">Таким образом, элемент управления ActiveX® Мсвебдвд по умолчанию отключает экранную заставку.</span><span class="sxs-lookup"><span data-stu-id="f21e6-112">The MSWebDVD ActiveX® control therefore disables the system screen saver by default.</span></span> <span data-ttu-id="f21e6-113">Объект</span><span class="sxs-lookup"><span data-stu-id="f21e6-113">Object</span></span>

## <a name="see-also"></a><span data-ttu-id="f21e6-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f21e6-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21e6-115">**ресторескринсавер**</span><span class="sxs-lookup"><span data-stu-id="f21e6-115">**RestoreScreenSaver**</span></span>](restorescreensaver-method.md)
</dt> <dt>

[<span data-ttu-id="f21e6-116">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="f21e6-116">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



