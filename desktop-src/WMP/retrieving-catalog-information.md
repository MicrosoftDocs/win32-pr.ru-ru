---
title: Получение сведений о каталоге
description: Получение сведений о каталоге
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Интернет-магазины проигрывателя Windows Media, получение сведений о каталоге
- Интернет-магазины, получение сведений о каталоге
- Тип 1 Интернет-магазины, получение сведений о каталоге
- Интернет-магазины проигрывателя Windows Media, диагностические сведения о каталогах
- Интернет-магазины, диагностические сведения о каталогах
- Тип 1 Интернет-магазины, диагностические сведения о каталогах
- Интернет-магазины проигрывателя Windows Media, catcomp.exe
- Интернет-магазины, catcomp.exe
- Введите 1 Интернет-магазины, catcomp.exe
- catcomp.exe
- диагностические сведения о каталогах
- получение сведений о каталоге
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721d6ba3e4d6b5106cf44446d4c96ed842ccd61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778263"
---
# <a name="retrieving-catalog-information"></a><span data-ttu-id="fb677-115">Получение сведений о каталоге</span><span class="sxs-lookup"><span data-stu-id="fb677-115">Retrieving Catalog Information</span></span>

<span data-ttu-id="fb677-116">Вы можете отобразить диагностическую информацию в каталоге, запустив каткомп со следующим синтаксисом:</span><span class="sxs-lookup"><span data-stu-id="fb677-116">You can display diagnostic information on a catalog by running catcomp with the following syntax:</span></span>


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



<span data-ttu-id="fb677-117">Например, следующая команда отображает сведения обо всем каталоге, включая версию, языковой стандарт и внутреннюю информацию по элементам каталога:</span><span class="sxs-lookup"><span data-stu-id="fb677-117">For example, the following command displays information on an entire catalog, including the version, locale, and internal information on catalog items:</span></span>


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



<span data-ttu-id="fb677-118">Ниже отображаются сведения о дорожке с ИДЕНТИФИКАТОРом 3256:</span><span class="sxs-lookup"><span data-stu-id="fb677-118">The following displays information for the track with ID 3256:</span></span>


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




