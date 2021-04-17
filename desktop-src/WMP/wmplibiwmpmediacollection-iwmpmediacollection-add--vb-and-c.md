---
title: Ивмпмедиаколлектион Add, метод
description: Метод Add добавляет новый элемент мультимедиа или список воспроизведения в библиотеку. | Ивмпмедиаколлектион Add, метод
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Добавление метода Windows Media Player
- Добавление метода Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Add
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665102"
---
# <a name="iwmpmediacollectionadd-method"></a><span data-ttu-id="d5119-107">Метод Ивмпмедиаколлектион:: Add</span><span class="sxs-lookup"><span data-stu-id="d5119-107">IWMPMediaCollection::add method</span></span>

<span data-ttu-id="d5119-108">Метод **Add** добавляет новый элемент мультимедиа или список воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="d5119-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5119-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5119-109">Syntax</span></span>


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a><span data-ttu-id="d5119-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5119-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5119-111">*бструрл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5119-111">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5119-112">**Строка System. String** , которая представляет собой URL-адрес, указывающий расположение элемента мультимедиа или списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d5119-112">A **System.String** that is the URL that specifies the location of the media item or playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5119-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5119-113">Return value</span></span>

<span data-ttu-id="d5119-114">Интерфейс **вмплиб. ивмпмедиа** для добавленного элемента или списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d5119-114">The **WMPLib.IWMPMedia** interface for the added item or playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5119-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5119-115">Remarks</span></span>

<span data-ttu-id="d5119-116">Этот метод загружает существующий элемент мультимедиа или список воспроизведения в библиотеку по заданному пути.</span><span class="sxs-lookup"><span data-stu-id="d5119-116">This method loads an existing media item or playlist into the library, given a path.</span></span> <span data-ttu-id="d5119-117">Этот метод не перемещает и не изменяет файл.</span><span class="sxs-lookup"><span data-stu-id="d5119-117">This method does not move or change the file.</span></span> <span data-ttu-id="d5119-118">Этот метод завершается ошибкой, если задан недопустимый локальный путь, но сами элементы мультимедиа не проверяются на допустимость перед добавлением в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="d5119-118">This method fails if given an invalid local path, but media items themselves are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="d5119-119">Этот метод принимает как статические, так и автоматические файлы списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d5119-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="d5119-120">Метод **ивмпплайлистколлектион. импортплайлист** также можно использовать для добавления статического списка воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="d5119-120">The **IWMPPlaylistCollection.importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="d5119-121">Перед вызовом этого метода необходимо иметь полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="d5119-121">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="d5119-122">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d5119-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d5119-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="d5119-123">Examples</span></span>

<span data-ttu-id="d5119-124">В следующем примере в коллекцию носителей проигрывателя Windows Media добавляются три объекта мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d5119-124">The following example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="d5119-125">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="d5119-125">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
```





## <a name="requirements"></a><span data-ttu-id="d5119-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d5119-126">Requirements</span></span>



| <span data-ttu-id="d5119-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d5119-127">Requirement</span></span> | <span data-ttu-id="d5119-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d5119-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5119-129">Версия</span><span class="sxs-lookup"><span data-stu-id="d5119-129">Version</span></span><br/>   | <span data-ttu-id="d5119-130">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d5119-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d5119-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d5119-131">Namespace</span></span><br/> | <span data-ttu-id="d5119-132">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="d5119-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d5119-133">Сборка</span><span class="sxs-lookup"><span data-stu-id="d5119-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d5119-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d5119-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5119-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5119-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5119-136">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d5119-136">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d5119-137">**Ивмпмедиаколлектион. Remove (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d5119-137">**IWMPMediaCollection.remove (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d5119-138">**Ивмпплайлистколлектион. Импортплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d5119-138">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





