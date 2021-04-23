---
title: Метод Media. Жетмаркернаме
description: Метод Жетмаркернаме извлекает имя маркера по указанному индексу.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- Жетмаркернаме метод Windows Media Player
- Жетмаркернаме метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Жетмаркернаме
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699094"
---
# <a name="mediagetmarkername-method"></a><span data-ttu-id="05734-106">Метод Media. Жетмаркернаме</span><span class="sxs-lookup"><span data-stu-id="05734-106">Media.getMarkerName method</span></span>

<span data-ttu-id="05734-107">Метод **жетмаркернаме** извлекает имя маркера по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="05734-107">The **getMarkerName** method retrieves the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="05734-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05734-108">Syntax</span></span>


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="05734-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="05734-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05734-110">*маркернум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05734-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05734-111">**Число** (**длинное**), определяющее индекс маркера.</span><span class="sxs-lookup"><span data-stu-id="05734-111">**Number** (**long**) specifying a marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05734-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05734-112">Return value</span></span>

<span data-ttu-id="05734-113">Этот метод возвращает **строку**.</span><span class="sxs-lookup"><span data-stu-id="05734-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="05734-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05734-114">Remarks</span></span>

<span data-ttu-id="05734-115">Этот метод возвращает **значение NULL** , если указанный маркер не существует.</span><span class="sxs-lookup"><span data-stu-id="05734-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="05734-116">Некоторые цифровые мультимедийные элементы не содержат маркеров.</span><span class="sxs-lookup"><span data-stu-id="05734-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="05734-117">Используйте **маркеркаунт** , чтобы узнать, сколько маркеров находится в текущем клипе.</span><span class="sxs-lookup"><span data-stu-id="05734-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="05734-118">Номера индексов маркеров начинаются с 1.</span><span class="sxs-lookup"><span data-stu-id="05734-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="05734-119">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="05734-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="05734-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="05734-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="05734-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="05734-121">Examples</span></span>

<span data-ttu-id="05734-122">В следующем примере JScript используется *носитель*. **жетмаркернаме** для заполнения HTML-элемента textarea с именем мнамес именами маркеров в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="05734-122">The following JScript example uses *Media*.**getMarkerName** to fill an HTML TEXTAREA element named MNAMES with the names of the markers in the current media item.</span></span> <span data-ttu-id="05734-123">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="05734-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="05734-124">Требования</span><span class="sxs-lookup"><span data-stu-id="05734-124">Requirements</span></span>



| <span data-ttu-id="05734-125">Требование</span><span class="sxs-lookup"><span data-stu-id="05734-125">Requirement</span></span> | <span data-ttu-id="05734-126">Значение</span><span class="sxs-lookup"><span data-stu-id="05734-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05734-127">Версия</span><span class="sxs-lookup"><span data-stu-id="05734-127">Version</span></span><br/> | <span data-ttu-id="05734-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="05734-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="05734-129">DLL</span><span class="sxs-lookup"><span data-stu-id="05734-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="05734-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05734-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05734-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05734-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05734-132">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="05734-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="05734-133">**Media. Жетмаркертиме**</span><span class="sxs-lookup"><span data-stu-id="05734-133">**Media.getMarkerTime**</span></span>](media-getmarkertime.md)
</dt> <dt>

[<span data-ttu-id="05734-134">**Media. Маркеркаунт**</span><span class="sxs-lookup"><span data-stu-id="05734-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="05734-135">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="05734-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="05734-136">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="05734-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





