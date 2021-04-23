---
description: В этом примере показано, как локализовать пакет установщик Windows, описанный в примере установки. Исходный пакет установки изменен с английского на французскую языковую версию.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Пример локализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662980"
---
# <a name="a-localization-example"></a><span data-ttu-id="425df-104">Пример локализации</span><span class="sxs-lookup"><span data-stu-id="425df-104">A Localization Example</span></span>

<span data-ttu-id="425df-105">В этом примере показано, как локализовать пакет установщик Windows, описанный в [примере установки](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="425df-105">This example illustrates how to localize the Windows Installer package described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="425df-106">Исходный пакет установки изменен с английского на французскую языковую версию.</span><span class="sxs-lookup"><span data-stu-id="425df-106">The original installation package is changed from an English into French language version.</span></span>

<span data-ttu-id="425df-107">Пример локализации имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="425df-107">The localization sample has the following specifications:</span></span>

-   <span data-ttu-id="425df-108">Пользовательский интерфейс установки MNP2000 приложения следует изменить с английского на французский.</span><span class="sxs-lookup"><span data-stu-id="425df-108">The installation UI for the application MNP2000 should be changed from English to French.</span></span>
-   <span data-ttu-id="425df-109">Французская версия MNP2000 включает Readme.txt и Help.txt файлы, написанные на французском языке.</span><span class="sxs-lookup"><span data-stu-id="425df-109">The French version of MNP2000 includes Readme.txt and Help.txt files written in the French language.</span></span>
-   <span data-ttu-id="425df-110">Версия на французском языке включает список агентов путешествий в Франции, которые могут предоставлять билеты в красный парк.</span><span class="sxs-lookup"><span data-stu-id="425df-110">The French version includes a list of travel agents in France that can provide tickets to Red Park Arena.</span></span> <span data-ttu-id="425df-111">Этот список (представленный в виде нового файла, Fre.txt) не является частью английской версии.</span><span class="sxs-lookup"><span data-stu-id="425df-111">This list (provided as a new file, Fre.txt) is not a part of the English version.</span></span>

<span data-ttu-id="425df-112">Общая процедура локализации установки описана в разделе [локализация пакета установщик Windows](localizing-a-windows-installer-package.md).</span><span class="sxs-lookup"><span data-stu-id="425df-112">The general procedure for localizing an installation is described in the section [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="425df-113">Скопируйте английскую версию MNP2000.msi и все исходные файлы, описанные в разделе [Планирование установки](planning-the-installation.md) в новую папку.</span><span class="sxs-lookup"><span data-stu-id="425df-113">Copy the English version of MNP2000.msi and all the source files described in [Planning the Installation](planning-the-installation.md) into a new folder.</span></span> <span data-ttu-id="425df-114">Измените имя MNP2000.msi в папке на MNPFren.msi.</span><span class="sxs-lookup"><span data-stu-id="425df-114">Change the name of the MNP2000.msi in the folder to MNPFren.msi.</span></span> <span data-ttu-id="425df-115">В следующих разделах эта копия будет изменена для локализации приложения на французский.</span><span class="sxs-lookup"><span data-stu-id="425df-115">In the following sections you will modify this copy to localize the application into French.</span></span>

[<span data-ttu-id="425df-116">Продолжить</span><span class="sxs-lookup"><span data-stu-id="425df-116">Continue</span></span>](checking-the-installation-database-code-page.md)

 

 



