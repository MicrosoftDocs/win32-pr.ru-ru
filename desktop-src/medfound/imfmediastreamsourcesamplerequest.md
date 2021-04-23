---
description: Представляет запрос примера из Медиастреамсаурце.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Интерфейс Имфмедиастреамсаурцесамплерекуест
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351512"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a><span data-ttu-id="0d95b-103">Интерфейс Имфмедиастреамсаурцесамплерекуест</span><span class="sxs-lookup"><span data-stu-id="0d95b-103">IMFMediaStreamSourceSampleRequest interface</span></span>

<span data-ttu-id="0d95b-104">Представляет запрос примера из Медиастреамсаурце.</span><span class="sxs-lookup"><span data-stu-id="0d95b-104">Represents a request for a sample from a MediaStreamSource.</span></span>

## <a name="members"></a><span data-ttu-id="0d95b-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="0d95b-105">Members</span></span>

<span data-ttu-id="0d95b-106">Интерфейс **имфмедиастреамсаурцесамплерекуест** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0d95b-106">The **IMFMediaStreamSourceSampleRequest** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0d95b-107">**Имфмедиастреамсаурцесамплерекуест** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0d95b-107">**IMFMediaStreamSourceSampleRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="0d95b-108">Методы</span><span class="sxs-lookup"><span data-stu-id="0d95b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0d95b-109">Методы</span><span class="sxs-lookup"><span data-stu-id="0d95b-109">Methods</span></span>

<span data-ttu-id="0d95b-110">Интерфейс **имфмедиастреамсаурцесамплерекуест** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0d95b-110">The **IMFMediaStreamSourceSampleRequest** interface has these methods.</span></span>



| <span data-ttu-id="0d95b-111">Метод</span><span class="sxs-lookup"><span data-stu-id="0d95b-111">Method</span></span>                                                           | <span data-ttu-id="0d95b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0d95b-112">Description</span></span>                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="0d95b-113">**сетсампле**</span><span class="sxs-lookup"><span data-stu-id="0d95b-113">**SetSample**</span></span>](imfmediastreamsourcesamplerequest-setsample.md) | <span data-ttu-id="0d95b-114">Задает образец для источника потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0d95b-114">Sets the sample for the media stream source.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d95b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d95b-115">Remarks</span></span>

<span data-ttu-id="0d95b-116">**Мфмедиастреамсаурцесамплерекуест** реализуется классом среды выполнения [**Windows. Media. Core. медиастреамсаурцесамплерекуест**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="0d95b-116">**MFMediaStreamSourceSampleRequest** is implemented by the [**Windows.Media.Core.MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) runtime class.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d95b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0d95b-117">Requirements</span></span>



| <span data-ttu-id="0d95b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0d95b-118">Requirement</span></span> | <span data-ttu-id="0d95b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0d95b-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0d95b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d95b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d95b-121">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="0d95b-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0d95b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d95b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d95b-123">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="0d95b-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="0d95b-124">IDL</span><span class="sxs-lookup"><span data-stu-id="0d95b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d95b-125"><dt>Мфидл. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d95b-125"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d95b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d95b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d95b-127">Интерфейсы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d95b-127">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
