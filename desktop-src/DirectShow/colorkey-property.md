---
description: Свойство ColorKey задает или получает цветовой ключ, используемый в закрытых субтитрах.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: ColorKey, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494637"
---
# <a name="colorkey-property"></a><span data-ttu-id="a9207-103">ColorKey, свойство</span><span class="sxs-lookup"><span data-stu-id="a9207-103">ColorKey Property</span></span>

> [!Note]  
> <span data-ttu-id="a9207-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a9207-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a9207-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="a9207-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a9207-106">`ColorKey`Свойство задает или получает цветовой ключ, используемый в закрытых субтитрах.</span><span class="sxs-lookup"><span data-stu-id="a9207-106">The `ColorKey` property sets or retrieves the color key used in closed captioning.</span></span>

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a><span data-ttu-id="a9207-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9207-107">Return Value</span></span>

<span data-ttu-id="a9207-108">Возвращает целочисленное значение, представляющее цвет, используемый в качестве прозрачного фона для текста с субтитрами.</span><span class="sxs-lookup"><span data-stu-id="a9207-108">Returns an integer value representing the color to use as a transparent background for closed-captioned text.</span></span> <span data-ttu-id="a9207-109">Значение по умолчанию в 256 Colors — пурпурный, а «выкл.-черный» — в любой другой глубине цвета.</span><span class="sxs-lookup"><span data-stu-id="a9207-109">The default value in 256 colors is magenta, and off-black in any other color depth.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9207-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9207-110">Remarks</span></span>

<span data-ttu-id="a9207-111">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a9207-111">This property is read/write.</span></span> <span data-ttu-id="a9207-112">Это свойство применяется только к закрытым заголовкам, если таковые существуют, а не к потоку субтитров.</span><span class="sxs-lookup"><span data-stu-id="a9207-112">This property applies only to the closed-captions, if any exist, not to the subpicture stream.</span></span>

 

 



