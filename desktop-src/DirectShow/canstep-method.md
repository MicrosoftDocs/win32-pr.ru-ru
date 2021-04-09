---
description: Метод Канстеп определяет, может ли декодер MPEG-2 в локальной системе выполнять пошаговое выполнение кадра в указанном направлении.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Метод Канстеп
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072173"
---
# <a name="canstep-method"></a><span data-ttu-id="79c10-103">Метод Канстеп</span><span class="sxs-lookup"><span data-stu-id="79c10-103">CanStep Method</span></span>

> [!Note]  
> <span data-ttu-id="79c10-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="79c10-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="79c10-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="79c10-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="79c10-106">`CanStep`Метод определяет, может ли декодер MPEG-2 в локальной системе выполнять пошаговое выполнение кадра в указанном направлении.</span><span class="sxs-lookup"><span data-stu-id="79c10-106">The `CanStep` method determines whether the MPEG-2 decoder on the local system can perform frame stepping in a specified direction.</span></span>

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a><span data-ttu-id="79c10-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="79c10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79c10-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*бдиректион*</span><span class="sxs-lookup"><span data-stu-id="79c10-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span></span>
</dt> <dd>

<span data-ttu-id="79c10-109">Логическое значение, используемое в качестве флага для указания направления (вперед или назад) возможностей пошагового выполнения декодера.</span><span class="sxs-lookup"><span data-stu-id="79c10-109">Boolean used as a flag to specify the direction, forward or backward, of decoder's frame-stepping ability.</span></span>



| <span data-ttu-id="79c10-110">Значение</span><span class="sxs-lookup"><span data-stu-id="79c10-110">Value</span></span> | <span data-ttu-id="79c10-111">Описание</span><span class="sxs-lookup"><span data-stu-id="79c10-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="79c10-112">true</span><span class="sxs-lookup"><span data-stu-id="79c10-112">true</span></span>  | <span data-ttu-id="79c10-113">Можно ли дедекодерировать шаг назад?</span><span class="sxs-lookup"><span data-stu-id="79c10-113">Can decoder step backward?</span></span>                           |
| <span data-ttu-id="79c10-114">false</span><span class="sxs-lookup"><span data-stu-id="79c10-114">false</span></span> | <span data-ttu-id="79c10-115">Можно ли отдекодеровать шаг вперед?</span><span class="sxs-lookup"><span data-stu-id="79c10-115">Can decoder step forward?</span></span> <span data-ttu-id="79c10-116">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79c10-116">This is the default value.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79c10-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79c10-117">Return Value</span></span>

<span data-ttu-id="79c10-118">Возвращает логическое значение true, если декодер может выполнить шаг в указанном направлении, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="79c10-118">Returns a Boolean value of true if the decoder can step in the specified direction, and false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="79c10-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79c10-119">Remarks</span></span>

<span data-ttu-id="79c10-120">Не все аппаратные декодеры MPEG-2 поддерживают новые возможности пошагового выполнения пакетов в DirectShow® 8,0.</span><span class="sxs-lookup"><span data-stu-id="79c10-120">Not all hardware MPEG-2 decoders support the new frame stepping capabilities in DirectShow® 8.0.</span></span> <span data-ttu-id="79c10-121">Этот метод запрашивает у декодера возможности пошагового выполнения кадра.</span><span class="sxs-lookup"><span data-stu-id="79c10-121">This method queries the decoder for its frame stepping capabilities.</span></span> <span data-ttu-id="79c10-122">Если декодер может выполнять пошаговое выполнение, приложение может использовать метод [**Step**](step-method.md) для пошагового перехода к кадрам.</span><span class="sxs-lookup"><span data-stu-id="79c10-122">If the decoder can perform frame stepping, an application can use the [**Step**](step-method.md) method to step through frames.</span></span> <span data-ttu-id="79c10-123">Этот метод всегда будет возвращать **значение true** , если используется программный декодер.</span><span class="sxs-lookup"><span data-stu-id="79c10-123">This method will always return **true** if a software decoder is being used.</span></span>

 

 



