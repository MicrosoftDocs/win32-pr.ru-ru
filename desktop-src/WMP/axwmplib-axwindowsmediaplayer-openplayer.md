---
title: Аксвиндовсмедиаплайер. Опенплайер, метод
description: Метод Опенплайер открывает проигрыватель Windows Media с использованием указанного URL-адреса. | Аксвиндовсмедиаплайер. Опенплайер, метод
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- Опенплайер метод Windows Media Player
- Опенплайер метод Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, метод Опенплайер
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694734"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a><span data-ttu-id="b8f3e-107">Аксвиндовсмедиаплайер. Опенплайер, метод</span><span class="sxs-lookup"><span data-stu-id="b8f3e-107">AxWindowsMediaPlayer.openPlayer method</span></span>

<span data-ttu-id="b8f3e-108">Метод **опенплайер** открывает проигрыватель Windows Media с использованием указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f3e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8f3e-109">Syntax</span></span>


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="b8f3e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8f3e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f3e-111">*бструрл*</span><span class="sxs-lookup"><span data-stu-id="b8f3e-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f3e-112">**Строка System. String** , которая является URL-адресом элемента мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-112">The **System.String** that is the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f3e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8f3e-113">Return value</span></span>

<span data-ttu-id="b8f3e-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f3e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8f3e-115">Remarks</span></span>

<span data-ttu-id="b8f3e-116">Этот метод запускает проигрыватель Windows Media с указанным URL-адресом в качестве текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="b8f3e-117">Если проигрыватель был ранее закрыт в режиме обложки, он будет открыт с использованием обложки, последней выбранной пользователем.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="b8f3e-118">В противном случае проигрыватель откроется в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="b8f3e-118">Otherwise, the Player opens in full mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f3e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b8f3e-119">Requirements</span></span>



| <span data-ttu-id="b8f3e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b8f3e-120">Requirement</span></span> | <span data-ttu-id="b8f3e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b8f3e-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f3e-122">Версия</span><span class="sxs-lookup"><span data-stu-id="b8f3e-122">Version</span></span><br/>   | <span data-ttu-id="b8f3e-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b8f3e-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b8f3e-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b8f3e-124">Namespace</span></span><br/> | <span data-ttu-id="b8f3e-125">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="b8f3e-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b8f3e-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="b8f3e-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b8f3e-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b8f3e-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8f3e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8f3e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f3e-129">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b8f3e-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





