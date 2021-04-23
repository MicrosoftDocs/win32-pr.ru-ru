---
title: Аксвиндовсмедиаплайер. URL, свойство
description: Свойство URL Возвращает или задает имя элемента мультимедиа для воспроизведения.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- URL-адрес свойства проигрывателя Windows Media
- Свойство URL-адреса проигрыватель Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство URL-адреса
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698849"
---
# <a name="axwindowsmediaplayerurl-property"></a><span data-ttu-id="d8e21-106">Аксвиндовсмедиаплайер. URL, свойство</span><span class="sxs-lookup"><span data-stu-id="d8e21-106">AxWindowsMediaPlayer.URL property</span></span>

<span data-ttu-id="d8e21-107">Свойство URL Возвращает или задает имя элемента мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8e21-107">The URL property gets or sets the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e21-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8e21-108">Syntax</span></span>


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a><span data-ttu-id="d8e21-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d8e21-109">Property value</span></span>

<span data-ttu-id="d8e21-110">Строка System. String, которая является URL-адресом элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d8e21-110">A System.String that is the URL of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e21-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8e21-111">Remarks</span></span>

<span data-ttu-id="d8e21-112">Этому свойству можно задать только URL-адрес в зоне безопасности с тем же или менее ограниченным, чем зона безопасности вызывающей программы или веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="d8e21-112">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="d8e21-113">Приложения, которые открывают элементы мультимедиа из защищенного брандмауэра, будут иметь лучшую производительность, если адрес указан с помощью DNS-имени, а не IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="d8e21-113">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="d8e21-114">Не вызывайте этот метод из кода обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="d8e21-114">Do not call this method from event handler code.</span></span> <span data-ttu-id="d8e21-115">Вызов **URL-адреса** из обработчика событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="d8e21-115">Calling **URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="d8e21-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="d8e21-116">Examples</span></span>

<span data-ttu-id="d8e21-117">В следующем примере пользователю предоставляется возможность указать файл мультимедиа, введя путь к файлу в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="d8e21-117">The following example allows the user to specify a media file by entering a file path in a text box.</span></span> <span data-ttu-id="d8e21-118">При нажатии кнопки свойству URL присваивается указанный файл, и файл воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="d8e21-118">When a button is clicked, the URL property is set to the specified file and the file is played.</span></span> <span data-ttu-id="d8e21-119">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="d8e21-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d8e21-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d8e21-120">Requirements</span></span>



| <span data-ttu-id="d8e21-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d8e21-121">Requirement</span></span> | <span data-ttu-id="d8e21-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d8e21-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e21-123">Версия</span><span class="sxs-lookup"><span data-stu-id="d8e21-123">Version</span></span><br/>   | <span data-ttu-id="d8e21-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d8e21-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d8e21-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d8e21-125">Namespace</span></span><br/> | <span data-ttu-id="d8e21-126">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="d8e21-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d8e21-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="d8e21-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d8e21-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d8e21-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8e21-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8e21-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e21-130">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d8e21-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





