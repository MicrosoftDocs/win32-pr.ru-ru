---
description: Предоставляет функциональные возможности для генерации случайных чисел, преобразования и кодирования и декодирования из Base64.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Служебный объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669073"
---
# <a name="utilities-object"></a><span data-ttu-id="7270f-103">Служебный объект</span><span class="sxs-lookup"><span data-stu-id="7270f-103">Utilities object</span></span>

<span data-ttu-id="7270f-104">\[Объект **служебных программ** доступен для использования в операционных системах, указанных в разделе требования.\]</span><span class="sxs-lookup"><span data-stu-id="7270f-104">\[The **Utilities** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="7270f-105">Объект **Utilities** предоставляет функциональные возможности для генерации случайных чисел, преобразования, кодирования и декодирования из Base64.</span><span class="sxs-lookup"><span data-stu-id="7270f-105">The **Utilities** object provides functionality for random number generation, conversions, and encoding and decoding from base64.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7270f-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="7270f-106">When to use</span></span>

<span data-ttu-id="7270f-107">Объект **Utilities** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="7270f-107">The **Utilities** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="7270f-108">Кодирует строку в кодировке Base64 или декодировать строку из Base64.</span><span class="sxs-lookup"><span data-stu-id="7270f-108">Encode a string as base64 or decode a string from base64.</span></span>
-   <span data-ttu-id="7270f-109">Преобразуйте двоичную упакованную строку в массив байтов и наоборот.</span><span class="sxs-lookup"><span data-stu-id="7270f-109">Convert a binary-packed string to a byte array and vice versa.</span></span>
-   <span data-ttu-id="7270f-110">Преобразовать двоичную упакованную строку в шестнадцатеричную строку и наоборот.</span><span class="sxs-lookup"><span data-stu-id="7270f-110">Convert a binary-packed string to a hexadecimal string and vice versa.</span></span>
-   <span data-ttu-id="7270f-111">Создание безопасного случайного числа.</span><span class="sxs-lookup"><span data-stu-id="7270f-111">Generate a secure random number.</span></span>
-   <span data-ttu-id="7270f-112">Преобразование местного времени в время в формате UTC (время по Гринвичу) и наоборот.</span><span class="sxs-lookup"><span data-stu-id="7270f-112">Convert local time to Coordinated Universal Time (Greenwich Mean Time) and vice versa.</span></span>

## <a name="members"></a><span data-ttu-id="7270f-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="7270f-113">Members</span></span>

<span data-ttu-id="7270f-114">В объект **Utilities** входят следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7270f-114">The **Utilities** object has these types of members:</span></span>

-   [<span data-ttu-id="7270f-115">Методы</span><span class="sxs-lookup"><span data-stu-id="7270f-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7270f-116">Методы</span><span class="sxs-lookup"><span data-stu-id="7270f-116">Methods</span></span>

<span data-ttu-id="7270f-117">Объект **Utilities** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7270f-117">The **Utilities** object has these methods.</span></span>



| <span data-ttu-id="7270f-118">Метод</span><span class="sxs-lookup"><span data-stu-id="7270f-118">Method</span></span>                                                               | <span data-ttu-id="7270f-119">Описание</span><span class="sxs-lookup"><span data-stu-id="7270f-119">Description</span></span>                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="7270f-120">**Base64Decode**</span><span class="sxs-lookup"><span data-stu-id="7270f-120">**Base64Decode**</span></span>](utilities-base64decode.md)                       | <span data-ttu-id="7270f-121">Декодирует строку из Base64.</span><span class="sxs-lookup"><span data-stu-id="7270f-121">Decodes a string from base64.</span></span><br/>                                     |
| [<span data-ttu-id="7270f-122">**Base64Encode**</span><span class="sxs-lookup"><span data-stu-id="7270f-122">**Base64Encode**</span></span>](utilities-base64encode.md)                       | <span data-ttu-id="7270f-123">Кодирует строку в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="7270f-123">Encodes a string as base64.</span></span><br/>                                       |
| [<span data-ttu-id="7270f-124">**бинаристрингтобитеаррай**</span><span class="sxs-lookup"><span data-stu-id="7270f-124">**BinaryStringToByteArray**</span></span>](utilities-binarystringtobytearray.md) | <span data-ttu-id="7270f-125">Преобразует упакованную двоичную строку в массив байтов.</span><span class="sxs-lookup"><span data-stu-id="7270f-125">Converts a binary-packed string to an array of bytes.</span></span><br/>             |
| [<span data-ttu-id="7270f-126">**бинаритохекс**</span><span class="sxs-lookup"><span data-stu-id="7270f-126">**BinaryToHex**</span></span>](utilities-binarytohex.md)                         | <span data-ttu-id="7270f-127">Преобразует упакованную двоичную строку в шестнадцатеричную строку.</span><span class="sxs-lookup"><span data-stu-id="7270f-127">Converts a binary-packed string to a hexadecimal string.</span></span><br/>          |
| [<span data-ttu-id="7270f-128">**битеаррайтобинаристринг**</span><span class="sxs-lookup"><span data-stu-id="7270f-128">**ByteArrayToBinaryString**</span></span>](utilities-bytearraytobinarystring.md) | <span data-ttu-id="7270f-129">Преобразует массив байтов в двоичную строку.</span><span class="sxs-lookup"><span data-stu-id="7270f-129">Converts an array of bytes to a binary-packed string.</span></span><br/>             |
| [<span data-ttu-id="7270f-130">**Псевдослучайных**</span><span class="sxs-lookup"><span data-stu-id="7270f-130">**GetRandom**</span></span>](utilities-getrandom.md)                             | <span data-ttu-id="7270f-131">Создает безопасное случайное число.</span><span class="sxs-lookup"><span data-stu-id="7270f-131">Generates a secure random number.</span></span><br/>                                 |
| [<span data-ttu-id="7270f-132">**хекстобинари**</span><span class="sxs-lookup"><span data-stu-id="7270f-132">**HexToBinary**</span></span>](utilities-hextobinary.md)                         | <span data-ttu-id="7270f-133">Преобразует шестнадцатеричную строку в двоичную строку.</span><span class="sxs-lookup"><span data-stu-id="7270f-133">Converts a hexadecimal string to a binary-packed string.</span></span><br/>          |
| [<span data-ttu-id="7270f-134">**локалтиметаутктиме**</span><span class="sxs-lookup"><span data-stu-id="7270f-134">**LocalTimeToUTCTime**</span></span>](utilities-localtimetoutctime.md)           | <span data-ttu-id="7270f-135">Преобразует местное время компьютера в время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="7270f-135">Converts the computer's local time to Coordinated Universal Time.</span></span><br/> |
| [<span data-ttu-id="7270f-136">**утктиметолокалтиме**</span><span class="sxs-lookup"><span data-stu-id="7270f-136">**UTCTimeToLocalTime**</span></span>](utilities-utctimetolocaltime.md)           | <span data-ttu-id="7270f-137">Преобразовывает время в формате UTC в местное время компьютера.</span><span class="sxs-lookup"><span data-stu-id="7270f-137">Converts Coordinated Universal Time to the computer's local time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7270f-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7270f-138">Remarks</span></span>

<span data-ttu-id="7270f-139">Объект **служебных программ** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="7270f-139">The **Utilities** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="7270f-140">ProgID для объекта **служебных программ** — CAPICOM. Utilities. 1.</span><span class="sxs-lookup"><span data-stu-id="7270f-140">The ProgID for the **Utilities** object is CAPICOM.Utilities.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="7270f-141">Требования</span><span class="sxs-lookup"><span data-stu-id="7270f-141">Requirements</span></span>



| <span data-ttu-id="7270f-142">Требование</span><span class="sxs-lookup"><span data-stu-id="7270f-142">Requirement</span></span> | <span data-ttu-id="7270f-143">Значение</span><span class="sxs-lookup"><span data-stu-id="7270f-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7270f-144">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7270f-144">Redistributable</span></span><br/> | <span data-ttu-id="7270f-145">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="7270f-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7270f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7270f-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="7270f-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7270f-147"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




