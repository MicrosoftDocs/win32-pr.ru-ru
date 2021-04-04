---
title: Получение статистики модуля записи
description: Получение статистики модуля записи
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Расширенный системный формат (ASF), статистика записи
- ASF (Расширенный системный формат), статистика записи
- Статистика модуля записи, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103987274"
---
# <a name="to-get-writer-statistics"></a><span data-ttu-id="ca040-106">Получение статистики модуля записи</span><span class="sxs-lookup"><span data-stu-id="ca040-106">To Get Writer Statistics</span></span>

<span data-ttu-id="ca040-107">Модуль записи может предоставлять статистические сведения о операциях записи.</span><span class="sxs-lookup"><span data-stu-id="ca040-107">The writer can provide statistical information about writing operations.</span></span> <span data-ttu-id="ca040-108">Существует два метода для сбора статистики модуля записи: [**ивмвритерадванцед::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) IWMWriterAdvanced3 и [**:: жетстатистиксекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span><span class="sxs-lookup"><span data-stu-id="ca040-108">There are two methods for gathering writer statistics: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) and [**IWMWriterAdvanced3::GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span></span> <span data-ttu-id="ca040-109">Сведения, полученные с помощью **жетстатистиксекс** , являются более точными, чем сведения, полученные функцией **статистики**.</span><span class="sxs-lookup"><span data-stu-id="ca040-109">The information retrieved by **GetStatisticsEx** is more specific than the information retrieved by **GetStatistics**.</span></span>

<span data-ttu-id="ca040-110">Оба метода заполняют структуры статистическими данными.</span><span class="sxs-lookup"><span data-stu-id="ca040-110">Both methods populate structures with statistical information.</span></span> <span data-ttu-id="ca040-111">**В статистике** используется [**Структура \_ \_ статистики модуля записи WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) , а в **жетстатистиксекс** используется структура [**\_ \_ Statistics \_ модуля записи WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) .</span><span class="sxs-lookup"><span data-stu-id="ca040-111">**GetStatistics** uses the [**WM\_WRITER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) structure, and **GetStatisticsEx** uses the [**WM\_WRITER\_STATISTICS\_EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) structure.</span></span> <span data-ttu-id="ca040-112">**Жетстатистиксекс** не дублирует данные, полученные функцией **статистики**.</span><span class="sxs-lookup"><span data-stu-id="ca040-112">**GetStatisticsEx** does not duplicate the data obtained by **GetStatistics**.</span></span> <span data-ttu-id="ca040-113">Для получения наиболее полных сведений следует вызывать оба метода.</span><span class="sxs-lookup"><span data-stu-id="ca040-113">For the most complete information, you should call both methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca040-114">См. также</span><span class="sxs-lookup"><span data-stu-id="ca040-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca040-115">**Интерфейс Ивмвритерадванцед**</span><span class="sxs-lookup"><span data-stu-id="ca040-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="ca040-116">**Интерфейс IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="ca040-116">**IWMWriterAdvanced3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[<span data-ttu-id="ca040-117">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="ca040-117">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




