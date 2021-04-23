---
description: Свойство Куррентаудиостреам задает или получает номер включенного звукового потока.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Куррентаудиостреам, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655587"
---
# <a name="currentaudiostream-property"></a><span data-ttu-id="469e0-103">Куррентаудиостреам, свойство</span><span class="sxs-lookup"><span data-stu-id="469e0-103">CurrentAudioStream Property</span></span>

> [!Note]  
> <span data-ttu-id="469e0-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="469e0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="469e0-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="469e0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="469e0-106">`CurrentAudioStream`Свойство задает или получает номер включенного звукового потока.</span><span class="sxs-lookup"><span data-stu-id="469e0-106">The `CurrentAudioStream` property sets or retrieves the number of the enabled audio stream.</span></span>

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a><span data-ttu-id="469e0-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="469e0-107">Return Value</span></span>

<span data-ttu-id="469e0-108">Возвращает целочисленное значение от 0 до 7, указывающее текущий аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="469e0-108">Returns an integer value from 0 through 7 indicating the current audio stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="469e0-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="469e0-109">Remarks</span></span>

<span data-ttu-id="469e0-110">Это свойство доступно для чтения и записи и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="469e0-110">This property is read/write with no default value.</span></span> <span data-ttu-id="469e0-111">Прежде чем пытаться задать новый аудиопоток, вызовите [**исаудиостреаменаблед**](isaudiostreamenabled-method.md) , чтобы убедиться, что поток доступен.</span><span class="sxs-lookup"><span data-stu-id="469e0-111">Before attempting to set a new audio stream, call [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) to verify that the stream is available.</span></span>

## <a name="see-also"></a><span data-ttu-id="469e0-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="469e0-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="469e0-113">**аудиостреамсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="469e0-113">**AudioStreamsAvailable**</span></span>](audiostreamsavailable-property.md)
</dt> </dl>

 

 



