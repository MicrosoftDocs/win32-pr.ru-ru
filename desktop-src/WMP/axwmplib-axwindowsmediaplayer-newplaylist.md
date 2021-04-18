---
title: Аксвиндовсмедиаплайер. Невплайлист, метод
description: Метод Невплайлист возвращает интерфейс Ивмпплайлист для нового списка воспроизведения.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- Невплайлист метод Windows Media Player
- Невплайлист метод Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, метод Невплайлист
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698765"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a><span data-ttu-id="e3e8d-106">Аксвиндовсмедиаплайер. Невплайлист, метод</span><span class="sxs-lookup"><span data-stu-id="e3e8d-106">AxWindowsMediaPlayer.newPlaylist method</span></span>

<span data-ttu-id="e3e8d-107">Метод Невплайлист возвращает интерфейс Ивмпплайлист для нового списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e3e8d-107">The newPlaylist method returns an IWMPPlaylist interface for a new playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e8d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3e8d-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a><span data-ttu-id="e3e8d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3e8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e8d-110">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="e3e8d-110">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="e3e8d-111">**Строка System. String** , которая является именем нового списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e3e8d-111">The **System.String** that is the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="e3e8d-112">*бструрл*</span><span class="sxs-lookup"><span data-stu-id="e3e8d-112">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="e3e8d-113">**Строка System. String** , которая является URL-адресом списка воспроизведения метафайла Windows Media, который используется для инициализации нового списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e3e8d-113">The **System.String** that is the URL of the Windows Media metafile playlist that is used to initialize the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3e8d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3e8d-114">Return value</span></span>

<span data-ttu-id="e3e8d-115">Интерфейс Вмплиб. Ивмпплайлист, представляющий только что созданный список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e3e8d-115">A WMPLib.IWMPPlaylist interface that represents the newly created playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3e8d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3e8d-116">Remarks</span></span>

<span data-ttu-id="e3e8d-117">Если параметр *бструрл* имеет значение null или является строкой нулевой длины (""), этот метод создает пустой **список воспроизведения**.</span><span class="sxs-lookup"><span data-stu-id="e3e8d-117">If the *bstrURL* parameter is a null or zero-length string (""), this method creates an empty **playlist**.</span></span> <span data-ttu-id="e3e8d-118">Если параметр *bstrName* является строкой нулевой длины (""), этот метод применяет текущее имя метафайла.</span><span class="sxs-lookup"><span data-stu-id="e3e8d-118">If the *bstrName* parameter is a zero-length string (""), this method applies the current metafile name.</span></span>

<span data-ttu-id="e3e8d-119">Новый список воспроизведения, созданный с помощью этого метода, не добавляется в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="e3e8d-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="e3e8d-120">Чтобы добавить новый список воспроизведения в библиотеку, используйте Ивмпплайлистколлектион. **импортплайлист** или ивмпплайлистколлектион. **невплайлист**.</span><span class="sxs-lookup"><span data-stu-id="e3e8d-120">To add a new playlist to the library, use IWMPPlaylistCollection.**importPlaylist** or IWMPPlaylistCollection.**newPlaylist**.</span></span> <span data-ttu-id="e3e8d-121">Все начальные и конечные пробелы в имени списка воспроизведения автоматически удаляются при добавлении в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="e3e8d-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="e3e8d-122">Так как библиотека допускает наличие нескольких списков воспроизведения с одинаковыми именами, перед добавлением нового списка воспроизведения может потребоваться проверить, есть ли у него указанное имя.</span><span class="sxs-lookup"><span data-stu-id="e3e8d-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3e8d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e3e8d-123">Requirements</span></span>



| <span data-ttu-id="e3e8d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e3e8d-124">Requirement</span></span> | <span data-ttu-id="e3e8d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e3e8d-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e8d-126">Версия</span><span class="sxs-lookup"><span data-stu-id="e3e8d-126">Version</span></span><br/>   | <span data-ttu-id="e3e8d-127">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e3e8d-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e3e8d-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3e8d-128">Namespace</span></span><br/> | <span data-ttu-id="e3e8d-129">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="e3e8d-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e3e8d-130">Сборка</span><span class="sxs-lookup"><span data-stu-id="e3e8d-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e3e8d-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e3e8d-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3e8d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3e8d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e8d-133">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e3e8d-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3e8d-134">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e3e8d-134">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3e8d-135">**Ивмпплайлистколлектион. Импортплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e3e8d-135">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3e8d-136">**Ивмпплайлистколлектион. Невплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e3e8d-136">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





