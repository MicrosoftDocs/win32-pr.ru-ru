---
title: Доступ к Active Directory с помощью Visual Basic
description: Одной из наиболее эффективных функций, которые стали доступны в операционной системе Microsoft Windows 2000, является служба Microsoft Active Directory Directory.
ms.assetid: b5021e38-92a2-43d2-b3cb-15ff5c74c1d8
ms.tgt_platform: multiple
keywords:
- Доступ к Active Directory с помощью Visual Basic ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbc469de112c37c1c2ea5865d88252c4bd98466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067343"
---
# <a name="accessing-active-directory-using-visual-basic"></a><span data-ttu-id="7f62d-104">Доступ к Active Directory с помощью Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7f62d-104">Accessing Active Directory Using Visual Basic</span></span>

<span data-ttu-id="7f62d-105">Одной из наиболее эффективных функций, которые стали доступны в операционной системе Microsoft Windows 2000, является служба Microsoft Active Directory Directory.</span><span class="sxs-lookup"><span data-stu-id="7f62d-105">One of the most powerful features that became available with the Microsoft Windows 2000 operating system is the Microsoft Active Directory directory service.</span></span> <span data-ttu-id="7f62d-106">При входе в домен Windows 2000 Active Directory помещается в действие. для поиска ближайшего цветового принтера в здании можно использовать Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f62d-106">When you log on to a Windows 2000 domain, Active Directory is put into action; to search for the closest color printer in your building, you can use Active Directory.</span></span> <span data-ttu-id="7f62d-107">Он может использоваться для поиска в адресной книге или для поиска пользователей, работающих в здании 40.</span><span class="sxs-lookup"><span data-stu-id="7f62d-107">It can be used for an address book lookup or a search for users who work in building 40.</span></span> <span data-ttu-id="7f62d-108">С Active Directory можно использовать смарт-карту для входа в домен Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7f62d-108">With Active Directory, you can use a smart card to log on to a Windows 2000 domain.</span></span> <span data-ttu-id="7f62d-109">Можно даже присоединять данные из программного обеспечения базы данных Microsoft SQL Server и Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f62d-109">You can even join data from Microsoft SQL Server database software and Active Directory.</span></span>

<span data-ttu-id="7f62d-110">Многие другие технологии Майкрософт, такие как сервер очереди сообщений Майкрософт (MSMQ), COM (хранилище классов), протокол IPsec, групповая политика объекты (GPO) и Exchange, интегрированы с Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f62d-110">Many other Microsoft technologies, such as Microsoft Message Queue Server (MSMQ), COM (Class Store), Internet Protocol security (IPsec), Group Policy Objects (GPOs), and Exchange are integrated with Active Directory.</span></span>

<span data-ttu-id="7f62d-111">В этом разделе описано, как использовать интерфейсы Active Directory служб (ADSI) для доступа к Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f62d-111">This section discusses how to use the Active Directory Service Interfaces (ADSI) to access Active Directory.</span></span> <span data-ttu-id="7f62d-112">Использование сценария для вымышленной компании — корпорации Fabrikam — вы узнаете, как выполнять некоторые базовые задачи администрирования.</span><span class="sxs-lookup"><span data-stu-id="7f62d-112">Using a scenario for a fictitious company — the Fabrikam Corporation — you will learn how to perform some basic administrative tasks.</span></span>

<span data-ttu-id="7f62d-113">По мере выполнения этого сценария примеры кода в каждом разделе будут создаваться по отдельности.</span><span class="sxs-lookup"><span data-stu-id="7f62d-113">As you progress through this scenario, the code examples in each section build upon themselves.</span></span>

<span data-ttu-id="7f62d-114">Для краткости все примеры кода написаны с помощью системы разработки Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7f62d-114">For brevity, all code examples are written with the Microsoft Visual Basic development system.</span></span> <span data-ttu-id="7f62d-115">Дополнительные сведения о преобразовании C++ см. [в статье сопоставление кода Visual Basic ADSI с кодом c++](mapping-adsi-visual-basic-code-to-c-code.md).</span><span class="sxs-lookup"><span data-stu-id="7f62d-115">For more information about C++ conversion, see [Mapping ADSI Visual Basic Code to C++ Code](mapping-adsi-visual-basic-code-to-c-code.md).</span></span>

 

 




