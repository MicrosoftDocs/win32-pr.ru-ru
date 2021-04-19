---
description: Свойство Summary keywords в базах данных установки или преобразованиях содержит список ключевых слов.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Свойство сводки ключевых слов
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689090"
---
# <a name="keywords-summary-property"></a><span data-ttu-id="7597a-103">Свойство сводки ключевых слов</span><span class="sxs-lookup"><span data-stu-id="7597a-103">Keywords Summary property</span></span>

<span data-ttu-id="7597a-104">Свойство **Summary keywords** в базах данных установки или преобразованиях содержит список ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="7597a-104">The **Keywords Summary** property in installation databases or transforms contains a list of keywords.</span></span> <span data-ttu-id="7597a-105">Ключевые слова могут использоваться в браузерах файлов для поиска файлов по ключевым словам.</span><span class="sxs-lookup"><span data-stu-id="7597a-105">The keywords may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="7597a-106">Это свойство содержит список источников исправления в пакете исправлений.</span><span class="sxs-lookup"><span data-stu-id="7597a-106">This property contains a list of sources of the patch in a patch package.</span></span>

<span data-ttu-id="7597a-107">Вы должны быть автором базы данных установки, преобразованием или пакетом исправлений, чтобы предоставить значение этого свойства в сводных данных.</span><span class="sxs-lookup"><span data-stu-id="7597a-107">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="7597a-108">Авторы должны выполнить следующие действия, чтобы определить правильное значение.</span><span class="sxs-lookup"><span data-stu-id="7597a-108">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="7597a-109">В пакете установки установите значение этого свойства в список ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="7597a-109">In an installation package, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="7597a-110">Ключевое слово должно включать "Installer", а также ключевые слова для конкретного продукта и может быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="7597a-110">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="7597a-111">В преобразовании задайте значение этого свойства в виде списка ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="7597a-111">In a transform, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="7597a-112">Ключевое слово должно включать "Installer", а также ключевые слова для конкретного продукта и может быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="7597a-112">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="7597a-113">В пакете исправлений присвойте свойству значение этого свойства в виде разделенного точкой с запятой списка сетевых или URL-адресов для источников исправления.</span><span class="sxs-lookup"><span data-stu-id="7597a-113">In a patch package, set the value of this property to a semicolon-delimited list of network or URL locations for the sources of the patch.</span></span> <span data-ttu-id="7597a-114">После установки исправления установщик добавляет их в исходный список для пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="7597a-114">When the patch is installed, the installer adds these to the source list for the patch package.</span></span> <span data-ttu-id="7597a-115">Если кэшированное исправление отсутствует, установщик может выполнить поиск источника в исходном расположении, добавить его в список источников по **ключевым словам** свойства или расположение, добавленное в исходный список с помощью функций [**мсисаурцелистаддсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) или [**мсисаурцелистаддсаурцеекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) .</span><span class="sxs-lookup"><span data-stu-id="7597a-115">If the cached patch becomes missing, the installer can search for a source in the original location, a location added to the source list by the **Keywords Summary** property, or a location added to the source list using the [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) or [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7597a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7597a-116">Requirements</span></span>



| <span data-ttu-id="7597a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7597a-117">Requirement</span></span> | <span data-ttu-id="7597a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7597a-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7597a-119">Версия</span><span class="sxs-lookup"><span data-stu-id="7597a-119">Version</span></span><br/> | <span data-ttu-id="7597a-120">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7597a-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7597a-121">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7597a-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7597a-122">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="7597a-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7597a-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7597a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7597a-124">Описания свойств сводки</span><span class="sxs-lookup"><span data-stu-id="7597a-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




