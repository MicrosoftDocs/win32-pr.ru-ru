---
title: IWMPMedia2, свойство ошибки
description: Свойство Error получает интерфейс Ивмперроритем, если в элементе мультимедиа есть условие ошибки.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Проигрыватель Windows Media, свойство ошибки
- Свойство ошибки Windows Media Player, интерфейс IWMPMedia2
- Интерфейс IWMPMedia2 Windows Media Player, свойство Error
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665108"
---
# <a name="iwmpmedia2error-property"></a><span data-ttu-id="d09ac-106">Свойство IWMPMedia2:: Error</span><span class="sxs-lookup"><span data-stu-id="d09ac-106">IWMPMedia2::Error property</span></span>

<span data-ttu-id="d09ac-107">Свойство **Error** получает интерфейс **ивмперроритем** , если в элементе мультимедиа есть условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="d09ac-107">The **Error** property gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span>

<span data-ttu-id="d09ac-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d09ac-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d09ac-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d09ac-109">Syntax</span></span>


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a><span data-ttu-id="d09ac-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d09ac-110">Property value</span></span>

<span data-ttu-id="d09ac-111">Интерфейс **вмплиб. ивмперроритем** , предоставляющий доступ к сведениям о состоянии ошибки.</span><span class="sxs-lookup"><span data-stu-id="d09ac-111">A **WMPLib.IWMPErrorItem** interface that provides access to information about the error condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="d09ac-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d09ac-112">Remarks</span></span>

<span data-ttu-id="d09ac-113">Если не удается воспроизвести элемент мультимедиа, это свойство получает интерфейс **ивмперроритем** , содержащий сведения о возникшей проблеме.</span><span class="sxs-lookup"><span data-stu-id="d09ac-113">If the media item cannot be played, this property gets an **IWMPErrorItem** interface that contains information about the problem encountered.</span></span>

## <a name="requirements"></a><span data-ttu-id="d09ac-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d09ac-114">Requirements</span></span>



| <span data-ttu-id="d09ac-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d09ac-115">Requirement</span></span> | <span data-ttu-id="d09ac-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d09ac-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d09ac-117">Версия</span><span class="sxs-lookup"><span data-stu-id="d09ac-117">Version</span></span><br/>   | <span data-ttu-id="d09ac-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d09ac-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d09ac-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d09ac-119">Namespace</span></span><br/> | <span data-ttu-id="d09ac-120">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="d09ac-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d09ac-121">Сборка</span><span class="sxs-lookup"><span data-stu-id="d09ac-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d09ac-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d09ac-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09ac-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d09ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09ac-124">**Ивмперроритем (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d09ac-124">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d09ac-125">**Интерфейс IWMPMedia2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d09ac-125">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





