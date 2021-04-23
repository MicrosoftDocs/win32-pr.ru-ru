---
title: Событие Player. Аудиолангуажечанже
description: Событие Аудиолангуажечанже возникает при изменении текущего звукового языка. | Событие Player. Аудиолангуажечанже
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Проигрыватель Windows Media Event Аудиолангуажечанже
- Проигрыватель Windows Media Event Аудиолангуажечанже, класс Player
- Класс проигрывателя Windows Media Player, событие Аудиолангуажечанже
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704348"
---
# <a name="playeraudiolanguagechange-event"></a><span data-ttu-id="09b7c-107">Событие Player. Аудиолангуажечанже</span><span class="sxs-lookup"><span data-stu-id="09b7c-107">Player.AudioLanguageChange event</span></span>

<span data-ttu-id="09b7c-108">Событие **аудиолангуажечанже** возникает при изменении текущего звукового языка.</span><span class="sxs-lookup"><span data-stu-id="09b7c-108">The **AudioLanguageChange** event occurs when the current audio language changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b7c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09b7c-109">Syntax</span></span>


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a><span data-ttu-id="09b7c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="09b7c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09b7c-111">*Надежно*</span><span class="sxs-lookup"><span data-stu-id="09b7c-111">*LangID*</span></span> 
</dt> <dd>

<span data-ttu-id="09b7c-112">**Число** (**длинное**), определяющее новый идентификатор локали (LCID).</span><span class="sxs-lookup"><span data-stu-id="09b7c-112">**Number** (**long**) specifying the new locale identifier (LCID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09b7c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09b7c-113">Return value</span></span>

<span data-ttu-id="09b7c-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="09b7c-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09b7c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09b7c-115">Remarks</span></span>

<span data-ttu-id="09b7c-116">Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.</span><span class="sxs-lookup"><span data-stu-id="09b7c-116">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="09b7c-117">Значение параметров события указывается проигрывателем Windows Media, и к нему можно получить доступ или передать методу в импортированном файле Microsoft JScript, используя имя параметра.</span><span class="sxs-lookup"><span data-stu-id="09b7c-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported Microsoft JScript file by using the parameter name given.</span></span> <span data-ttu-id="09b7c-118">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="09b7c-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="09b7c-119">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="09b7c-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="09b7c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="09b7c-120">Requirements</span></span>



| <span data-ttu-id="09b7c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="09b7c-121">Requirement</span></span> | <span data-ttu-id="09b7c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="09b7c-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09b7c-123">Версия</span><span class="sxs-lookup"><span data-stu-id="09b7c-123">Version</span></span><br/> | <span data-ttu-id="09b7c-124">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="09b7c-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="09b7c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="09b7c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="09b7c-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09b7c-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09b7c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09b7c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b7c-128">**Controls. Куррентаудиолангуаже**</span><span class="sxs-lookup"><span data-stu-id="09b7c-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="09b7c-129">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="09b7c-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





