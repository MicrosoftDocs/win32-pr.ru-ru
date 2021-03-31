---
description: Метод Stop останавливает воспроизведение.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Метод «завершение» (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999156"
---
# <a name="stop-method-directshow"></a><span data-ttu-id="e7c39-103">Метод «завершение» (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7c39-103">Stop Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="e7c39-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e7c39-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e7c39-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="e7c39-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e7c39-106">`Stop`Метод останавливает воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="e7c39-106">The `Stop` method stops playback.</span></span>

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a><span data-ttu-id="e7c39-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7c39-107">Return Value</span></span>

<span data-ttu-id="e7c39-108">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="e7c39-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7c39-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7c39-109">Remarks</span></span>

<span data-ttu-id="e7c39-110">Если для [**енаблересетонстоп**](enableresetonstop-property.md) задано значение true, вызов `Stop` помещает Навигатор DVD вместе с остальной частью графа фильтра в остановленное состояние, что означает, что при следующем нажатии кнопки **воспроизведения** воспроизведение начинается в начале диска. Если для **енаблересетонстоп** задано значение true, воспроизведение возобновляется, когда пользователь выдает следующую команду **Play** .</span><span class="sxs-lookup"><span data-stu-id="e7c39-110">If [**EnableResetOnStop**](enableresetonstop-property.md) is set to true, calling `Stop` puts the DVD Navigator, along with the rest of the filter graph, into a stopped state, which means that the next time the user presses the **Play** button, playback starts at the beginning of the disc. If **EnableResetOnStop** is set to true, playback resumes where it left off when the user issues the next **Play** command.</span></span>

 

 



