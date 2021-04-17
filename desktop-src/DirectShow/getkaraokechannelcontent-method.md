---
description: Метод Жеткараокечаннелконтент извлекает значение, указывающее тип содержимого в указанном канале караоке в указанном потоке.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Метод Жеткараокечаннелконтент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673027"
---
# <a name="getkaraokechannelcontent-method"></a><span data-ttu-id="cb3de-103">Метод Жеткараокечаннелконтент</span><span class="sxs-lookup"><span data-stu-id="cb3de-103">GetKaraokeChannelContent Method</span></span>

> [!Note]  
> <span data-ttu-id="cb3de-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cb3de-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cb3de-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="cb3de-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cb3de-106">`GetKaraokeChannelContent`Метод получает значение, указывающее тип содержимого в указанном канале караоке в указанном потоке.</span><span class="sxs-lookup"><span data-stu-id="cb3de-106">The `GetKaraokeChannelContent` method retrieves a value that indicates the type of content in the specified karaoke channel in the specified stream.</span></span>

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a><span data-ttu-id="cb3de-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb3de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb3de-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="cb3de-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="cb3de-109">Задает аудиопоток в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="cb3de-109">Specifies the audio stream as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="cb3de-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span><span class="sxs-lookup"><span data-stu-id="cb3de-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span></span>
</dt> <dd>

<span data-ttu-id="cb3de-111">Указывает канал в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="cb3de-111">Specifies the channel as an Integer.</span></span> <span data-ttu-id="cb3de-112">Возможные значения для каждого канала:</span><span class="sxs-lookup"><span data-stu-id="cb3de-112">The possible values for each channel are:</span></span>



| <span data-ttu-id="cb3de-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cb3de-113">Value</span></span>  | <span data-ttu-id="cb3de-114">Описание</span><span class="sxs-lookup"><span data-stu-id="cb3de-114">Description</span></span>    |
|--------|----------------|
| <span data-ttu-id="cb3de-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="cb3de-115">0x0001</span></span> | <span data-ttu-id="cb3de-116">Guide вокал 1</span><span class="sxs-lookup"><span data-stu-id="cb3de-116">Guide Vocal 1</span></span>  |
| <span data-ttu-id="cb3de-117">0x0002</span><span class="sxs-lookup"><span data-stu-id="cb3de-117">0x0002</span></span> | <span data-ttu-id="cb3de-118">Guide вокал 2</span><span class="sxs-lookup"><span data-stu-id="cb3de-118">Guide Vocal 2</span></span>  |
| <span data-ttu-id="cb3de-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="cb3de-119">0x0004</span></span> | <span data-ttu-id="cb3de-120">Guide Мелодия 1</span><span class="sxs-lookup"><span data-stu-id="cb3de-120">Guide Melody 1</span></span> |
| <span data-ttu-id="cb3de-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="cb3de-121">0x0008</span></span> | <span data-ttu-id="cb3de-122">Guide Мелодия 2</span><span class="sxs-lookup"><span data-stu-id="cb3de-122">Guide Melody 2</span></span> |
| <span data-ttu-id="cb3de-123">0x0010</span><span class="sxs-lookup"><span data-stu-id="cb3de-123">0x0010</span></span> | <span data-ttu-id="cb3de-124">Мелодия</span><span class="sxs-lookup"><span data-stu-id="cb3de-124">Guide Melody A</span></span> |
| <span data-ttu-id="cb3de-125">0x0020</span><span class="sxs-lookup"><span data-stu-id="cb3de-125">0x0020</span></span> | <span data-ttu-id="cb3de-126">Guide Мелодия B</span><span class="sxs-lookup"><span data-stu-id="cb3de-126">Guide Melody B</span></span> |
| <span data-ttu-id="cb3de-127">0x0040</span><span class="sxs-lookup"><span data-stu-id="cb3de-127">0x0040</span></span> | <span data-ttu-id="cb3de-128">Звуковой результат A</span><span class="sxs-lookup"><span data-stu-id="cb3de-128">Sound Effect A</span></span> |
| <span data-ttu-id="cb3de-129">0x0080</span><span class="sxs-lookup"><span data-stu-id="cb3de-129">0x0080</span></span> | <span data-ttu-id="cb3de-130">Звуковой результат б</span><span class="sxs-lookup"><span data-stu-id="cb3de-130">Sound Effect B</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb3de-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb3de-131">Return Value</span></span>

<span data-ttu-id="cb3de-132">Возвращает целочисленное значение, отдельные биты которого задают содержимое канала караоке.</span><span class="sxs-lookup"><span data-stu-id="cb3de-132">Returns an integer value whose individual bits specify the contents of the karaoke channel.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3de-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb3de-133">Remarks</span></span>

<span data-ttu-id="cb3de-134">Нумерация видеоканалов DVD отсчитывается от нуля, поэтому каналы 2, 3 и 4 являются вспомогательными каналами караоке.</span><span class="sxs-lookup"><span data-stu-id="cb3de-134">DVD audio channel numbering is zero-based, so channels 2, 3, and 4 are the auxiliary karaoke channels.</span></span> <span data-ttu-id="cb3de-135">После возврата метода выполните операцию побитового и для *иконтент* , чтобы определить содержимое каждого канала.</span><span class="sxs-lookup"><span data-stu-id="cb3de-135">After the method returns, perform a bitwise AND operation on *iContent* to determine the contents of each channel.</span></span> <span data-ttu-id="cb3de-136">Так как на одном канале может быть записано несколько типов содержимого, следует проверить все возможные значения даже после обнаружения совпадения.</span><span class="sxs-lookup"><span data-stu-id="cb3de-136">Because a single channel might have more than one type of content recorded on it, you should test for all the possible values even after a match is found.</span></span>

<span data-ttu-id="cb3de-137">После того как пользователь знает содержимое каждого канала, он должен иметь возможность настраивать том или включать или отключать отдельные каналы по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="cb3de-137">After the user knows the contents of each channel, he or she must be able to adjust the volume or turn the individual channels on or off as needed.</span></span> <span data-ttu-id="cb3de-138">Реализуйте эту функцию в приложении с помощью свойства [**караокеаудиопресентатионмоде**](karaokeaudiopresentationmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="cb3de-138">Implement this functionality in your application by using the [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="cb3de-139">Для воспроизведения дисков караоке декодер аудио в системе пользователя должен быть совместим с реализацией DirectShow 8 караоке.</span><span class="sxs-lookup"><span data-stu-id="cb3de-139">To play karaoke discs, the audio decoder on the user's system must be compatible with the DirectShow 8 karaoke implementation.</span></span>

 

 

 



