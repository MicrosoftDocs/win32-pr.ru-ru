---
description: Класс устройств TAPI/Terminal состоит из телефонных устройств, связанных с каждым терминалом, в строке или на терминале в каждой строке, связанной с телефонным устройством. Доступ к этим устройствам осуществляется с помощью функций устройства TAPI Line или Phone Device.
ms.assetid: 466ed2cd-f737-4df4-8633-4fb5c95b4b6c
title: TAPI/терминал
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce64da984f766e8ca3c0c47f1b60db6e9d7d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674074"
---
# <a name="tapiterminal"></a><span data-ttu-id="c283e-104">TAPI/терминал</span><span class="sxs-lookup"><span data-stu-id="c283e-104">tapi/terminal</span></span>

<span data-ttu-id="c283e-105">Класс устройств TAPI/Terminal состоит из телефонных устройств, связанных с каждым терминалом, в строке или на терминале в каждой строке, связанной с телефонным устройством.</span><span class="sxs-lookup"><span data-stu-id="c283e-105">The tapi/terminal device class consists of the phone devices associated with each terminal on a line or the terminal on each line associated with a phone device.</span></span> <span data-ttu-id="c283e-106">Доступ к этим устройствам осуществляется с помощью функций [устройства TAPI Line](line-device-functions.md) или [Phone Device](phone-device-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c283e-106">You access these devices by using the TAPI [line device](line-device-functions.md) or [phone device functions](phone-device-functions.md).</span></span>

<span data-ttu-id="c283e-107">Функция [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **ДВСТРИНГФОРМАТ** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:</span><span class="sxs-lookup"><span data-stu-id="c283e-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

<span data-ttu-id="c283e-108">Элемент **адвдевицеид** представляет собой массив идентификаторов телефонных устройств.</span><span class="sxs-lookup"><span data-stu-id="c283e-108">The **adwDeviceId** member is an array of phone device identifiers.</span></span> <span data-ttu-id="c283e-109">Для каждого терминала, заданного элементом **двнумтерминалс** в структуре [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) для данного устройства линии, существует один элемент массива.</span><span class="sxs-lookup"><span data-stu-id="c283e-109">There is one array element for each terminal specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the given line device.</span></span> <span data-ttu-id="c283e-110">Каждый элемент указывает идентификатор телефонного устройства, связанного с соответствующим терминалом в строке.</span><span class="sxs-lookup"><span data-stu-id="c283e-110">Each element specifies the identifier of the phone device associated with the corresponding terminal on the line.</span></span> <span data-ttu-id="c283e-111">Если с терминалом не связано ни одно телефонное устройство, для элемента устанавливается значение – 1 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="c283e-111">If there is no phone device associated with a terminal, the element is set to –1 (0xFFFFFFFF).</span></span>

<span data-ttu-id="c283e-112">Функция [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **ДВСТРИНГФОРМАТ** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:</span><span class="sxs-lookup"><span data-stu-id="c283e-112">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

<span data-ttu-id="c283e-113">Элемент **адвтерминалид** представляет собой массив идентификаторов терминала.</span><span class="sxs-lookup"><span data-stu-id="c283e-113">The **adwTerminalID** member is an array of terminal identifiers.</span></span> <span data-ttu-id="c283e-114">Для каждого идентификатора устройства строки, заданного функцией [**линеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) или [**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) , существует один элемент массива.</span><span class="sxs-lookup"><span data-stu-id="c283e-114">There is one array element for each line device identifier specified by the [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) function.</span></span> <span data-ttu-id="c283e-115">Каждый элемент массива содержит идентификатор терминала, связанный с телефонным устройством для данного устройства линии.</span><span class="sxs-lookup"><span data-stu-id="c283e-115">Each array element contains the terminal identifier associated with the phone device for the given line device.</span></span> <span data-ttu-id="c283e-116">Если телефонного устройства нет, элементу присваивается значение – 1 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="c283e-116">If there is no phone device, the element is set to –1 (0xFFFFFFFF).</span></span> <span data-ttu-id="c283e-117">Идентификаторы терминала находятся в диапазоне от нуля до одного меньше числа, заданного элементом **двнумтерминалс** в структуре [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .</span><span class="sxs-lookup"><span data-stu-id="c283e-117">The terminal identifiers range in value from zero to one less than the number specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>

 

 



