---
title: Метод Media. Жетмаркертиме
description: Метод Жетмаркертиме извлекает время маркера по указанному индексу.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- Жетмаркертиме метод Windows Media Player
- Жетмаркертиме метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Жетмаркертиме
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699006"
---
# <a name="mediagetmarkertime-method"></a><span data-ttu-id="20447-106">Метод Media. Жетмаркертиме</span><span class="sxs-lookup"><span data-stu-id="20447-106">Media.getMarkerTime method</span></span>

<span data-ttu-id="20447-107">Метод **жетмаркертиме** извлекает время маркера по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="20447-107">The **getMarkerTime** method retrieves the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="20447-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20447-108">Syntax</span></span>


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="20447-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="20447-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20447-110">*маркернум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20447-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20447-111">**Число** (**длинное**), указывающее индекс маркера.</span><span class="sxs-lookup"><span data-stu-id="20447-111">**Number** (**long**) specifying the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20447-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20447-112">Return value</span></span>

<span data-ttu-id="20447-113">Этот метод возвращает **число** (**Double**), задающее положение маркера в секундах от начала клипа.</span><span class="sxs-lookup"><span data-stu-id="20447-113">This method returns a **Number** (**double**) specifying the location of the marker in seconds from the beginning of the clip.</span></span>

## <a name="remarks"></a><span data-ttu-id="20447-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20447-114">Remarks</span></span>

<span data-ttu-id="20447-115">Этот метод возвращает **значение NULL** , если указанный маркер не существует.</span><span class="sxs-lookup"><span data-stu-id="20447-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="20447-116">Некоторые цифровые мультимедийные элементы не содержат маркеров.</span><span class="sxs-lookup"><span data-stu-id="20447-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="20447-117">Используйте **маркеркаунт** , чтобы узнать, сколько маркеров находится в текущем клипе.</span><span class="sxs-lookup"><span data-stu-id="20447-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="20447-118">Номера индексов маркеров начинаются с 1.</span><span class="sxs-lookup"><span data-stu-id="20447-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="20447-119">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="20447-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="20447-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="20447-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="20447-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="20447-121">Examples</span></span>

<span data-ttu-id="20447-122">В следующем примере JScript используется *носитель*. **жетмаркертиме** для заполнения HTML-элемента textarea с именем мтимес расположением каждого маркера.</span><span class="sxs-lookup"><span data-stu-id="20447-122">The following JScript example uses *Media*.**getMarkerTime** to fill an HTML TEXTAREA element named MTIMES with the location of each marker.</span></span> <span data-ttu-id="20447-123">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="20447-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="20447-124">Требования</span><span class="sxs-lookup"><span data-stu-id="20447-124">Requirements</span></span>



| <span data-ttu-id="20447-125">Требование</span><span class="sxs-lookup"><span data-stu-id="20447-125">Requirement</span></span> | <span data-ttu-id="20447-126">Значение</span><span class="sxs-lookup"><span data-stu-id="20447-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="20447-127">Версия</span><span class="sxs-lookup"><span data-stu-id="20447-127">Version</span></span><br/> | <span data-ttu-id="20447-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="20447-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="20447-129">DLL</span><span class="sxs-lookup"><span data-stu-id="20447-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="20447-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20447-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20447-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20447-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20447-132">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="20447-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="20447-133">**Media. Жетмаркернаме**</span><span class="sxs-lookup"><span data-stu-id="20447-133">**Media.getMarkerName**</span></span>](media-getmarkername.md)
</dt> <dt>

[<span data-ttu-id="20447-134">**Media. Маркеркаунт**</span><span class="sxs-lookup"><span data-stu-id="20447-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="20447-135">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="20447-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="20447-136">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="20447-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





