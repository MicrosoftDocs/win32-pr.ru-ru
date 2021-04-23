---
title: Аксвиндовсмедиаплайер. Close, метод
description: Метод Close закрывает текущий файл мультимедиа, останавливает воспроизведение в проигрывателе Windows Media и освобождает ресурсы проигрывателя Windows Media.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- закрыть метод проигрыватель Windows Media Player
- закрыть метод проигрыватель Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер проигрыватель Windows Media Player, метод Close
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694908"
---
# <a name="axwindowsmediaplayerclose-method"></a><span data-ttu-id="1cce3-106">Аксвиндовсмедиаплайер. Close, метод</span><span class="sxs-lookup"><span data-stu-id="1cce3-106">AxWindowsMediaPlayer.close method</span></span>

<span data-ttu-id="1cce3-107">Метод Close закрывает текущий файл мультимедиа, останавливает воспроизведение в проигрывателе Windows Media и освобождает ресурсы проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1cce3-107">The close method closes the current digital media file, stops playback in Windows Media Player and releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cce3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cce3-108">Syntax</span></span>


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a><span data-ttu-id="1cce3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cce3-109">Parameters</span></span>

<span data-ttu-id="1cce3-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1cce3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cce3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cce3-111">Return value</span></span>

<span data-ttu-id="1cce3-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1cce3-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cce3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1cce3-113">Remarks</span></span>

<span data-ttu-id="1cce3-114">Этот метод закрывает текущий файл мультимедиа, а не проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1cce3-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="1cce3-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="1cce3-115">Examples</span></span>

<span data-ttu-id="1cce3-116">В следующем примере создается кнопка, которая при нажатии останавливает воспроизведение в проигрывателе Windows Media и освобождает используемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="1cce3-116">The following example creates a button that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="1cce3-117">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="1cce3-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1cce3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1cce3-118">Requirements</span></span>



| <span data-ttu-id="1cce3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1cce3-119">Requirement</span></span> | <span data-ttu-id="1cce3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1cce3-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cce3-121">Версия</span><span class="sxs-lookup"><span data-stu-id="1cce3-121">Version</span></span><br/>   | <span data-ttu-id="1cce3-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1cce3-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="1cce3-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1cce3-123">Namespace</span></span><br/> | <span data-ttu-id="1cce3-124">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="1cce3-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1cce3-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="1cce3-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1cce3-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1cce3-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cce3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1cce3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cce3-128">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="1cce3-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





