---
title: Аксвиндовсмедиаплайер. Кдромколлектион, свойство
description: Свойство Кдромколлектион получает интерфейс Ивмпкдромколлектион, предоставляющий доступ к коллекции компакт-дисков или DVD-дисководов.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- Проигрыватель Windows Media для свойства Кдромколлектион
- Кдромколлектион свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Кдромколлектион
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694386"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a><span data-ttu-id="c41c3-106">Аксвиндовсмедиаплайер. Кдромколлектион, свойство</span><span class="sxs-lookup"><span data-stu-id="c41c3-106">AxWindowsMediaPlayer.cdromCollection property</span></span>

<span data-ttu-id="c41c3-107">Свойство Кдромколлектион получает интерфейс **ивмпкдромколлектион** , предоставляющий доступ к коллекции компакт-дисков или DVD-дисководов.</span><span class="sxs-lookup"><span data-stu-id="c41c3-107">The cdromCollection property gets an **IWMPCdromCollection** interface that provides access to a collection of CD or DVD drives.</span></span>

<span data-ttu-id="c41c3-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c41c3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c41c3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c41c3-109">Syntax</span></span>


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a><span data-ttu-id="c41c3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c41c3-110">Property value</span></span>

<span data-ttu-id="c41c3-111">Интерфейс Вмплиб. Ивмпкдромколлектион.</span><span class="sxs-lookup"><span data-stu-id="c41c3-111">A WMPLib.IWMPCdromCollection interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="c41c3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c41c3-112">Remarks</span></span>

<span data-ttu-id="c41c3-113">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="c41c3-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="c41c3-114">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c41c3-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c41c3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c41c3-115">Requirements</span></span>



| <span data-ttu-id="c41c3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c41c3-116">Requirement</span></span> | <span data-ttu-id="c41c3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c41c3-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c41c3-118">Версия</span><span class="sxs-lookup"><span data-stu-id="c41c3-118">Version</span></span><br/>   | <span data-ttu-id="c41c3-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c41c3-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c41c3-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c41c3-120">Namespace</span></span><br/> | <span data-ttu-id="c41c3-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="c41c3-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c41c3-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="c41c3-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c41c3-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c41c3-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c41c3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c41c3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c41c3-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c41c3-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c41c3-126">**Интерфейс Ивмпкдромколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c41c3-126">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c41c3-127">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c41c3-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c41c3-128">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c41c3-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





