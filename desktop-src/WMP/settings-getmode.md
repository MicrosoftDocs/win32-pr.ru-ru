---
title: Метод Settings. Мода
description: Метод метода мода определяет, активен ли режим "цикл" или "случайный".
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- метод мода проигрыватель Windows Media
- метод мода проигрыватель Windows Media, класс параметров
- Класс параметров проигрыватель Windows Media Player, метод onmode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648669"
---
# <a name="settingsgetmode-method"></a><span data-ttu-id="60267-106">Метод Settings. Мода</span><span class="sxs-lookup"><span data-stu-id="60267-106">Settings.getMode method</span></span>

<span data-ttu-id="60267-107">Метод метода **мода** определяет, активен ли режим "цикл" или "случайный".</span><span class="sxs-lookup"><span data-stu-id="60267-107">The **getMode** method determines whether the loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="60267-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60267-108">Syntax</span></span>


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a><span data-ttu-id="60267-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="60267-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60267-110">*моденаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60267-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60267-111">**Строка** , указывающая имя рассматриваемого режима, содержащее одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="60267-111">**String** specifying the name of the mode in question, containing one of the following values.</span></span>



| <span data-ttu-id="60267-112">Строка</span><span class="sxs-lookup"><span data-stu-id="60267-112">String</span></span>     | <span data-ttu-id="60267-113">Описание</span><span class="sxs-lookup"><span data-stu-id="60267-113">Description</span></span>                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60267-114">ауторевинд</span><span class="sxs-lookup"><span data-stu-id="60267-114">autoRewind</span></span> | <span data-ttu-id="60267-115">Дорожки перезапускаются в начале после воспроизведения в конце.</span><span class="sxs-lookup"><span data-stu-id="60267-115">Tracks are restarted at the beginning after playing to the end.</span></span>                                                          |
| <span data-ttu-id="60267-116">loop</span><span class="sxs-lookup"><span data-stu-id="60267-116">loop</span></span>       | <span data-ttu-id="60267-117">Последовательность дорожек повторяется самим собой.</span><span class="sxs-lookup"><span data-stu-id="60267-117">The sequence of tracks repeats itself.</span></span>                                                                                   |
| <span data-ttu-id="60267-118">шовфраме</span><span class="sxs-lookup"><span data-stu-id="60267-118">showFrame</span></span>  | <span data-ttu-id="60267-119">Ближайший ключевой кадр отображается в текущей позиции, когда не воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="60267-119">The nearest key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="60267-120">Этот режим не подходит для звуковых дорожек.</span><span class="sxs-lookup"><span data-stu-id="60267-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="60267-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="60267-121">shuffle</span></span>    | <span data-ttu-id="60267-122">Дорожки воспроизводятся в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="60267-122">Tracks are played in random order.</span></span>                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60267-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60267-123">Return value</span></span>

<span data-ttu-id="60267-124">Этот метод возвращает **логическое** значение, указывающее, активен ли заданный режим.</span><span class="sxs-lookup"><span data-stu-id="60267-124">This method returns a **Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="60267-125">Требования</span><span class="sxs-lookup"><span data-stu-id="60267-125">Requirements</span></span>



| <span data-ttu-id="60267-126">Требование</span><span class="sxs-lookup"><span data-stu-id="60267-126">Requirement</span></span> | <span data-ttu-id="60267-127">Значение</span><span class="sxs-lookup"><span data-stu-id="60267-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60267-128">Версия</span><span class="sxs-lookup"><span data-stu-id="60267-128">Version</span></span><br/> | <span data-ttu-id="60267-129">Для режимов цикла и случайного воспроизведения проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="60267-129">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="60267-130">Для режимов Ауторевинд и Шовфраме, проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="60267-130">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="60267-131">DLL</span><span class="sxs-lookup"><span data-stu-id="60267-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="60267-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60267-132"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="60267-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60267-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60267-134">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="60267-134">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="60267-135">**Settings. setMode**</span><span class="sxs-lookup"><span data-stu-id="60267-135">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





