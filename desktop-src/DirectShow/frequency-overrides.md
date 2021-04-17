---
description: Переопределения частоты
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Переопределения частоты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536647"
---
# <a name="frequency-overrides"></a><span data-ttu-id="8fd20-103">Переопределения частоты</span><span class="sxs-lookup"><span data-stu-id="8fd20-103">Frequency Overrides</span></span>

<span data-ttu-id="8fd20-104">Было потрачено значительное количество усилий, чтобы убедиться, что для каждой страны или региона заданы правильные частоты вещания и стандартные сочетания цветов.</span><span class="sxs-lookup"><span data-stu-id="8fd20-104">A significant amount of effort was spent to ensure that the broadcast frequencies and color standard assignments are correct for each country/region.</span></span> <span data-ttu-id="8fd20-105">Несмотря на это, существуют ситуации, когда таблицы частоты недостаточно, содержат ошибки или устаревают.</span><span class="sxs-lookup"><span data-stu-id="8fd20-105">Even so, there will be situations when the frequency tables are not sufficient, contain errors, or become obsolete.</span></span> <span data-ttu-id="8fd20-106">Для решения этой проблемы частоты, перечисленные в таблицах частот фильтра ТВ-тюнера, можно выборочно переопределять с помощью следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="8fd20-106">To address this problem, the frequencies listed in the TV Tuner filter's frequency tables may be selectively overridden, by using the following registry key:</span></span>

<span data-ttu-id="8fd20-107">**HKey \_ Локальный \_ компьютер** \\ **программное обеспечение** \\ **Microsoft** \\ **TV системные службы** \\ **тваутотуне** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="8fd20-107">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

> [!Note]  
> <span data-ttu-id="8fd20-108">Начиная с Windows 7, для приложений x86, работающих на 64-разрядных версиях Windows, используется следующий перенаправленный раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="8fd20-108">Starting in Windows 7, the following redirected registry key is used for x86 applications running on x64 versions of Windows:</span></span>

 

<span data-ttu-id="8fd20-109">**HKey \_ Локальное \_** \\ **программное обеспечение** \\ **WOW6432Node** \\ **Microsoft** \\ **TV системные службы** \\ **тваутотуне** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="8fd20-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Wow6432Node**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

<span data-ttu-id="8fd20-110">Переопределения частоты группируются в определяемые приложением "области настройки", которые определяются по числу.</span><span class="sxs-lookup"><span data-stu-id="8fd20-110">Frequency overrides are grouped into application-defined "tuning spaces," which are identified by number.</span></span> <span data-ttu-id="8fd20-111">В следующем примере показан пример переопределения:</span><span class="sxs-lookup"><span data-stu-id="8fd20-111">The following example shows an example override:</span></span>

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

<span data-ttu-id="8fd20-112">В этом случае "TS0-1" указывает пространство настройки 0 для частотных кабелей.</span><span class="sxs-lookup"><span data-stu-id="8fd20-112">In this case, "TS0-1" indicates Tuning Space 0 for cable frequencies.</span></span> <span data-ttu-id="8fd20-113">Первый номер определяет пространство настройки.</span><span class="sxs-lookup"><span data-stu-id="8fd20-113">The first number identifies the tuning space.</span></span> <span data-ttu-id="8fd20-114">Второе число — 0 для частот вещания или 1 — для частотных кабелей.</span><span class="sxs-lookup"><span data-stu-id="8fd20-114">The second number is either 0 for broadcast frequencies or 1 for cable frequencies.</span></span>

<span data-ttu-id="8fd20-115">Подключ с именем "12" переопределяет значение частоты для частоты в индексе 12 в текущей таблице частоты.</span><span class="sxs-lookup"><span data-stu-id="8fd20-115">The subkey named "12" overrides the frequency value for the frequency at index 12 in the current frequency table.</span></span> <span data-ttu-id="8fd20-116">Значение подраздела — **DWORD** , указывающий частоту в герцах (Гц).</span><span class="sxs-lookup"><span data-stu-id="8fd20-116">The value of the subkey is a **DWORD** that specifies the frequency in Hertz (Hz).</span></span> <span data-ttu-id="8fd20-117">В этом примере устанавливается частота 67,25 МГц.</span><span class="sxs-lookup"><span data-stu-id="8fd20-117">In this example, the frequency is set to 67.25 MHz.</span></span> <span data-ttu-id="8fd20-118">Переопределения можно определить для любых номеров каналов в диапазоне от 1 до 999 включительно.</span><span class="sxs-lookup"><span data-stu-id="8fd20-118">Overrides can be defined for any channel numbers in the range of 1 to 999, inclusive.</span></span> <span data-ttu-id="8fd20-119">Если оборудование настройки не поддерживает заданную частоту, запрос на настройку завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8fd20-119">If the tuning hardware does not support a given frequency, the tune request will fail.</span></span>

<span data-ttu-id="8fd20-120">Этот механизм также можно использовать для создания новых номеров каналов за пределами существующего диапазона в таблице Frequency.</span><span class="sxs-lookup"><span data-stu-id="8fd20-120">This mechanism can also be used to create new channel numbers outside the existing range in the frequency table.</span></span> <span data-ttu-id="8fd20-121">Метод [**иамтунер:: чаннелминмакс**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) вернет диапазон расширенных каналов.</span><span class="sxs-lookup"><span data-stu-id="8fd20-121">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method will return the extended channel range.</span></span> <span data-ttu-id="8fd20-122">Например, если исходный диапазон каналов имел значение от 1 до 158, а переопределение канала "200" добавляется в реестр, метод **чаннелминмакс** будет возвращать значение 200 в качестве максимального канала.</span><span class="sxs-lookup"><span data-stu-id="8fd20-122">For example, if the original channel range was 1 to 158, and a channel override of "200" is added to the registry, the **ChannelMinMax** method will return 200 as the maximum channel.</span></span> <span data-ttu-id="8fd20-123">В этом случае номера каналов в диапазоне от 159 до 199 не будут иметь назначенных частот, поэтому все запросы на настройку в этом диапазоне будут автоматически завершаться сбоем.</span><span class="sxs-lookup"><span data-stu-id="8fd20-123">In this case, channel numbers in the range of 159 to 199 will have no frequencies assigned to them, so any tuning requests in that range will automatically fail.</span></span>

<span data-ttu-id="8fd20-124">Метод [**иамтунер::p UT \_ тунингспаце**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) позволяет приложению выбрать набор переопределений и точную информацию для использования.</span><span class="sxs-lookup"><span data-stu-id="8fd20-124">The [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method allows the application to choose which set of overrides and fine-tuning information to use.</span></span> <span data-ttu-id="8fd20-125">Номера пространства настройки являются произвольными.</span><span class="sxs-lookup"><span data-stu-id="8fd20-125">Tuning space numbers are arbitrary.</span></span> <span data-ttu-id="8fd20-126">Ответственность за поддержание связи между пространством настройки и таблицей частоты является обязанностью приложения.</span><span class="sxs-lookup"><span data-stu-id="8fd20-126">It is the application's responsibility to maintain the relationship between the tuning space and the frequency table.</span></span> <span data-ttu-id="8fd20-127">Самый простой подход заключается в использовании кода страны или региона в качестве номера пространства настройки.</span><span class="sxs-lookup"><span data-stu-id="8fd20-127">The most straightforward approach is to use the country/region code as the tuning space number.</span></span> <span data-ttu-id="8fd20-128">Затем каждый раз, когда приложение переключается на новый код страны или региона, оно также переключается на то же пространство настройки (в этом порядке).</span><span class="sxs-lookup"><span data-stu-id="8fd20-128">Then, every time the application switches to a new country/region code, it also switches to the same tuning space (in that order).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fd20-129">См. также</span><span class="sxs-lookup"><span data-stu-id="8fd20-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fd20-130">Международная Настройка аналогового ТВ</span><span class="sxs-lookup"><span data-stu-id="8fd20-130">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



