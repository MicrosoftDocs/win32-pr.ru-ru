---
description: Метод Жетсубпиктурелангуаже извлекает язык для указанного потока субтитров.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Метод Жетсубпиктурелангуаже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672949"
---
# <a name="getsubpicturelanguage-method"></a><span data-ttu-id="90d4d-103">Метод Жетсубпиктурелангуаже</span><span class="sxs-lookup"><span data-stu-id="90d4d-103">GetSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="90d4d-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="90d4d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="90d4d-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="90d4d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="90d4d-106">`GetSubpictureLanguage`Метод получает язык для указанного потока субтитров.</span><span class="sxs-lookup"><span data-stu-id="90d4d-106">The `GetSubpictureLanguage` method retrieves the language for the specified subpicture stream.</span></span>

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="90d4d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="90d4d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90d4d-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="90d4d-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="90d4d-109">Указывает номер потока субтитров, язык текста которого требуется получить в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="90d4d-109">Specifies the subpicture stream number whose text language you want to retrieve as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90d4d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90d4d-110">Return Value</span></span>

<span data-ttu-id="90d4d-111">Возвращает читаемую строку, идентифицирующую язык аудиопотока в текущем заголовке.</span><span class="sxs-lookup"><span data-stu-id="90d4d-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



