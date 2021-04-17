---
description: Установщик Windows может объявить о доступности приложения пользователям или другим приложениям без фактической установки приложения.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Рекламу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650734"
---
# <a name="advertisement"></a><span data-ttu-id="d05a7-103">Рекламу</span><span class="sxs-lookup"><span data-stu-id="d05a7-103">Advertisement</span></span>

<span data-ttu-id="d05a7-104">Установщик Windows может объявить о доступности приложения пользователям или другим приложениям без фактической установки приложения.</span><span class="sxs-lookup"><span data-stu-id="d05a7-104">The Windows Installer can advertise the availability of an application to users or other applications without actually installing the application.</span></span> <span data-ttu-id="d05a7-105">Если приложение объявлено, то пользователям или другим приложениям предоставляются только интерфейсы, необходимые для загрузки и запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="d05a7-105">If an application is advertised, only the interfaces required for loading and launching the application are presented to the user or other applications.</span></span> <span data-ttu-id="d05a7-106">Если пользователь или приложение активирует объявленный интерфейс, установщик продолжит установку необходимых компонентов, как описано в разделе [Установка по запросу](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="d05a7-106">If a user or application activates an advertised interface the installer then proceeds to install the necessary components as described in [Installation-On-Demand](installation-on-demand.md).</span></span>

<span data-ttu-id="d05a7-107">Два типа рекламы — это назначение и публикация.</span><span class="sxs-lookup"><span data-stu-id="d05a7-107">The two types of advertising are assigning and publishing.</span></span> <span data-ttu-id="d05a7-108">Приложение отображается как установленное для пользователя, если оно назначено пользователю.</span><span class="sxs-lookup"><span data-stu-id="d05a7-108">An application appears installed to a user when that application is assigned to the user.</span></span> <span data-ttu-id="d05a7-109">Меню **Пуск** содержит соответствующие сочетания клавиш, значки отображаются, файлы связаны с приложением, а записи реестра соответствуют установке приложения.</span><span class="sxs-lookup"><span data-stu-id="d05a7-109">The **Start** menu contains the appropriate shortcuts, icons are displayed, files are associated with the application, and registry entries reflect the application's installation.</span></span> <span data-ttu-id="d05a7-110">Когда пользователь пытается открыть назначенное приложение, он устанавливается по запросу.</span><span class="sxs-lookup"><span data-stu-id="d05a7-110">When the user tries to open an assigned application it is installed upon demand.</span></span>

<span data-ttu-id="d05a7-111">Установщик поддерживает объявление приложений и функций в соответствии с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="d05a7-111">The installer supports the advertisement of applications and features according to the operating system.</span></span> <span data-ttu-id="d05a7-112">Установщик регистрирует сведения о COM-классе для назначенных приложений, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d05a7-112">The installer registers COM class information for assigned applications beginning with Windows XP.</span></span> <span data-ttu-id="d05a7-113">Это позволяет установщику установить приложение при создании экземпляра объявленного класса.</span><span class="sxs-lookup"><span data-stu-id="d05a7-113">This enables the installer to install the application upon the creation of an instance of an advertised class.</span></span> <span data-ttu-id="d05a7-114">Дополнительные сведения см. в разделе [поддержка платформ объявления](platform-support-of-advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="d05a7-114">For more information, see [Platform Support of Advertisement](platform-support-of-advertisement.md).</span></span>

<span data-ttu-id="d05a7-115">Приложение можно опубликовать с сервера, начиная с Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d05a7-115">You can publish an application from the server beginning with Windows Server 2003.</span></span> <span data-ttu-id="d05a7-116">После этого опубликованное приложение устанавливается с помощью сопоставления файлов или типа MIME.</span><span class="sxs-lookup"><span data-stu-id="d05a7-116">The published application is then installed through its file association or Multipurpose Internet Mail Extension (MIME) type.</span></span> <span data-ttu-id="d05a7-117">Публикация не заполняет пользовательский интерфейс ни одним из значков приложения.</span><span class="sxs-lookup"><span data-stu-id="d05a7-117">Publishing does not populate the user interface with any of the application's icons.</span></span> <span data-ttu-id="d05a7-118">Клиентская операционная система может установить опубликованное приложение, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d05a7-118">The client operating system can install a published application beginning with Windows XP.</span></span>

 

 



