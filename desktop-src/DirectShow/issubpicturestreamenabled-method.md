---
description: Метод Иссубпиктурестреаменаблед извлекает значение, указывающее, включен ли указанный поток субтитров в текущем заголовке.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Метод Иссубпиктурестреаменаблед
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894993"
---
# <a name="issubpicturestreamenabled-method"></a><span data-ttu-id="2ce6c-103">Метод Иссубпиктурестреаменаблед</span><span class="sxs-lookup"><span data-stu-id="2ce6c-103">IsSubpictureStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="2ce6c-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2ce6c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2ce6c-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="2ce6c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2ce6c-106">`IsSubpictureStreamEnabled`Метод получает значение, указывающее, включен ли указанный поток субтитров в текущем заголовке.</span><span class="sxs-lookup"><span data-stu-id="2ce6c-106">The `IsSubpictureStreamEnabled` method retrieves a value indicating whether the specified subpicture stream is enabled in the current title.</span></span>

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="2ce6c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ce6c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce6c-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="2ce6c-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="2ce6c-109">Указывает поток субтитров в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="2ce6c-109">Specifies the subpicture stream as an Integer.</span></span>



| <span data-ttu-id="2ce6c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2ce6c-110">Value</span></span>   | <span data-ttu-id="2ce6c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2ce6c-111">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="2ce6c-112">от 0 до 31</span><span class="sxs-lookup"><span data-stu-id="2ce6c-112">0 to 31</span></span> | <span data-ttu-id="2ce6c-113">поток субтитров</span><span class="sxs-lookup"><span data-stu-id="2ce6c-113">subpicture stream</span></span>        |
| <span data-ttu-id="2ce6c-114">63</span><span class="sxs-lookup"><span data-stu-id="2ce6c-114">63</span></span>      | <span data-ttu-id="2ce6c-115">выключение потока с низкой скоростью</span><span class="sxs-lookup"><span data-stu-id="2ce6c-115">muted low-bitrate stream</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce6c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ce6c-116">Return Value</span></span>

<span data-ttu-id="2ce6c-117">Возвращает логическое значение, указывающее, доступен ли указанный звуковой поток в текущем заголовке.</span><span class="sxs-lookup"><span data-stu-id="2ce6c-117">Returns a Boolean value indicating whether the specified audio stream is available in the current title.</span></span> <span data-ttu-id="2ce6c-118">Значение true означает, что он доступен.</span><span class="sxs-lookup"><span data-stu-id="2ce6c-118">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce6c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ce6c-119">Remarks</span></span>

<span data-ttu-id="2ce6c-120">Хотя диск может содержать до 32 потоков подизображений, каждый поток необязательно доступен для каждого заголовка.</span><span class="sxs-lookup"><span data-stu-id="2ce6c-120">Although a disc can contain up to 32 subpicture streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="2ce6c-121">Перед установкой свойства [**куррентсубпиктурестреам**](currentsubpicturestream-property.md) всегда проверяйте, что поток доступен для заголовка.</span><span class="sxs-lookup"><span data-stu-id="2ce6c-121">Always verify that a stream is available for a title before setting the [**CurrentSubpictureStream**](currentsubpicturestream-property.md) property.</span></span>

 

 



