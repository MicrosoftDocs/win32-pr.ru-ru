---
description: Свойство Двддиректори задает или получает текущий каталог текущего тома DVD.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Двддиректори, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894697"
---
# <a name="dvddirectory-property"></a><span data-ttu-id="77194-103">Двддиректори, свойство</span><span class="sxs-lookup"><span data-stu-id="77194-103">DVDDirectory Property</span></span>

> [!Note]  
> <span data-ttu-id="77194-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="77194-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="77194-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="77194-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="77194-106">`DVDDirectory`Свойство задает или получает текущий каталог текущего тома DVD.</span><span class="sxs-lookup"><span data-stu-id="77194-106">The `DVDDirectory` property sets or retrieves the current directory of the current DVD volume.</span></span>

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a><span data-ttu-id="77194-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77194-107">Return Value</span></span>

<span data-ttu-id="77194-108">Возвращает строковое значение, указывающее путь к корневому каталогу DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="77194-108">Returns a string value indicating the path to the DVD root directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="77194-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77194-109">Remarks</span></span>

<span data-ttu-id="77194-110">Это свойство доступно для чтения и записи и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="77194-110">This property is read/write with no default value.</span></span> <span data-ttu-id="77194-111">Используйте этот метод, чтобы задать корневой путь при наличии нескольких DVD-дисководов в системе.</span><span class="sxs-lookup"><span data-stu-id="77194-111">Use this method to set the root path when there is more than one DVD drive on a system.</span></span> <span data-ttu-id="77194-112">Если в системе только один диск и буква диска выше "C", объект Мсвебдвд находит его автоматически.</span><span class="sxs-lookup"><span data-stu-id="77194-112">When there is only one drive on the system and its drive letter is higher than "C", the MSWebDVD object finds it automatically.</span></span> <span data-ttu-id="77194-113">Для стандартного DVD-Video диска корневой путь должен включать в себя \_ Каталог видео служб терминалов:</span><span class="sxs-lookup"><span data-stu-id="77194-113">For a standard DVD-Video disc, the root path should include the ts\_video directory:</span></span>


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



<span data-ttu-id="77194-114">Некоторые DVD-тома могут иметь видео в каталоге, отличном от "Video \_ TS".</span><span class="sxs-lookup"><span data-stu-id="77194-114">Some DVD volumes may have their video in a directory named something other than "video\_ts."</span></span> <span data-ttu-id="77194-115">Общая идея состоит в том, что дополнительный "том DVD" (набор. ИФО.</span><span class="sxs-lookup"><span data-stu-id="77194-115">The general idea is that an additional "DVD volume" (the set of .IFO.</span></span> <span data-ttu-id="77194-116">VOB и. Файлы БУП, которые обычно хранятся в \_ каталоге Video TS), можно поместить в подкаталог на диске. Если изменить корень так, чтобы он указывал на этот каталог, Мсвебдвд будет выполнять действия на этом отдельном томе DVD.</span><span class="sxs-lookup"><span data-stu-id="77194-116">VOB, and .BUP files that would normally be stored in the VIDEO\_TS directory) can be placed in a subdirectory on the disc. By changing the root to point to this directory, MSWebDVD will operate on this separate DVD volume.</span></span> <span data-ttu-id="77194-117">Будет доступен новый набор меню, заголовков и т. д., не зависящий от заголовков в \_ корневом каталоге служб Video TS, который больше не будет доступен.</span><span class="sxs-lookup"><span data-stu-id="77194-117">A new set of menus, titles, and so on will be available, independent of the titles in the VIDEO\_TS root, which will no longer be accessible.</span></span> <span data-ttu-id="77194-118">Такие каталоги называются "скрытыми каталогами".</span><span class="sxs-lookup"><span data-stu-id="77194-118">Such directories are called "hidden directories."</span></span> <span data-ttu-id="77194-119">В следующем примере показано, как задать скрытый каталог в качестве корневого, где "Hidden" — это заполнитель для любого имени, которое авторы диска задали в каталоге.</span><span class="sxs-lookup"><span data-stu-id="77194-119">The following example shows how to set a hidden directory as the root, where "hidden" is a placeholder for whatever name the disc authors have given to the directory.</span></span>


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



