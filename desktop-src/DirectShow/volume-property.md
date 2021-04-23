---
description: Свойство Volume задает или получает громкость динамика для выходных данных аудиопотока.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Свойство Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543767"
---
# <a name="volume-property"></a><span data-ttu-id="6ed85-103">Свойство Volume</span><span class="sxs-lookup"><span data-stu-id="6ed85-103">Volume Property</span></span>

> [!Note]  
> <span data-ttu-id="6ed85-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6ed85-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6ed85-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="6ed85-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6ed85-106">`Volume`Свойство задает или получает громкость динамика для выходных данных аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="6ed85-106">The `Volume` property sets or retrieves the speaker volume for the audio stream output.</span></span>

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a><span data-ttu-id="6ed85-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ed85-107">Return Value</span></span>

<span data-ttu-id="6ed85-108">Возвращает уровень громкости в виде затухания в децибел в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="6ed85-108">Returns the volume level as attenuation in decibels as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ed85-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ed85-109">Remarks</span></span>

<span data-ttu-id="6ed85-110">Это свойство доступно для чтения и записи со значением по умолчанию 0.</span><span class="sxs-lookup"><span data-stu-id="6ed85-110">This property is read/write with a default value of 0.</span></span> <span data-ttu-id="6ed85-111">Полный том равен 0, а 10 000 — тишина; шкала является логарифмической.</span><span class="sxs-lookup"><span data-stu-id="6ed85-111">Full volume is 0, and 10,000 is silence; the scale is logarithmic.</span></span> <span data-ttu-id="6ed85-112">Умножьте требуемый уровень шкала на 100 (например, 10 000 = 100 dB).</span><span class="sxs-lookup"><span data-stu-id="6ed85-112">Multiply the desired decibel level by 100 (for example 10,000 = 100 dB).</span></span>

 

 



