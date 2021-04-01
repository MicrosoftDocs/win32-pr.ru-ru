---
description: Будущее криптографических и защищенных коммуникаций легко прогнозировать.
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: Расширение функциональности CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999460"
---
# <a name="extending-cryptoapi-functionality"></a><span data-ttu-id="a9446-103">Расширение функциональности CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="a9446-103">Extending CryptoAPI Functionality</span></span>

<span data-ttu-id="a9446-104">Будущее [*криптографических*](../secgloss/c-gly.md) и защищенных коммуникаций легко прогнозировать.</span><span class="sxs-lookup"><span data-stu-id="a9446-104">The future of [*cryptography*](../secgloss/c-gly.md) and secure communications cannot easily be predicted.</span></span> <span data-ttu-id="a9446-105">Могут возникать новые типы сертификатов, различные расширения сертификатов могут обнаружить распространенное использование, а новые типы сообщений могут быть введены.</span><span class="sxs-lookup"><span data-stu-id="a9446-105">New certificate types might emerge, various certificate extensions might find common usage, and new message types might be introduced.</span></span> <span data-ttu-id="a9446-106">По этой причине расширяемость является частью структуры ключевых функций [*CryptoAPI*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a9446-106">Because of this, extensibility is part of the design of key [*CryptoAPI*](../secgloss/c-gly.md) functions.</span></span>

<span data-ttu-id="a9446-107">В следующих разделах содержатся обзоры использования OID для расширения функций CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="a9446-107">The following sections present overviews on the use of OIDs for extending CryptoAPI functions.</span></span>



| <span data-ttu-id="a9446-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="a9446-108">Topic</span></span>                                                                              | <span data-ttu-id="a9446-109">Содержимое</span><span class="sxs-lookup"><span data-stu-id="a9446-109">Contents</span></span>                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9446-110">Общие сведения о OID</span><span class="sxs-lookup"><span data-stu-id="a9446-110">OID Overview</span></span>](oid-overview.md)                                                   | <span data-ttu-id="a9446-111">Основные понятия OID.</span><span class="sxs-lookup"><span data-stu-id="a9446-111">OID fundamental concepts.</span></span>                                                                                                           |
| [<span data-ttu-id="a9446-112">Создание новых функциональных возможностей</span><span class="sxs-lookup"><span data-stu-id="a9446-112">Creating the New Functionality</span></span>](creating-the-new-functionality.md)               | <span data-ttu-id="a9446-113">Создание OID и функций для расширения использования существующих API.</span><span class="sxs-lookup"><span data-stu-id="a9446-113">Creating OIDs and functions to extend the use of existing APIs.</span></span>                                                                     |
| [<span data-ttu-id="a9446-114">Регистрация новых функций</span><span class="sxs-lookup"><span data-stu-id="a9446-114">Registering the New Functionality</span></span>](registering-the-new-functionality.md)         | <span data-ttu-id="a9446-115">Настройка новых функций, связанных с OID.</span><span class="sxs-lookup"><span data-stu-id="a9446-115">Setting up new OID-related functions.</span></span>                                                                                               |
| [<span data-ttu-id="a9446-116">Установка новых функций</span><span class="sxs-lookup"><span data-stu-id="a9446-116">Installing the New Functionality</span></span>](installing-the-new-functionality.md)           | <span data-ttu-id="a9446-117">Установка функций OID в память для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="a9446-117">Installing OID functions to memory to improve performance.</span></span>                                                                          |
| [<span data-ttu-id="a9446-118">Расширение функциональных возможностей Цертопенсторе</span><span class="sxs-lookup"><span data-stu-id="a9446-118">Extending CertOpenStore Functionality</span></span>](extending-certopenstore-functionality.md) | <span data-ttu-id="a9446-119">Расширение функциональных возможностей [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) с помощью устанавливаемой или зарегистрированной функции поставщика хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a9446-119">Extending [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) functionality using installable or registered certificate-store-provider function.</span></span> |



 

 

 
