---
description: Чтобы воспроизвести образец, который необходимо скопировать или создать с помощью программного средства, установщик Windows файл базы данных.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Импорт пустой базы данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265417"
---
# <a name="importing-a-blank-database"></a><span data-ttu-id="d2f6e-103">Импорт пустой базы данных</span><span class="sxs-lookup"><span data-stu-id="d2f6e-103">Importing a Blank Database</span></span>

<span data-ttu-id="d2f6e-104">Чтобы воспроизвести образец, который необходимо скопировать или создать с помощью программного средства, установщик Windows файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="d2f6e-104">To reproduce the sample you need to copy, or create with a software tool, a Windows Installer database file.</span></span> <span data-ttu-id="d2f6e-105">Полностью пустая база данных установки, Schema.msi, предоставляется вместе с [компонентами Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="d2f6e-105">A totally blank installation database, Schema.msi, is provided with the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="d2f6e-106">Пакет SDK также предоставляет частично пустую базу данных uisample.msi, которая содержит предлагаемые таблицы последовательности и данные, необходимые для простого пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d2f6e-106">The SDK also provides a partially blank database, uisample.msi, that contains the suggested sequence tables and data required for a simple user interface.</span></span> <span data-ttu-id="d2f6e-107">Создайте копию uisample.msi и переместите ее в тот же каталог, где находится папка блокнота, созданная при [планировании установки](planning-the-installation.md).</span><span class="sxs-lookup"><span data-stu-id="d2f6e-107">Make a copy of uisample.msi and move it into the same directory containing the Notepad folder you created in [Planning the Installation](planning-the-installation.md).</span></span> <span data-ttu-id="d2f6e-108">Переименуйте файл MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="d2f6e-108">Rename the file MNP2000.msi.</span></span> <span data-ttu-id="d2f6e-109">Файл базы данных установки и исходные файлы должны располагаться в корне того же каталога.</span><span class="sxs-lookup"><span data-stu-id="d2f6e-109">The installation database file and the source files must both be located at the root of the same directory.</span></span> <span data-ttu-id="d2f6e-110">Пример:</span><span class="sxs-lookup"><span data-stu-id="d2f6e-110">For example:</span></span>

<span data-ttu-id="d2f6e-111">В. \\ пример \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="d2f6e-111">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="d2f6e-112">В. \\ пример \\ блокнота</span><span class="sxs-lookup"><span data-stu-id="d2f6e-112">C:\\Sample\\Notepad</span></span>\\

<span data-ttu-id="d2f6e-113">Если Uisample.msi не используется, необходимо получить пустую базу данных, например Schema.msi, и ввести сведения для установки с помощью средства редактирования базы данных, такого как Orca, которое предоставляется вместе с пакетом SDK или другим редактором базы данных.</span><span class="sxs-lookup"><span data-stu-id="d2f6e-113">If you do not use Uisample.msi, then you must obtain a blank database, such as Schema.msi, and enter information for the installation using a database editing tool such as Orca, which is provided with the SDK, or another database editor.</span></span>

[<span data-ttu-id="d2f6e-114">Продолжить</span><span class="sxs-lookup"><span data-stu-id="d2f6e-114">Continue</span></span>](specifying-directory-structure.md)

 

 



