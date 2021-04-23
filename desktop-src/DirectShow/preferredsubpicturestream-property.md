---
description: Свойство Преферредсубпиктурестреам извлекает предпочтительный поток субтитров для текущего сеанса просмотра.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Преферредсубпиктурестреам, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894641"
---
# <a name="preferredsubpicturestream-property"></a><span data-ttu-id="a563f-103">Преферредсубпиктурестреам, свойство</span><span class="sxs-lookup"><span data-stu-id="a563f-103">PreferredSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="a563f-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a563f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a563f-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="a563f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a563f-106">`PreferredSubpictureStream`Свойство получает предпочтительный поток субтитров для текущего сеанса просмотра.</span><span class="sxs-lookup"><span data-stu-id="a563f-106">The `PreferredSubpictureStream` property retrieves the preferred subpicture stream for the current viewing session.</span></span>

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="a563f-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a563f-107">Return Value</span></span>

<span data-ttu-id="a563f-108">Возвращает целочисленное значение, представляющее текущий предпочтительный поток субтитров в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="a563f-108">Returns an Integer value representing the current preferred subpicture stream in the system registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="a563f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a563f-109">Remarks</span></span>

<span data-ttu-id="a563f-110">Предпочтительный поток субтитров задается с помощью [**дефаултсубпиктурелЦид**](defaultsubpicturelcid-property.md)объекта [мсдвдадм](msdvdadm-object.md) .</span><span class="sxs-lookup"><span data-stu-id="a563f-110">The preferred subpicture stream is set with [MSDVDAdm](msdvdadm-object.md) object's [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md).</span></span>

 

 



