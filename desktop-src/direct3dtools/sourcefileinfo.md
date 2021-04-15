---
description: Представляет сведения о файле исходного кода.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Саурцефилеинфо
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495246"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span data-ttu-id="830e6-103"><span id="vspixengine.sourcefileinfo"></span>Структура Саурцефилеинфо</span><span class="sxs-lookup"><span data-stu-id="830e6-103"><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo structure</span></span>

<span data-ttu-id="830e6-104">Представляет сведения о файле исходного кода.</span><span class="sxs-lookup"><span data-stu-id="830e6-104">Represents information about a source code file.</span></span>

## <a name="syntax"></a><span data-ttu-id="830e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="830e6-105">Syntax</span></span>


```C++
} SourceFileInfo;
```

## <a name="members"></a><span data-ttu-id="830e6-106">Члены</span><span class="sxs-lookup"><span data-stu-id="830e6-106">Members</span></span>

<span data-ttu-id="830e6-107">**Файлов**</span><span class="sxs-lookup"><span data-stu-id="830e6-107">**fileName**</span></span>  
<span data-ttu-id="830e6-108">Строка COM, комтаининг путь к файлу для связанного исходного файла.</span><span class="sxs-lookup"><span data-stu-id="830e6-108">A COM string comtaining the filepath of the associated source file.</span></span>

<span data-ttu-id="830e6-109">**чекксумбитекаунт**</span><span class="sxs-lookup"><span data-stu-id="830e6-109">**checksumByteCount**</span></span>  
<span data-ttu-id="830e6-110">Число байтов в контрольной сумме.</span><span class="sxs-lookup"><span data-stu-id="830e6-110">The number of bytes in the checksum.</span></span> <span data-ttu-id="830e6-111">Если Чекксумалгорисм равен ЧЕККСУМАЛГОРИСМ:: MD5, Чекксумбитекаунт имеет значение 16.</span><span class="sxs-lookup"><span data-stu-id="830e6-111">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::md5, checkSumByteCount is 16.</span></span> <span data-ttu-id="830e6-112">Если Чекксумалгорисм равен ЧЕККСУМАЛГОРИСМ:: SHA1, Чекксумбитекаунт — 20.</span><span class="sxs-lookup"><span data-stu-id="830e6-112">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::sha1, checkSumByteCount is 20.</span></span>

<span data-ttu-id="830e6-113">**чекксумалгорисм**</span><span class="sxs-lookup"><span data-stu-id="830e6-113">**checkSumAlgorithm**</span></span>  
<span data-ttu-id="830e6-114">Указывает алгоритм, используемый для формирования контрольной суммы файла.</span><span class="sxs-lookup"><span data-stu-id="830e6-114">Specifies the algorithm used to generate the checksum of the file.</span></span> <span data-ttu-id="830e6-115">Поддерживаемые алгоритмы: MD5 и SHA1.</span><span class="sxs-lookup"><span data-stu-id="830e6-115">Supported algorithms are MD5 and SHA1.</span></span> <span data-ttu-id="830e6-116">Дополнительные сведения см. в разделе Перечисление ЧЕККСУМАЛГОРИСМ.</span><span class="sxs-lookup"><span data-stu-id="830e6-116">For more information, see the CHECKSUMALGORITHM enum.</span></span>

<span data-ttu-id="830e6-117">**чекксумфирстпарт**</span><span class="sxs-lookup"><span data-stu-id="830e6-117">**checkSumFirstPart**</span></span>  
<span data-ttu-id="830e6-118">Первая 8 байт контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="830e6-118">The first 8 byte portion of the checksum.</span></span>

<span data-ttu-id="830e6-119">**чекксумсекондпарт**</span><span class="sxs-lookup"><span data-stu-id="830e6-119">**checkSumSecondPart**</span></span>  
<span data-ttu-id="830e6-120">Вторая 8 байт контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="830e6-120">The second 8 byte portion of the checksum.</span></span>

<span data-ttu-id="830e6-121">**чекксумсирдпарт**</span><span class="sxs-lookup"><span data-stu-id="830e6-121">**checkSumThirdPart**</span></span>  
<span data-ttu-id="830e6-122">Третья 8 байт контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="830e6-122">The third 8 byte portion of the checksum.</span></span>

<span data-ttu-id="830e6-123">**чекксумфаурспарт**</span><span class="sxs-lookup"><span data-stu-id="830e6-123">**checkSumFourthPart**</span></span>  
<span data-ttu-id="830e6-124">Четвертая 8 байта контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="830e6-124">The fourth 8 byte portion of the checksum.</span></span>

## <a name="requirements"></a><span data-ttu-id="830e6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="830e6-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="830e6-126">Header</span><span class="sxs-lookup"><span data-stu-id="830e6-126">Header</span></span></p></td><td><span data-ttu-id="830e6-127">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="830e6-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



