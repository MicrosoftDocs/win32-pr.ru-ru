---
title: Ивмпсеттингс, свойство тома
description: Свойство Volume получает или задает текущий том воспроизведения.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Проигрыватель Windows Media, свойство тома
- Свойство тома проигрыватель Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство Volume
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685270"
---
# <a name="iwmpsettingsvolume-property"></a><span data-ttu-id="6f3d6-106">Свойство Ивмпсеттингс:: Volume</span><span class="sxs-lookup"><span data-stu-id="6f3d6-106">IWMPSettings::volume property</span></span>

<span data-ttu-id="6f3d6-107">Свойство **Volume** получает или задает текущий том воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-107">The **volume** property gets or sets the current playback volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f3d6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f3d6-108">Syntax</span></span>


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="6f3d6-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6f3d6-109">Property value</span></span>

<span data-ttu-id="6f3d6-110">Объект **System. Int32** , который является уровнем громкости в диапазоне от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-110">A **System.Int32** that is the volume level, ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f3d6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f3d6-111">Remarks</span></span>

<span data-ttu-id="6f3d6-112">Нулевое значение указывает на отсутствие тома (без звука).</span><span class="sxs-lookup"><span data-stu-id="6f3d6-112">A value of zero specifies no volume (muted).</span></span> <span data-ttu-id="6f3d6-113">Значение 100 указывает полный том.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-113">A value of 100 specifies full volume.</span></span> <span data-ttu-id="6f3d6-114">Если для этого свойства не указано значение, по умолчанию используется последний параметр тома, установленный для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6f3d6-114">If no value is specified for this property, it defaults to the last volume setting established for Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f3d6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6f3d6-115">Requirements</span></span>



| <span data-ttu-id="6f3d6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6f3d6-116">Requirement</span></span> | <span data-ttu-id="6f3d6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6f3d6-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f3d6-118">Версия</span><span class="sxs-lookup"><span data-stu-id="6f3d6-118">Version</span></span><br/>   | <span data-ttu-id="6f3d6-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6f3d6-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6f3d6-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6f3d6-120">Namespace</span></span><br/> | <span data-ttu-id="6f3d6-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="6f3d6-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6f3d6-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="6f3d6-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6f3d6-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6f3d6-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f3d6-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f3d6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f3d6-125">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6f3d6-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





