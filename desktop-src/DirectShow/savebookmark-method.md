---
description: Метод Савебукмарк сохраняет текущую позицию на диске и состояние объекта Мсвебдвд, чтобы пользователь мог вернуться к тому же месту позже.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Метод Савебукмарк (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675343"
---
# <a name="savebookmark-method"></a><span data-ttu-id="98e22-103">Метод Савебукмарк</span><span class="sxs-lookup"><span data-stu-id="98e22-103">SaveBookmark Method</span></span>

> [!Note]  
> <span data-ttu-id="98e22-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="98e22-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="98e22-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="98e22-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="98e22-106">`SaveBookmark`Метод сохраняет текущую позицию на диске и состояние объекта **мсвебдвд** , чтобы пользователь мог вернуться к тому же месту позже.</span><span class="sxs-lookup"><span data-stu-id="98e22-106">The `SaveBookmark` method saves the current disc position and state of the **MSWebDVD** object so the user can return to the same place later.</span></span>

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a><span data-ttu-id="98e22-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98e22-107">Return Value</span></span>

<span data-ttu-id="98e22-108">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="98e22-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e22-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98e22-109">Remarks</span></span>

<span data-ttu-id="98e22-110">Закладка является моментальным снимком текущего состояния DVD-навигатора.</span><span class="sxs-lookup"><span data-stu-id="98e22-110">A bookmark is a snapshot of the DVD Navigator's current state.</span></span> <span data-ttu-id="98e22-111">Сюда входят такие сведения, как место воспроизведения на диске и выбор потоков аудио-и звуковых изображений.</span><span class="sxs-lookup"><span data-stu-id="98e22-111">This includes information such as where it is playing on the disc, and which audio and subpictures streams are selected.</span></span> <span data-ttu-id="98e22-112">Сохранив закладку, пользователь может закрыть приложение, завершить работу компьютера и вернуться позже, чтобы продолжить просмотр диска справа от того, где он или он остался, и все параметры, как и ранее.</span><span class="sxs-lookup"><span data-stu-id="98e22-112">By saving a bookmark, the user can close the application, shut down the computer, and come back later to continue viewing the disc right where he or she left off, with all settings just as they were before.</span></span> <span data-ttu-id="98e22-113">В любое заданное время можно сохранить только одну закладку.</span><span class="sxs-lookup"><span data-stu-id="98e22-113">Only one bookmark can be saved at any given time.</span></span> <span data-ttu-id="98e22-114">При вызове `SaveBookmark` старая закладка перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="98e22-114">When you call `SaveBookmark`, the old bookmark is overwritten.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e22-115">Требования</span><span class="sxs-lookup"><span data-stu-id="98e22-115">Requirements</span></span>



| <span data-ttu-id="98e22-116">Требование</span><span class="sxs-lookup"><span data-stu-id="98e22-116">Requirement</span></span> | <span data-ttu-id="98e22-117">Значение</span><span class="sxs-lookup"><span data-stu-id="98e22-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="98e22-118">Header</span><span class="sxs-lookup"><span data-stu-id="98e22-118">Header</span></span><br/> | <dl> <span data-ttu-id="98e22-119"><dt>Сегмент. h</dt></span><span class="sxs-lookup"><span data-stu-id="98e22-119"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e22-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98e22-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e22-121">**ресторебукмарк**</span><span class="sxs-lookup"><span data-stu-id="98e22-121">**RestoreBookmark**</span></span>](restorebookmark-method.md)
</dt> </dl>

 

 




