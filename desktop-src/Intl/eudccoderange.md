---
description: Раздел реестра Еудккодеранже определяет диапазоны кодов EUDC для различных кодовых страниц (наборов символов).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: еудккодеранже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684245"
---
# <a name="eudccoderange"></a><span data-ttu-id="241a5-103">еудккодеранже</span><span class="sxs-lookup"><span data-stu-id="241a5-103">EUDCCodeRange</span></span>

<span data-ttu-id="241a5-104">Раздел реестра Еудккодеранже определяет диапазоны кодов [EUDC](end-user-defined-characters.md) для различных кодовых страниц (наборов символов).</span><span class="sxs-lookup"><span data-stu-id="241a5-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="241a5-105">Он используется только инструментами, которые создают Еудкс и не являются непосредственной проблемой для пользователей EUDC.</span><span class="sxs-lookup"><span data-stu-id="241a5-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="241a5-106">Этот раздел реестра находится в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="241a5-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="241a5-107">\_ \_ \\ \\ CurrentControlSet \\ управления \\ \\ кодовой страницей NLS \\ в системе hKey локального компьютера</span><span class="sxs-lookup"><span data-stu-id="241a5-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="241a5-108">Формат будет следующим:</span><span class="sxs-lookup"><span data-stu-id="241a5-108">The format is:</span></span>

<span data-ttu-id="241a5-109">Еудккодеранже кодовая страница = Фромто \[ , фромто\]</span><span class="sxs-lookup"><span data-stu-id="241a5-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="241a5-110">где:</span><span class="sxs-lookup"><span data-stu-id="241a5-110">where:</span></span>



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="241a5-111">CodePage</span><span class="sxs-lookup"><span data-stu-id="241a5-111">CodePage</span></span> | <span data-ttu-id="241a5-112">Одна из строк "932" (японский), "936" (упрощенный китайский), "949" (корейский), "950" (китайский (традиционное письмо)) или "Unicode" (Юникод).</span><span class="sxs-lookup"><span data-stu-id="241a5-112">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="241a5-113">Другие значения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="241a5-113">No other values are supported.</span></span>                                     |
| <span data-ttu-id="241a5-114">фромто</span><span class="sxs-lookup"><span data-stu-id="241a5-114">FromTo</span></span>   | <span data-ttu-id="241a5-115">Строковое значение, состоящее из пары из 4-значных шестнадцатеричных значений, разделенных дефисом (-).</span><span class="sxs-lookup"><span data-stu-id="241a5-115">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="241a5-116">Можно указать до четырех значений Фромто, но каждое из них должно быть отделено от предыдущего значения запятой (,).</span><span class="sxs-lookup"><span data-stu-id="241a5-116">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="241a5-117">Ниже приведены правильные значения для записи реестра.</span><span class="sxs-lookup"><span data-stu-id="241a5-117">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="241a5-118">См. также</span><span class="sxs-lookup"><span data-stu-id="241a5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="241a5-119">Записи реестра EUDC</span><span class="sxs-lookup"><span data-stu-id="241a5-119">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="241a5-120">EUDC</span><span class="sxs-lookup"><span data-stu-id="241a5-120">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



