---
title: Аксвиндовсмедиаплайер. Куррентмедиа, свойство
description: Свойство Куррентмедиа Возвращает или задает интерфейс Ивмпмедиа, соответствующий текущему элементу мультимедиа.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- Проигрыватель Windows Media для свойства Куррентмедиа
- Куррентмедиа свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Куррентмедиа
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698952"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a><span data-ttu-id="8f70f-106">Аксвиндовсмедиаплайер. Куррентмедиа, свойство</span><span class="sxs-lookup"><span data-stu-id="8f70f-106">AxWindowsMediaPlayer.currentMedia property</span></span>

<span data-ttu-id="8f70f-107">Свойство Куррентмедиа Возвращает или задает интерфейс Ивмпмедиа, соответствующий текущему элементу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8f70f-107">The currentMedia property gets or sets the IWMPMedia interface that corresponds to the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f70f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f70f-108">Syntax</span></span>


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="8f70f-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8f70f-109">Property value</span></span>

<span data-ttu-id="8f70f-110">Интерфейс Вмплиб. Ивмпмедиа, предоставляющий доступ к текущему элементу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8f70f-110">The WMPLib.IWMPMedia interface that provides access to the current media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f70f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f70f-111">Remarks</span></span>

<span data-ttu-id="8f70f-112">Если Аксвиндовсмедиаплайер. Settings. Свойство **автозапуска** имеет значение true, воспроизведение начинается автоматически при установке **куррентмедиа**.</span><span class="sxs-lookup"><span data-stu-id="8f70f-112">If the AxWindowsMediaPlayer.settings.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="8f70f-113">Интерфейс Ивмпмедиа для данного элемента мультимедиа можно получить с помощью свойства Ивмпплайлист. Item (метод Ивмпплайлист. Get \_ Item в C#).</span><span class="sxs-lookup"><span data-stu-id="8f70f-113">You can retrieve an IWMPMedia interface for a given media item through the IWMPPlaylist.Item property (the IWMPPlaylist.get\_Item method in C#).</span></span> <span data-ttu-id="8f70f-114">Чтобы загрузить элемент мультимедиа с помощью имени файла, задайте свойство URL-адреса или используйте Невмедиа.</span><span class="sxs-lookup"><span data-stu-id="8f70f-114">To load a media item using a file name, set the URL property or use newMedia.</span></span>

## <a name="examples"></a><span data-ttu-id="8f70f-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="8f70f-115">Examples</span></span>

<span data-ttu-id="8f70f-116">В следующем примере извлекается первый элемент мультимедиа из библиотеки и используется свойство Куррентмедиа, чтобы задать полученный элемент мультимедиа в качестве текущего элемента мультимедиа и отобразить его имя.</span><span class="sxs-lookup"><span data-stu-id="8f70f-116">The following example retrieves the first media item in the library and uses the currentMedia property to set the retrieved media item as the current media item and display its name.</span></span> <span data-ttu-id="8f70f-117">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="8f70f-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
```





## <a name="requirements"></a><span data-ttu-id="8f70f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8f70f-118">Requirements</span></span>



| <span data-ttu-id="8f70f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8f70f-119">Requirement</span></span> | <span data-ttu-id="8f70f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8f70f-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f70f-121">Версия</span><span class="sxs-lookup"><span data-stu-id="8f70f-121">Version</span></span><br/>   | <span data-ttu-id="8f70f-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8f70f-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="8f70f-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8f70f-123">Namespace</span></span><br/> | <span data-ttu-id="8f70f-124">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="8f70f-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8f70f-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="8f70f-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8f70f-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8f70f-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f70f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f70f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f70f-128">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8f70f-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8f70f-129">**Аксвиндовсмедиаплайер. Невмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8f70f-129">**AxWindowsMediaPlayer.newMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[<span data-ttu-id="8f70f-130">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8f70f-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8f70f-131">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8f70f-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8f70f-132">**Ивмпплайлист. Item (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8f70f-132">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8f70f-133">**Ивмпсеттингс. Автозапуск (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8f70f-133">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





