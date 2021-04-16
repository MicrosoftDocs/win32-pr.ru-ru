---
description: ИНВАРИАНТный ЯЗЫКовой стандарт \_
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650528"
---
# <a name="locale_invariant"></a><span data-ttu-id="ba714-103">ИНВАРИАНТный ЯЗЫКовой стандарт \_</span><span class="sxs-lookup"><span data-stu-id="ba714-103">LOCALE\_INVARIANT</span></span>

<span data-ttu-id="ba714-104">**Windows XP:** Языковой стандарт, используемый для функций на уровне операционной системы, требующих единообразных и независимых от локалей результатов.</span><span class="sxs-lookup"><span data-stu-id="ba714-104">**Windows XP:** The locale used for operating system-level functions that require consistent and locale-independent results.</span></span> <span data-ttu-id="ba714-105">Например, инвариантный языковой стандарт используется, когда приложение сравнивает символьные строки с помощью функции [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) и ожидает единообразный результат независимо от национальной настройки пользователя.</span><span class="sxs-lookup"><span data-stu-id="ba714-105">For example, the invariant locale is used when an application compares character strings using the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) function and expects a consistent result regardless of the user locale.</span></span> <span data-ttu-id="ba714-106">Параметры инвариантного языкового стандарта похожи на английский (США), но не должны использоваться для вывода форматированных данных.</span><span class="sxs-lookup"><span data-stu-id="ba714-106">The settings of the invariant locale are similar to those for English (United States) but should not be used to display formatted data.</span></span> <span data-ttu-id="ba714-107">Как правило, приложение не использует ИНВАРИАНТ языкового стандарта, \_ поскольку оно ждет, что результаты действия зависят от правил, регулирующих каждый отдельный языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="ba714-107">Typically, an application does not use LOCALE\_INVARIANT because it expects the results of an action to depend on the rules governing each individual locale.</span></span> <span data-ttu-id="ba714-108">Значение ИНВАРИАНТного языкового стандарта \_ — 0x007f.</span><span class="sxs-lookup"><span data-stu-id="ba714-108">The value of LOCALE\_INVARIANT IS 0x007f.</span></span>

 

 
