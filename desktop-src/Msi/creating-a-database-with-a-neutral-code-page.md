---
description: Рекомендуемый подход к обработке кодовых страниц заключается в создании нейтральной базовой базы данных, которая содержит только символы, которые можно преобразовать в любую кодовую страницу.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Создание базы данных со нейтральной кодовой страницей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080932"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a><span data-ttu-id="b8286-103">Создание базы данных со нейтральной кодовой страницей</span><span class="sxs-lookup"><span data-stu-id="b8286-103">Creating a Database with a Neutral Code Page</span></span>

<span data-ttu-id="b8286-104">Рекомендуемый подход к обработке кодовых страниц заключается в создании нейтральной базовой базы данных, которая содержит только символы, которые можно преобразовать в любую кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="b8286-104">The recommended approach for handling code pages is to author a neutral base database that only contains characters that can be translated into any code page.</span></span> <span data-ttu-id="b8286-105">Затем в базе данных можно задать кодовую страницу локализации, а также добавить сведения о локализации, как описано в разделе [локализация пакета установщик Windows](localizing-a-windows-installer-package.md).</span><span class="sxs-lookup"><span data-stu-id="b8286-105">The database may then be set to the code page of the localization and the localization information can be added as described in [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="b8286-106">Чтобы создать нейтральную базу данных, Избегайте использования дополнительных символов, не принадлежащих кодировке ASCII, и, следовательно, требуется специальная кодовая страница.</span><span class="sxs-lookup"><span data-stu-id="b8286-106">To author a neutral database, avoid extended characters that do not belong to the ASCII character set and therefore require a special code page.</span></span> <span data-ttu-id="b8286-107">Например, знак авторского права, © и зарегистрированный знак товарного знака,, не символы ASCII, и для правильного показа требуется специальная кодовая страница ANSI.</span><span class="sxs-lookup"><span data-stu-id="b8286-107">For example, the copyright sign, ©, and the registered trademark sign, , are not ASCII characters, and require a special ANSI code page for proper display.</span></span> <span data-ttu-id="b8286-108">Вместо этого используйте (c) и (r), так как эти символы можно преобразовать в символы для английской версии языка.</span><span class="sxs-lookup"><span data-stu-id="b8286-108">Instead use (c) and (r), because these characters can be translated or transformed to the symbols for the English-language version.</span></span> <span data-ttu-id="b8286-109">Эта нейтральная база данных затем может быть локализована путем установки ее кодовой страницы и добавления сведений о локализации путем редактирования таблицы или импорта текстовых файлов архива.</span><span class="sxs-lookup"><span data-stu-id="b8286-109">This neutral database can then be localized by setting its code page and adding localization information by table editing or by importing text archive files.</span></span>

 

 



