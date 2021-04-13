---
description: Каждый идентификатор языка состоит из основного идентификатора языка, указывающего язык и идентификатор языка, указывающий страну или регион.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Константы и строки идентификатора языка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346042"
---
# <a name="language-identifier-constants-and-strings"></a><span data-ttu-id="da187-103">Константы и строки идентификатора языка</span><span class="sxs-lookup"><span data-stu-id="da187-103">Language Identifier Constants and Strings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da187-104">Константы идентификатора языка являются устаревшими, и их использование не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="da187-104">Language identifier constants are deprecated and their use is discouraged.</span></span> <span data-ttu-id="da187-105">Использование имен языковых стандартов вместо идентификаторов языкового стандарта всегда является предпочтительным.</span><span class="sxs-lookup"><span data-stu-id="da187-105">Use of locale names instead of locale identifiers is always preferable.</span></span>

<span data-ttu-id="da187-106">Описание идентификаторов языков см. в разделе [идентификатор языка](language-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="da187-106">See [language identifier](language-identifiers.md) for a description of language identifiers.</span></span>

<span data-ttu-id="da187-107">Идентификатор первичного или подязыка может быть определен пользователем или заранее.</span><span class="sxs-lookup"><span data-stu-id="da187-107">A primary or sublanguage identifier can be user-defined or predefined.</span></span> <span data-ttu-id="da187-108">Сведения о предопределенных основных идентификаторах языка с допустимыми идентификаторами языков см. в разделе [[MS-LCID]: Справочник по идентификатору языка (LCID) Windows](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span><span class="sxs-lookup"><span data-stu-id="da187-108">For the predefined primary language identifiers with their valid sublanguage identifiers, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span></span>

> [!Note]  
> <span data-ttu-id="da187-109">Если идентификатор языка отсутствует для использования с основным идентификатором языка, приложение должно использовать подязык **\_ по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="da187-109">If there is no sublanguage identifier to use with a primary language identifier, your application should use **SUBLANG\_DEFAULT**.</span></span> <span data-ttu-id="da187-110">Для ресурсов, которые одинаковы для всех языков основного языка, следует использовать **\_ нейтральный** языковой набор.</span><span class="sxs-lookup"><span data-stu-id="da187-110">It should use **SUBLANG\_NEUTRAL** for resources that are the same for all sublanguages of a primary language.</span></span>

<span data-ttu-id="da187-111">Определяемый пользователем основной идентификатор языка имеет значение в диапазоне от 0x0200 до 0x03ff.</span><span class="sxs-lookup"><span data-stu-id="da187-111">A user-defined primary language identifier has a value in the range 0x0200 to 0x03ff.</span></span> <span data-ttu-id="da187-112">Все остальные значения зарезервированы для использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="da187-112">All other values are reserved for operating system use.</span></span>

<span data-ttu-id="da187-113">Определяемый пользователем идентификатор языка имеет значение в диапазоне от 0x20 до 0x3F.</span><span class="sxs-lookup"><span data-stu-id="da187-113">A user-defined sublanguage identifier has a value in the range 0x20 to 0x3f.</span></span> <span data-ttu-id="da187-114">Все остальные значения зарезервированы для использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="da187-114">All other values are reserved for operating system use.</span></span>
