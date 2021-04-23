---
description: Метод Исаудиостреаменаблед извлекает значение, указывающее, включен ли указанный аудиопоток в текущем заголовке.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Метод Исаудиостреаменаблед
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536449"
---
# <a name="isaudiostreamenabled-method"></a><span data-ttu-id="0bb8e-103">Метод Исаудиостреаменаблед</span><span class="sxs-lookup"><span data-stu-id="0bb8e-103">IsAudioStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="0bb8e-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0bb8e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0bb8e-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="0bb8e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0bb8e-106">`IsAudioStreamEnabled`Метод получает значение, указывающее, включен ли указанный аудиопоток в текущем заголовке.</span><span class="sxs-lookup"><span data-stu-id="0bb8e-106">The `IsAudioStreamEnabled` method retrieves a value indicating whether the specified audio stream is enabled in the current title.</span></span>

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="0bb8e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bb8e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb8e-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="0bb8e-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="0bb8e-109">Задает аудиопоток в виде целочисленного значения от 0 до 7.</span><span class="sxs-lookup"><span data-stu-id="0bb8e-109">Specifies the audio stream as an Integer value from 0 through 7.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bb8e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bb8e-110">Return Value</span></span>

<span data-ttu-id="0bb8e-111">Возвращает логическое значение, указывающее, доступен ли указанный звуковой поток для текущего заголовка.</span><span class="sxs-lookup"><span data-stu-id="0bb8e-111">Returns a Boolean value indicating whether the specified audio stream is available for the current title.</span></span> <span data-ttu-id="0bb8e-112">Значение true означает, что он доступен.</span><span class="sxs-lookup"><span data-stu-id="0bb8e-112">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bb8e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bb8e-113">Remarks</span></span>

<span data-ttu-id="0bb8e-114">Хотя диск может содержать до восьми независимых звуковых потоков, каждый поток необязательно доступен для каждого заголовка.</span><span class="sxs-lookup"><span data-stu-id="0bb8e-114">Although a disc can contain up to eight independent audio streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="0bb8e-115">Например, основной заголовок фильма может иметь три звуковых потока для английского, испанского и японского, но название «поступающий Аттрактионс» может иметь только один аудиопоток на английском языке.</span><span class="sxs-lookup"><span data-stu-id="0bb8e-115">For example, a main movie title might have three audio streams for English, Spanish, and Japanese, but the "Coming Attractions" title might have only one audio stream in English.</span></span> <span data-ttu-id="0bb8e-116">Перед установкой свойства [**куррентаудиостреам**](currentaudiostream-property.md) всегда проверяйте, что поток доступен для заголовка.</span><span class="sxs-lookup"><span data-stu-id="0bb8e-116">Always verify that a stream is available for a title before setting the [**CurrentAudioStream**](currentaudiostream-property.md) property.</span></span>

 

 



