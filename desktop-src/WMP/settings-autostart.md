---
title: Параметры. Автозапуск
description: Свойство "Автозапуск" указывает или получает значение, указывающее, начинается ли воспроизведение текущего элемента мультимедиа автоматически.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Параметры. Автозапуск проигрывателя Windows Media
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647993"
---
# <a name="settingsautostart"></a><span data-ttu-id="1adb6-104">Параметры. Автозапуск</span><span class="sxs-lookup"><span data-stu-id="1adb6-104">Settings.autoStart</span></span>

<span data-ttu-id="1adb6-105">Свойство " **Автозапуск** " указывает или получает значение, указывающее, начинается ли воспроизведение текущего элемента мультимедиа автоматически.</span><span class="sxs-lookup"><span data-stu-id="1adb6-105">The **autoStart** property specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="1adb6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1adb6-106">Syntax</span></span>

<span data-ttu-id="1adb6-107">Player. Settings. Автозапуск</span><span class="sxs-lookup"><span data-stu-id="1adb6-107">player.settings.autoStart</span></span>

## <a name="possible-values"></a><span data-ttu-id="1adb6-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1adb6-108">Possible Values</span></span>

<span data-ttu-id="1adb6-109">Это свойство является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1adb6-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="1adb6-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1adb6-110">Value</span></span> | <span data-ttu-id="1adb6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1adb6-111">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="1adb6-112">true</span><span class="sxs-lookup"><span data-stu-id="1adb6-112">true</span></span>  | <span data-ttu-id="1adb6-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1adb6-113">Default.</span></span> <span data-ttu-id="1adb6-114">Элемент мультимедиа начинает воспроизводиться автоматически (см. примечания).</span><span class="sxs-lookup"><span data-stu-id="1adb6-114">The media item begins playing automatically (see Remarks).</span></span> |
| <span data-ttu-id="1adb6-115">false</span><span class="sxs-lookup"><span data-stu-id="1adb6-115">false</span></span> | <span data-ttu-id="1adb6-116">Элемент мультимедиа не начинает воспроизводиться автоматически.</span><span class="sxs-lookup"><span data-stu-id="1adb6-116">The media item does not begin playing automatically.</span></span>                |



 

## <a name="remarks"></a><span data-ttu-id="1adb6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1adb6-117">Remarks</span></span>

<span data-ttu-id="1adb6-118">Если параметру **автозапуска** присвоено значение true, воспроизведение элемента мультимедиа начнется при *проигрывателе*. **URL-адрес**, *проигрыватель*. **куррентплайлист** или *Player*. **куррентмедиа** .</span><span class="sxs-lookup"><span data-stu-id="1adb6-118">If **autoStart** is set to true, the media item will begin playing when *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** is set.</span></span> <span data-ttu-id="1adb6-119">В противном случае воспроизведение не начнется до тех пор, пока *элементы управления* не будут. вызывается метод **Play** .</span><span class="sxs-lookup"><span data-stu-id="1adb6-119">Otherwise, it will not start playing until the *Controls*.**play** method is called.</span></span>

<span data-ttu-id="1adb6-120">Так как свойство **автозапуска** для полного режима проигрывателя Windows Media может быть установлено глобально внешними событиями (например, Загрузка компакт-диска), для обложек и удаленных элементов управления проигрывателя не существует надежного значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1adb6-120">Because the **autoStart** property for the full mode of Windows Media Player can be set globally by external events (such as loading a CD), there is no reliable default value for skins and remoted Player controls.</span></span> <span data-ttu-id="1adb6-121">Это связано с тем, что в обоих случаях используется подсистема воспроизведения для проигрывателя в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="1adb6-121">This is because the playback engine of the full mode Player is used in both cases.</span></span>

<span data-ttu-id="1adb6-122">Необходимо задать для параметра **Автозапуск** значение false непосредственно перед установкой *проигрывателя*. **URL-адрес**, *проигрыватель*. **куррентплайлист** или *Player*. **куррентмедиа** в обложках и удаленных элементах управления проигрывателя Windows Media, если вы хотите убедиться, что элемент мультимедиа не начинает воспроизводиться немедленно.</span><span class="sxs-lookup"><span data-stu-id="1adb6-122">You should set **autoStart** to false immediately before you set *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** in skins and remoted Windows Media Player controls if you want to ensure that the media item does not start playing immediately.</span></span> <span data-ttu-id="1adb6-123">Кроме того, если не задать для параметра **Автозапуск** значение true непосредственно перед указанием элемента мультимедиа, не следует полагаться на этот параметр в качестве замены с помощью *элементов управления*. метод **Play** .</span><span class="sxs-lookup"><span data-stu-id="1adb6-123">Also, unless you set **autostart** to true immediately before specifying a media item, you should not rely on this setting as a substitute for using the *Controls*.**play** method.</span></span>

## <a name="examples"></a><span data-ttu-id="1adb6-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="1adb6-124">Examples</span></span>

<span data-ttu-id="1adb6-125">В следующем примере создается элемент CHECKBOX HTML, который позволяет пользователю указать, будет ли элемент управления проигрывателя автоматически воспроизводить текущий элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1adb6-125">The following example creates an HTML CHECKBOX element that allows the user to specify whether the Player control plays the current media item automatically.</span></span> <span data-ttu-id="1adb6-126">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="1adb6-126">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a><span data-ttu-id="1adb6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1adb6-127">Requirements</span></span>



| <span data-ttu-id="1adb6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1adb6-128">Requirement</span></span> | <span data-ttu-id="1adb6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1adb6-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1adb6-130">Версия</span><span class="sxs-lookup"><span data-stu-id="1adb6-130">Version</span></span><br/> | <span data-ttu-id="1adb6-131">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1adb6-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1adb6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1adb6-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="1adb6-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1adb6-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1adb6-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1adb6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1adb6-135">**Player. Куррентмедиа**</span><span class="sxs-lookup"><span data-stu-id="1adb6-135">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="1adb6-136">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="1adb6-136">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="1adb6-137">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="1adb6-137">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





