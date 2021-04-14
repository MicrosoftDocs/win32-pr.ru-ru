---
description: Значение свойства сводки номера редакции в потоке сводных данных должно быть изменено на новое уникальное значение при локализации базы данных, так как база данных установки изменяется. См. раздел коды пакетов.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Обновление потока сводных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c022023f79d8f4d3999db6e11e4cf65b73e1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424041"
---
# <a name="updating-a-summary-information-stream"></a><span data-ttu-id="13e7c-104">Обновление потока сводных данных</span><span class="sxs-lookup"><span data-stu-id="13e7c-104">Updating a Summary Information Stream</span></span>

<span data-ttu-id="13e7c-105">Значение свойства [**сводки номера редакции**](revision-number-summary.md) в [потоке сводных данных](summary-information-stream.md) должно быть изменено на новое уникальное значение при локализации базы данных, так как база данных установки изменяется.</span><span class="sxs-lookup"><span data-stu-id="13e7c-105">The value of the [**Revision Number Summary**](revision-number-summary.md) Property in the [summary information stream](summary-information-stream.md) must be changed to a new, unique value when localizing a database, because the installation database is being changed.</span></span> <span data-ttu-id="13e7c-106">См. раздел [коды пакетов](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="13e7c-106">See [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="13e7c-107">Значение свойства [**Сводка шаблона**](template-summary.md) в потоке сводных данных должно быть изменено на числовой идентификатор языка (LangID) нового языка.</span><span class="sxs-lookup"><span data-stu-id="13e7c-107">The value of the [**Template Summary**](template-summary.md) Property in the summary information stream must be changed to the numeric language identifier (LANGID) of the new language.</span></span>

<span data-ttu-id="13e7c-108">Если текстовые строки с описанием в потоке сводных данных локализованы на новый язык, для свойства « [**Сводка кодовой**](codepage-summary.md) страницы» необходимо задать правильную кодовую страницу для нового языка.</span><span class="sxs-lookup"><span data-stu-id="13e7c-108">If the descriptive text strings in the summary information stream are localized to the new language, the [**Codepage Summary**](codepage-summary.md) Property must be set to the correct code page for the new language.</span></span>

<span data-ttu-id="13e7c-109">Вы можете изменить поток сводных данных локализованного пакета с помощью той же процедуры, что и при [добавлении сводных данных](adding-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="13e7c-109">You may modify the summary information stream of the localized package by the same procedure as in [Adding Summary Information](adding-summary-information.md).</span></span> <span data-ttu-id="13e7c-110">Пример, демонстрирующий использование методов сводки базы данных, также предоставляется в установщик Windows SDK в качестве служебной WiSumInf.vbs.</span><span class="sxs-lookup"><span data-stu-id="13e7c-110">An example demonstrating the use of the database summary information methods is also provided in the Windows Installer SDK as the utility WiSumInf.vbs.</span></span> <span data-ttu-id="13e7c-111">Дополнительные сведения о WiSumInf.vbs см. в разделе [Управление сводными сведениями](manage-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="13e7c-111">For more information about WiSumInf.vbs, see [Manage Summary Information](manage-summary-information.md).</span></span>

[<span data-ttu-id="13e7c-112">Продолжить</span><span class="sxs-lookup"><span data-stu-id="13e7c-112">Continue</span></span>](adding-localized-resources.md)

 

 



