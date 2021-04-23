---
description: NLS включает ряд функций API, которые приложения могут использовать для сопоставления языковых стандартов и национальных настроек, а также перечисления нейтральных языковых стандартов.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Сопоставление данных локали
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263437"
---
# <a name="mapping-locale-data"></a><span data-ttu-id="36738-103">Сопоставление данных локали</span><span class="sxs-lookup"><span data-stu-id="36738-103">Mapping Locale Data</span></span>

<span data-ttu-id="36738-104">NLS включает ряд функций API, которые приложения могут использовать для сопоставления языковых [стандартов и национальных настроек,](locale-identifiers.md) а также перечисления нейтральных [языковых](locale-names.md)стандартов.</span><span class="sxs-lookup"><span data-stu-id="36738-104">NLS includes a number of API functions that your applications can use to map locale data between [locale identifiers](locale-identifiers.md) and [locale names](locale-names.md), and list neutral locales.</span></span> <span data-ttu-id="36738-105">В этом разделе обсуждаются эти функции в Windows Vista и более поздних версиях, а также в операционных системах, предшествующих Windows Vista (иногда называемых системами нижнего уровня).</span><span class="sxs-lookup"><span data-stu-id="36738-105">This topic discusses the use of these functions on Windows Vista and later and on pre-Windows Vista operating systems (sometimes called "downlevel systems").</span></span>

## <a name="map-locale-data-on-windows-vista-and-later"></a><span data-ttu-id="36738-106">Сопоставьте данные национальной настройки в Windows Vista и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="36738-106">Map Locale Data on Windows Vista and Later</span></span>

<span data-ttu-id="36738-107">NLS предоставляет несколько функций сопоставления языкового стандарта для использования приложениями, разрабатываемыми для работы в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36738-107">NLS provides several locale mapping functions for use by applications that you develop to run on Windows Vista and later.</span></span> <span data-ttu-id="36738-108">Он также включает функции, которые приложения могут использовать для перечисления нейтральных языковых стандартов.</span><span class="sxs-lookup"><span data-stu-id="36738-108">It also includes functions that your applications can use to enumerate neutral locales.</span></span>

<span data-ttu-id="36738-109">**Использование стандартных функций преобразования для сопоставления данных**</span><span class="sxs-lookup"><span data-stu-id="36738-109">**Use the Standard Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="36738-110">Чтобы выполнить сопоставление между именем локали и идентификатором локали, приложение может вызвать функцию [**локаленаметолЦид**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) .</span><span class="sxs-lookup"><span data-stu-id="36738-110">To map between a locale name and a locale identifier, your application can call the [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function.</span></span> <span data-ttu-id="36738-111">Приложение использует [**лЦидтолокаленаме**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) для сопоставления идентификатора языкового стандарта и имени локали.</span><span class="sxs-lookup"><span data-stu-id="36738-111">The application uses [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to map between a locale identifier and a locale name.</span></span>

<span data-ttu-id="36738-112">**Список нейтральных языковых стандартов**</span><span class="sxs-lookup"><span data-stu-id="36738-112">**List Neutral Locales**</span></span>

<span data-ttu-id="36738-113">Чтобы перечислить Нейтральные языковые стандарты для Windows 7 и более поздних версий, приложение может вызвать [**енумсистемлокалесекс**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) с *dwFlags* , установленным в [**locale \_ неутралдата**](locale-neutraldata.md).</span><span class="sxs-lookup"><span data-stu-id="36738-113">To enumerate neutral locales for Windows 7 and later, your application can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) with *dwFlags* set to [**LOCALE\_NEUTRALDATA**](locale-neutraldata.md).</span></span> <span data-ttu-id="36738-114">Он также может использовать [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) с параметром *LCType* , установленным в [**locale \_ инеутрал**](locale-ineutral.md).</span><span class="sxs-lookup"><span data-stu-id="36738-114">It can also use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with *LCType* set to [**LOCALE\_INEUTRAL**](locale-ineutral.md).</span></span>

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="36738-115">Соответствие языковых данных в операционных системах, предшествующих Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36738-115">Map Locale Data on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="36738-116">NLS включает библиотеку с прямым связыванием (DLL), которая используется для приложений, разрабатываемых для работы в операционных системах, предшествующих Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="36738-116">NLS includes a direct-link library (DLL) to use for applications that you develop to run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="36738-117">Библиотека DLL поддерживает функции преобразования и перечисления для сопоставления данных.</span><span class="sxs-lookup"><span data-stu-id="36738-117">The DLL supports both conversion and listing functions for data mapping.</span></span>

> [!Note]  
> <span data-ttu-id="36738-118">Приложения, работающие только в Windows Vista и более поздних версиях, не должны использовать функции сопоставления нижнего уровня или перечисления.</span><span class="sxs-lookup"><span data-stu-id="36738-118">Applications that only run on Windows Vista and later should not use the downlevel mapping or listing functions.</span></span>

 

<span data-ttu-id="36738-119">**Использование функций преобразования прежних версий для сопоставления данных**</span><span class="sxs-lookup"><span data-stu-id="36738-119">**Use the Downlevel Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="36738-120">Приложение, нацеленное на систему нижнего уровня, может вызвать функцию [**довнлевеллЦидтолокаленаме**](downlevellcidtolocalename.md) для преобразования идентификатора локали в имя языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="36738-120">Your application targeted at a downlevel system can call the [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) function to convert a locale identifier to a locale name.</span></span> <span data-ttu-id="36738-121">Если необходимо преобразовать имя языкового стандарта в идентификатор локали, он должен вызвать [**довнлевеллокаленаметолЦид**](downlevellocalenametolcid.md).</span><span class="sxs-lookup"><span data-stu-id="36738-121">If it needs to convert a locale name to a locale identifier, it should call [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span></span>

<span data-ttu-id="36738-122">**Использование функций перечисления предыдущих версий для перечисления нейтральных языковых стандартов**</span><span class="sxs-lookup"><span data-stu-id="36738-122">**Use the Downlevel Listing Functions to Enumerate Neutral Locales**</span></span>

<span data-ttu-id="36738-123">Приложение должно вызывать [**довнлевелжетпарентлокалелЦид**](downlevelgetparentlocalelcid.md) для получения идентификатора локали родителя для локали.</span><span class="sxs-lookup"><span data-stu-id="36738-123">Your application should call the [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) to retrieve the locale identifier of the parent for a locale.</span></span> <span data-ttu-id="36738-124">Если приложению необходимо получить имя локали родителя для локали, оно должно вызвать [**довнлевелжетпарентлокаленаме**](downlevelgetparentlocalename.md).</span><span class="sxs-lookup"><span data-stu-id="36738-124">If the application needs to get the locale name of the parent for the locale, it should call [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="36738-125">См. также</span><span class="sxs-lookup"><span data-stu-id="36738-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36738-126">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="36738-126">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="36738-127">Идентификаторы языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="36738-127">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="36738-128">Имена языковых стандартов</span><span class="sxs-lookup"><span data-stu-id="36738-128">Locale Names</span></span>](locale-names.md)
</dt> </dl>

 

 



