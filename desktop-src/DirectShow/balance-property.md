---
description: Свойство Balance задает или получает баланс динамика для выходных данных аудиопотока.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Свойство Balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682314"
---
# <a name="balance-property"></a><span data-ttu-id="ff9a9-103">Свойство Balance</span><span class="sxs-lookup"><span data-stu-id="ff9a9-103">Balance Property</span></span>

> [!Note]  
> <span data-ttu-id="ff9a9-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ff9a9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ff9a9-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="ff9a9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ff9a9-106">`Balance`Свойство задает или получает баланс динамика для выходных данных аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="ff9a9-106">The `Balance` property sets or retrieves the speaker balance for the audio stream output.</span></span>

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a><span data-ttu-id="ff9a9-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff9a9-107">Return Value</span></span>

<span data-ttu-id="ff9a9-108">Возвращает целочисленное значение, представляющее уровни баланса.</span><span class="sxs-lookup"><span data-stu-id="ff9a9-108">Returns an integer value representing the balance levels.</span></span> <span data-ttu-id="ff9a9-109">Допустимый диапазон входных данных — от-10 000 до 10 000.</span><span class="sxs-lookup"><span data-stu-id="ff9a9-109">The allowable input range is -10,000 to 10,000.</span></span> <span data-ttu-id="ff9a9-110">Значение 0 задает нейтральный баланс, который и левый, и правый динамики получают один и тот же звуковой сигнал амплитуды.</span><span class="sxs-lookup"><span data-stu-id="ff9a9-110">A value of 0 sets a neutral balance, that is both left and right speakers are given the same amplitude audio signal.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff9a9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff9a9-111">Remarks</span></span>

<span data-ttu-id="ff9a9-112">Это свойство доступно для чтения и записи со значением по умолчанию 0, означающее, что оба динамика получают эквивалентные звуковые сигналы.</span><span class="sxs-lookup"><span data-stu-id="ff9a9-112">This property is read/write with a default value of 0, meaning that both speakers receive equivalent audio signals.</span></span> <span data-ttu-id="ff9a9-113">Как и свойство [**Volume**](volume-property.md) , единицы соответствуют .01 децибел (умноженному на-1, если</span><span class="sxs-lookup"><span data-stu-id="ff9a9-113">As with the [**Volume**](volume-property.md) property, units correspond to .01 decibels (multiplied by -1 when</span></span>


```
iBalance
```



<span data-ttu-id="ff9a9-114">является положительным значением).</span><span class="sxs-lookup"><span data-stu-id="ff9a9-114">is a positive value).</span></span> <span data-ttu-id="ff9a9-115">Например, значение 1000 указывает 10 баз данных в правильном канале и 90 dB в левом канале.</span><span class="sxs-lookup"><span data-stu-id="ff9a9-115">For example, a value of 1000 indicates 10 dB on the right channel and 90 dB on the left channel.</span></span>

 

 



