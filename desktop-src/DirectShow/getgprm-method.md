---
description: Метод Жетгпрм извлекает указанный общий регистр параметров.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Метод Жетгпрм
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537886"
---
# <a name="getgprm-method"></a><span data-ttu-id="1f42d-103">Метод Жетгпрм</span><span class="sxs-lookup"><span data-stu-id="1f42d-103">GetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="1f42d-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1f42d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1f42d-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="1f42d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1f42d-106">`GetGPRM`Метод получает указанный общий регистр параметров.</span><span class="sxs-lookup"><span data-stu-id="1f42d-106">The `GetGPRM` method retrieves the specified general parameter register.</span></span>

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="1f42d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f42d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f42d-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*ииндекс*</span><span class="sxs-lookup"><span data-stu-id="1f42d-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="1f42d-109">Указывает регистр для извлечения в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="1f42d-109">Specifies the register to retrieve as an Integer.</span></span> <span data-ttu-id="1f42d-110">Значение должно находиться в диапазоне от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="1f42d-110">The value must range from 0 through 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f42d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f42d-111">Return Value</span></span>

<span data-ttu-id="1f42d-112">Возвращает целочисленное значение, представляющее указанный регистр.</span><span class="sxs-lookup"><span data-stu-id="1f42d-112">Returns an integer value representing the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f42d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f42d-113">Remarks</span></span>

<span data-ttu-id="1f42d-114">Этот метод не требуется для навигации или воспроизведения DVD с помощью объекта **мсвебдвд** .</span><span class="sxs-lookup"><span data-stu-id="1f42d-114">This method is not required for any DVD navigation or playback functionality using the **MSWebDVD** object.</span></span> <span data-ttu-id="1f42d-115">Он предоставляется для тех, кто хорошо знаком со спецификацией DVD, которые хотят реализовать дополнительные функции.</span><span class="sxs-lookup"><span data-stu-id="1f42d-115">It is provided for those with a thorough understanding of the DVD specification who want to implement advanced features.</span></span> <span data-ttu-id="1f42d-116">Гпрмс можно использовать для хранения любых значений, поэтому их можно свободно задавать и считывать.</span><span class="sxs-lookup"><span data-stu-id="1f42d-116">GPRMs can be used to hold any values, so they can be freely set and read.</span></span> <span data-ttu-id="1f42d-117">Но поскольку Гпрмс используются для хранения команд диска, изменение их значений с помощью [**сетгпрм**](setgprm-method.md) может привести к непредсказуемому поведению.</span><span class="sxs-lookup"><span data-stu-id="1f42d-117">But since GPRMs are used to store disc commands as well, changing their values using [**SetGPRM**](setgprm-method.md) can result in unpredictable behavior.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f42d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f42d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f42d-119">**сетгпрм**</span><span class="sxs-lookup"><span data-stu-id="1f42d-119">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



