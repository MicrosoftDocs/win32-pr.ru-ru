---
description: При создании INF-файла для приложения установки также следует обращаться к формату INF-файла, который описан в общих рекомендациях по разделам INF-файлов и INF-файлов и директивам пакета средств разработки драйверов для Microsoft Windows 2000.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Создание файла INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662336"
---
# <a name="authoring-an-inf-file"></a><span data-ttu-id="ec1c8-103">Создание файла INF</span><span class="sxs-lookup"><span data-stu-id="ec1c8-103">Authoring an INF file</span></span>

<span data-ttu-id="ec1c8-104">При создании INF-файла для приложения установки также следует обращаться к формату INF-файла, который описан в *общих рекомендациях по* РАЗДЕЛам INF-файлов и INF-файлов и *директивам* пакета средств разработки драйверов для Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-104">When authoring an INF file for a Setup application you should also refer to the INF file format documented in *General Guidelines for INF Files* and *INF File Sections and Directives* of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="ec1c8-105">При создании INF-файлов для приложения установки придерживайтесь следующих правил.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-105">When authoring INF files for a setup application adhere to the following rules.</span></span>

-   <span data-ttu-id="ec1c8-106">В каждом INF-файле требуется раздел **версии** .</span><span class="sxs-lookup"><span data-stu-id="ec1c8-106">A **Version** section is required in every INF file.</span></span>
-   <span data-ttu-id="ec1c8-107">Разделы должны начинаться с имени раздела, заключенного в квадратные скобки ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="ec1c8-107">Sections must begin with the section name enclosed by square brackets (\[\]).</span></span>
-   <span data-ttu-id="ec1c8-108">Имена разделов **дестинатиондирс**, **саурцедисксфилес**, **саурцедискснамес**, **Strings** и **Version** должны быть идентичны типу раздела.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-108">Names of **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings**, and **Version** sections must be identical to the section type.</span></span> <span data-ttu-id="ec1c8-109">Например, используйте \[ дестинатиондирс \] .</span><span class="sxs-lookup"><span data-stu-id="ec1c8-109">For example use \[DestinationDirs\].</span></span> <span data-ttu-id="ec1c8-110">Авторы могут указывать имена других типов разделов.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-110">Authors may specify the names of other types of sections.</span></span>
-   <span data-ttu-id="ec1c8-111">К именам разделов **саурцедискснамес** и **саурцедисксфилес** можно добавить суффикс, зависящий от платформы.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-111">Names of **SourceDisksNames** and **SourceDisksFiles** sections may be appended with a platform-specific suffix.</span></span> <span data-ttu-id="ec1c8-112">Например, чтобы отобразить раздел **саурцедискснамес** , относящийся к Intel, используйте \[ саурцедискснамес. x86 \] .</span><span class="sxs-lookup"><span data-stu-id="ec1c8-112">For example, to show an Intel-specific **SourceDisksNames** section use \[SourceDisksNames.x86\].</span></span> <span data-ttu-id="ec1c8-113">Если функции настройки находят разделы **саурцедискснамес** и **саурцедисксфилес** , относящиеся к платформе, соответствующие платформе пользователя, функции используют разделы, относящиеся к конкретной платформе.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-113">If the setup functions find platform-specific **SourceDisksNames** and **SourceDisksFiles** sections matching the user's platform, the functions use the platform-specific sections.</span></span> <span data-ttu-id="ec1c8-114">В противном случае функции установки используют разделы **саурцедискснамес** и **саурцедисксфилес** , не имеющие суффикса.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-114">Otherwise the setup functions use the non-suffixed **SourceDisksNames** and **SourceDisksFiles** sections.</span></span> <span data-ttu-id="ec1c8-115">Функции установки могут программно определять систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-115">The setup functions can programmatically determine the user's system.</span></span> <span data-ttu-id="ec1c8-116">См. [Пример разделов INF саурцедискснамес и саурцедисксфилес](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span><span class="sxs-lookup"><span data-stu-id="ec1c8-116">See the [INF SourceDisksNames and SourceDisksFiles Sections Example](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span></span>
-   <span data-ttu-id="ec1c8-117">Значения могут быть выражены в виде заменяемых строк с помощью формы%*стркэй*%.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-117">Values may be expressed as replaceable strings using the form %*strkey*%.</span></span> <span data-ttu-id="ec1c8-118">Чтобы использовать символ% в строке, используйте%%.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-118">To use a % character in the string, use %%.</span></span> <span data-ttu-id="ec1c8-119">Стркэй должен быть определен в разделе **Strings** файла INF.</span><span class="sxs-lookup"><span data-stu-id="ec1c8-119">The strkey must be defined in a **Strings** section of the INF file.</span></span>

 

 



