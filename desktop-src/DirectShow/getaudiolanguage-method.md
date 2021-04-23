---
description: Метод Жетаудиолангуаже извлекает строку, указывающую, какой язык доступен в указанном звуковом потоке.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: Метод Жетаудиолангуаже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af71ad7943fe5442ded09f0b599c64c4b7215dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536638"
---
# <a name="getaudiolanguage-method"></a><span data-ttu-id="8c408-103">Метод Жетаудиолангуаже</span><span class="sxs-lookup"><span data-stu-id="8c408-103">GetAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="8c408-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8c408-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8c408-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="8c408-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8c408-106">`GetAudioLanguage`Метод получает строку, указывающую, какой язык доступен в указанном звуковом потоке.</span><span class="sxs-lookup"><span data-stu-id="8c408-106">The `GetAudioLanguage` method retrieves a string indicating which language is available on the specified audio stream.</span></span>

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="8c408-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c408-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c408-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="8c408-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="8c408-109">Указывает номер звукового потока в текущем заголовке в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="8c408-109">Specifies the audio stream number in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c408-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c408-110">Return Value</span></span>

<span data-ttu-id="8c408-111">Возвращает читаемую строку, идентифицирующую язык аудиопотока в текущем заголовке.</span><span class="sxs-lookup"><span data-stu-id="8c408-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



