---
description: Свойство Куррентсубпиктурестреам задает или получает текущий поток субтитров.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Куррентсубпиктурестреам, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538078"
---
# <a name="currentsubpicturestream-property"></a><span data-ttu-id="dd9d5-103">Куррентсубпиктурестреам, свойство</span><span class="sxs-lookup"><span data-stu-id="dd9d5-103">CurrentSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="dd9d5-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dd9d5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dd9d5-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="dd9d5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dd9d5-106">`CurrentSubpictureStream`Свойство задает или получает текущий поток субтитров.</span><span class="sxs-lookup"><span data-stu-id="dd9d5-106">The `CurrentSubpictureStream` property sets or retrieves the current subpicture stream.</span></span>

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="dd9d5-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd9d5-107">Return Value</span></span>

<span data-ttu-id="dd9d5-108">Возвращает целочисленное значение, представляющее поток.</span><span class="sxs-lookup"><span data-stu-id="dd9d5-108">Returns an integer value representing the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd9d5-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd9d5-109">Remarks</span></span>

<span data-ttu-id="dd9d5-110">Возможные значения этого свойства:</span><span class="sxs-lookup"><span data-stu-id="dd9d5-110">The possible values of this property are:</span></span>



| <span data-ttu-id="dd9d5-111">Значение</span><span class="sxs-lookup"><span data-stu-id="dd9d5-111">Value</span></span>   | <span data-ttu-id="dd9d5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="dd9d5-112">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="dd9d5-113">от 0 до 31</span><span class="sxs-lookup"><span data-stu-id="dd9d5-113">0 to 31</span></span> | <span data-ttu-id="dd9d5-114">Поток субтитров</span><span class="sxs-lookup"><span data-stu-id="dd9d5-114">The subpicture stream</span></span>    |
| <span data-ttu-id="dd9d5-115">63</span><span class="sxs-lookup"><span data-stu-id="dd9d5-115">63</span></span>      | <span data-ttu-id="dd9d5-116">Выключение потока с низкой скоростью</span><span class="sxs-lookup"><span data-stu-id="dd9d5-116">Muted low-bitrate stream</span></span> |



 

<span data-ttu-id="dd9d5-117">Это свойство доступно для чтения и записи и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dd9d5-117">This property is read/write with no default value.</span></span> <span data-ttu-id="dd9d5-118">Перед настройкой нового потока субтитров вызовите [**иссубпиктурестреаменаблед**](issubpicturestreamenabled-method.md) , чтобы убедиться, что поток доступен.</span><span class="sxs-lookup"><span data-stu-id="dd9d5-118">Before setting a new subpicture stream, call [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) to verify that the stream is available.</span></span>

<span data-ttu-id="dd9d5-119">Установка этого свойства приводит к тому, что свойство [**субпиктуреон**](subpictureon-property.md) переключается в **true**.</span><span class="sxs-lookup"><span data-stu-id="dd9d5-119">Setting this property causes the [**SubpictureOn**](subpictureon-property.md) property to toggle to **True**.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd9d5-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd9d5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd9d5-121">**субпиктуреон**</span><span class="sxs-lookup"><span data-stu-id="dd9d5-121">**SubpictureOn**</span></span>](subpictureon-property.md)
</dt> <dt>

[<span data-ttu-id="dd9d5-122">**субпиктурестреамсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="dd9d5-122">**SubpictureStreamsAvailable**</span></span>](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



