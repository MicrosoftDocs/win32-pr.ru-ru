---
description: Событие Упдатеоверлай отправляется при перемещении или изменении размера поверхности наложения или изменении ее цветового ключа.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: Упдатеоверлай (Ддрав. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669393"
---
# <a name="updateoverlay"></a><span data-ttu-id="4a327-103">упдатеоверлай</span><span class="sxs-lookup"><span data-stu-id="4a327-103">UpdateOverlay</span></span>

> [!Note]  
> <span data-ttu-id="4a327-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4a327-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4a327-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="4a327-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4a327-106">Событие **упдатеоверлай** отправляется при перемещении или изменении размера поверхности наложения или изменении ее цветового ключа.</span><span class="sxs-lookup"><span data-stu-id="4a327-106">The **UpdateOverlay** event is sent when the overlay surface has been moved or resized or its color key has changed.</span></span>

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a><span data-ttu-id="4a327-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a327-107">Remarks</span></span>

<span data-ttu-id="4a327-108">Приложения не должны беспокоиться о том, что область наложения изменяется или изменяется размер.</span><span class="sxs-lookup"><span data-stu-id="4a327-108">Applications should never be concerned about the overlay surface being resized or moved.</span></span> <span data-ttu-id="4a327-109">Все это обрабатывается внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="4a327-109">This is all handled internally.</span></span> <span data-ttu-id="4a327-110">Но это событие также отправляется при изменении ключа цвета.</span><span class="sxs-lookup"><span data-stu-id="4a327-110">But this event is also sent when the color key changes.</span></span> <span data-ttu-id="4a327-111">Это означает, что если приложение размещает Мсвебдвд как безоконное и отображает плавающие кнопки поверх видеоповерхности в полноэкранном режиме, оно должно реагировать на это событие, получая новое значение свойства **ColorKey** , чтобы оно может правильно нарисовать кнопки.</span><span class="sxs-lookup"><span data-stu-id="4a327-111">That means that if an application is hosting MSWebDVD as a windowless control and displaying floating buttons on top of the video surface in full-screen mode, it should respond to this event by getting the new value of the **ColorKey** property so that it can draw the buttons properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a327-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4a327-112">Requirements</span></span>



| <span data-ttu-id="4a327-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4a327-113">Requirement</span></span> | <span data-ttu-id="4a327-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4a327-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a327-115">Header</span><span class="sxs-lookup"><span data-stu-id="4a327-115">Header</span></span><br/> | <dl> <span data-ttu-id="4a327-116"><dt>Ддрав. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a327-116"><dt>Ddraw.h</dt></span></span> </dl> |



 

 




