---
description: Свойство Двдадм. ДефаултсубпиктурелЦид задает или получает параметр реестра для указанного пользователем кода языка по умолчанию для потока субтитров.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: ДефаултсубпиктурелЦид, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538240"
---
# <a name="defaultsubpicturelcid-property"></a><span data-ttu-id="f57ad-103">ДефаултсубпиктурелЦид, свойство</span><span class="sxs-lookup"><span data-stu-id="f57ad-103">DefaultSubpictureLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="f57ad-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f57ad-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f57ad-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f57ad-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f57ad-106">`DVDAdm.DefaultSubpictureLCID`Свойство задает или получает параметр реестра для указанного пользователем кода языка по умолчанию для потока субтитров.</span><span class="sxs-lookup"><span data-stu-id="f57ad-106">The `DVDAdm.DefaultSubpictureLCID` property sets or retrieves the registry setting for the user-specified default LCID for the subpicture stream.</span></span>

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a><span data-ttu-id="f57ad-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f57ad-107">Return Value</span></span>

<span data-ttu-id="f57ad-108">Возвращает целочисленное значение, представляющее указанный пользователем код языка по умолчанию, который хранится в параметрах реестра для приложения DVD.</span><span class="sxs-lookup"><span data-stu-id="f57ad-108">Returns an Integer value representing the user-specified default subpicture LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="f57ad-109">Это значение не обязательно соответствует потоку субтитров по умолчанию, созданному на DVD-диске.</span><span class="sxs-lookup"><span data-stu-id="f57ad-109">This value is not necessarily the same as the default subpicture stream as authored on the DVD.</span></span> <span data-ttu-id="f57ad-110">Диапазон допустимых кодов языка см. в документации по Win32 в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="f57ad-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f57ad-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f57ad-111">Remarks</span></span>

<span data-ttu-id="f57ad-112">Это свойство доступно для чтения и записи и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f57ad-112">This property is read/write with no default value.</span></span> <span data-ttu-id="f57ad-113">Если не указан LCID по умолчанию, объект Мсдвдадм будет воспроизводить поток субтитров, помеченный как поток по умолчанию на диске.</span><span class="sxs-lookup"><span data-stu-id="f57ad-113">If no default subpicture LCID is specified, the MSDVDAdm object will play the subpicture stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="f57ad-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f57ad-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f57ad-115">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="f57ad-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



