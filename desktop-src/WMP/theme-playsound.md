---
title: THEME. playSound
description: Метод playSound воспроизводит указанный звуковой файл.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- Проигрыватель Windows Media THEME. playSound
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688873"
---
# <a name="themeplaysound"></a><span data-ttu-id="84597-104">THEME. playSound</span><span class="sxs-lookup"><span data-stu-id="84597-104">THEME.playSound</span></span>

<span data-ttu-id="84597-105">Метод **PlaySound** воспроизводит указанный звуковой файл.</span><span class="sxs-lookup"><span data-stu-id="84597-105">The **playSound** method plays the specified sound file.</span></span>

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a><span data-ttu-id="84597-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84597-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84597-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span><span class="sxs-lookup"><span data-stu-id="84597-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span></span>
</dt> <dd>

<span data-ttu-id="84597-108">**Строка** , указывающая имя звукового файла для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="84597-108">A **String** specifying the name of the sound file to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84597-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84597-109">Return Value</span></span>

<span data-ttu-id="84597-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="84597-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="84597-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84597-111">Remarks</span></span>

<span data-ttu-id="84597-112">Этот метод позволяет добавлять звуковые эффекты к обложке, например при нажатии кнопок.</span><span class="sxs-lookup"><span data-stu-id="84597-112">This method allows you to add sound effects to a skin for example, when buttons are clicked.</span></span> <span data-ttu-id="84597-113">Звук воспроизводится операционной системой напрямую, а не проигрывателем Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="84597-113">The sound is played by the operating system directly and not by Windows Media Player.</span></span> <span data-ttu-id="84597-114">Это означает, что звук нельзя контролировать с помощью параметров и методов проигрывателя Windows Media, но его можно воспроизводить, пока проигрыватель Windows Media воспроизводит другой файл цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="84597-114">This means that the sound cannot be controlled with Windows Media Player settings and methods, but it can be played while Windows Media Player is playing another digital media file.</span></span>

<span data-ttu-id="84597-115">Этот метод поддерживает только файлы WAV.</span><span class="sxs-lookup"><span data-stu-id="84597-115">This method supports WAV files only.</span></span>

## <a name="requirements"></a><span data-ttu-id="84597-116">Требования</span><span class="sxs-lookup"><span data-stu-id="84597-116">Requirements</span></span>



| <span data-ttu-id="84597-117">Требование</span><span class="sxs-lookup"><span data-stu-id="84597-117">Requirement</span></span> | <span data-ttu-id="84597-118">Значение</span><span class="sxs-lookup"><span data-stu-id="84597-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="84597-119">Версия</span><span class="sxs-lookup"><span data-stu-id="84597-119">Version</span></span><br/> | <span data-ttu-id="84597-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="84597-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84597-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84597-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84597-122">**Элемент THEME**</span><span class="sxs-lookup"><span data-stu-id="84597-122">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





