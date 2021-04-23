---
description: Использование постоянных данных языкового стандарта
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Использование постоянных данных языкового стандарта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913695"
---
# <a name="using-persistent-locale-data"></a><span data-ttu-id="48431-103">Использование постоянных данных языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="48431-103">Using Persistent Locale Data</span></span>

<span data-ttu-id="48431-104">Глобализованное приложение часто сохраняет или передает данные, например время и дату.</span><span class="sxs-lookup"><span data-stu-id="48431-104">A globalized application often persists or transmits data, for example, time and date.</span></span> <span data-ttu-id="48431-105">При принятии решения о том, как приложение должно обрабатывать сохраняемость данных, помните, что данные не обязательно будут одинаковыми с компьютера на компьютер или между запусками приложения.</span><span class="sxs-lookup"><span data-stu-id="48431-105">When deciding how your application should handle data persistence, remember that data is not guaranteed to be the same from computer to computer or between runs of the application.</span></span> <span data-ttu-id="48431-106">Это справедливо для обоих [языков](locales-and-languages.md) , поставляемых с Windows и [пользовательскими языками](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="48431-106">This is true for both [locales](locales-and-languages.md) that ship with Windows and [custom locales](custom-locales.md).</span></span>

<span data-ttu-id="48431-107">При проектировании приложения необходимо учитывать множество изменений данных, связанных с языковым стандартом, которые могут возникать.</span><span class="sxs-lookup"><span data-stu-id="48431-107">Design of the application must take into account a variety of locale-related data changes that can occur.</span></span> <span data-ttu-id="48431-108">Пример:</span><span class="sxs-lookup"><span data-stu-id="48431-108">For example:</span></span>

-   <span data-ttu-id="48431-109">Символы валют могут изменяться в том случае, если страны принимают евро.</span><span class="sxs-lookup"><span data-stu-id="48431-109">Currency symbols can change as countries adopt the Euro.</span></span>
-   <span data-ttu-id="48431-110">Региональные настройки могут измениться.</span><span class="sxs-lookup"><span data-stu-id="48431-110">Regional preferences can change.</span></span> <span data-ttu-id="48431-111">Например, формат d/m/y может измениться на формат m/d/y для определенного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="48431-111">For example, the format d/m/y might change to the format m/d/y for a particular locale.</span></span>
-   <span data-ttu-id="48431-112">Написание названий дней может изменяться из-за орфографических реформс.</span><span class="sxs-lookup"><span data-stu-id="48431-112">The spelling of day names can change due to spelling reforms.</span></span> <span data-ttu-id="48431-113">Кроме того, можно изменить регистр для названий месяцев или дней.</span><span class="sxs-lookup"><span data-stu-id="48431-113">Additionally, casing can change for month or day names.</span></span>

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a><span data-ttu-id="48431-114">Использование форматов Locale-Independent для хранения данных и обмена данными</span><span class="sxs-lookup"><span data-stu-id="48431-114">Use Locale-Independent Formats for Storage and Data Interchange</span></span>

<span data-ttu-id="48431-115">Приложение, сохраняющее данные, должно использовать независимые от языкового стандарта форматы для хранения и обмена данными.</span><span class="sxs-lookup"><span data-stu-id="48431-115">An application that persists data should use locale-independent formats for storage and data interchange.</span></span> <span data-ttu-id="48431-116">Примеры являются жестко запрограммированными или стандартными форматами; Инвариантное [ \_ имя \_ локали](locale-name-constants.md)языкового стандарта, а также форматы двоичного хранения.</span><span class="sxs-lookup"><span data-stu-id="48431-116">Examples are hard-coded or standard formats; the invariant locale [LOCALE\_NAME\_INVARIANT](locale-name-constants.md); and binary storage formats.</span></span>

<span data-ttu-id="48431-117">Если требуются постоянные данные сортировки, приложение должно использовать функцию [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) .</span><span class="sxs-lookup"><span data-stu-id="48431-117">If persistent sorting data is required, the application must use the [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) function.</span></span> <span data-ttu-id="48431-118">Помните, что инвариантный формат не остается инвариантным для [сортировки](sorting.md), только для данных национальной настройки и календаря.</span><span class="sxs-lookup"><span data-stu-id="48431-118">Remember that an invariant format does not remain invariant for [sorting](sorting.md), only for locale and calendar data.</span></span>

## <a name="use-the-user-default-locale-for-data-presentation"></a><span data-ttu-id="48431-119">Использовать пользовательский язык по умолчанию для представления данных</span><span class="sxs-lookup"><span data-stu-id="48431-119">Use the User Default Locale for Data Presentation</span></span>

<span data-ttu-id="48431-120">Для представления постоянных данных приложению рекомендуется переформатировать данные с помощью пользовательского языка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="48431-120">To present persistent data, it is best for the application to reformat the data using the user default locale.</span></span> <span data-ttu-id="48431-121">Использование этого языкового стандарта позволяет переопределять пользовательские параметры.</span><span class="sxs-lookup"><span data-stu-id="48431-121">Use of this locale allows user overrides.</span></span> <span data-ttu-id="48431-122">Дополнительные сведения см. в разделе [Национальная настройка \_ пользователя \_ по умолчанию](locale-user-default.md).</span><span class="sxs-lookup"><span data-stu-id="48431-122">For more information, see [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="48431-123">См. также</span><span class="sxs-lookup"><span data-stu-id="48431-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48431-124">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="48431-124">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="48431-125">Пользовательские языковые стандарты</span><span class="sxs-lookup"><span data-stu-id="48431-125">Custom Locales</span></span>](custom-locales.md)
</dt> <dt>

[<span data-ttu-id="48431-126">Сортировка</span><span class="sxs-lookup"><span data-stu-id="48431-126">Sorting</span></span>](sorting.md)
</dt> </dl>

 

 



