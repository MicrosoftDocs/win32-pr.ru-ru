---
title: Player. URL
description: Свойство URL указывает или получает имя элемента мультимедиа для воспроизведения.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Проигрыватель Windows Media Player. URL
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704341"
---
# <a name="playerurl"></a><span data-ttu-id="de5c9-104">Player. URL</span><span class="sxs-lookup"><span data-stu-id="de5c9-104">Player.URL</span></span>

<span data-ttu-id="de5c9-105">Свойство **URL** указывает или получает имя элемента мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="de5c9-105">The **URL** property specifies or retrieves the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de5c9-106">Syntax</span></span>

<span data-ttu-id="de5c9-107">*проигрыватель* . **URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="de5c9-107">*player* .**URL**</span></span>

## <a name="possible-values"></a><span data-ttu-id="de5c9-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="de5c9-108">Possible Values</span></span>

<span data-ttu-id="de5c9-109">Это свойство является **строкой** для чтения и записи и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="de5c9-109">This property is a read/write **String** with no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de5c9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de5c9-110">Remarks</span></span>

<span data-ttu-id="de5c9-111">Этому свойству можно задать только URL-адрес в зоне безопасности с тем же или менее ограниченным, чем зона безопасности вызывающей программы или веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="de5c9-111">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="de5c9-112">Приложения, которые открывают элементы мультимедиа из защищенного брандмауэра, будут иметь лучшую производительность, если адрес указан с помощью DNS-имени, а не IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="de5c9-112">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="de5c9-113">Не вызывайте этот метод из кода обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="de5c9-113">Do not call this method from event handler code.</span></span> <span data-ttu-id="de5c9-114">Вызов *проигрывателя*. **URL-адрес** из обработчика событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="de5c9-114">Calling *Player*.**URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="de5c9-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="de5c9-115">Examples</span></span>

<span data-ttu-id="de5c9-116">В следующем примере создается HTML-элемент ввода текста и элемент ввода HTML-кнопки.</span><span class="sxs-lookup"><span data-stu-id="de5c9-116">The following example creates an HTML TEXT input element and an HTML BUTTON input element.</span></span> <span data-ttu-id="de5c9-117">Элемент TEXT позволяет пользователю ввести путь для указания файла цифрового мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="de5c9-117">The TEXT element allows the user to type a path to specify a digital media file to play.</span></span> <span data-ttu-id="de5c9-118">Элемент BUTTON выполняет сценарий JScript, который открывает файл и запускает проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="de5c9-118">The BUTTON element executes JScript that opens the file and starts Windows Media Player.</span></span> <span data-ttu-id="de5c9-119">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="de5c9-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="de5c9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="de5c9-120">Requirements</span></span>



| <span data-ttu-id="de5c9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="de5c9-121">Requirement</span></span> | <span data-ttu-id="de5c9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="de5c9-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de5c9-123">Версия</span><span class="sxs-lookup"><span data-stu-id="de5c9-123">Version</span></span><br/> | <span data-ttu-id="de5c9-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="de5c9-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="de5c9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="de5c9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="de5c9-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de5c9-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de5c9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de5c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5c9-128">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="de5c9-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





