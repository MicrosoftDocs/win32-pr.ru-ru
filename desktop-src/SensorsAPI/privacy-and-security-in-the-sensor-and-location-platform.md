---
description: Платформа датчиков и расположения Windows включает параметры конфиденциальности для защиты персональных данных пользователей.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Конфиденциальность и безопасность на платформе датчиков и расположений Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662276"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a><span data-ttu-id="c4a5a-103">Конфиденциальность и безопасность на платформе датчиков и расположений Windows</span><span class="sxs-lookup"><span data-stu-id="c4a5a-103">Privacy and Security in the Windows Sensor and Location Platform</span></span>

<span data-ttu-id="c4a5a-104">Платформа датчиков и расположения Windows включает параметры конфиденциальности для защиты персональных данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-104">The Windows Sensor and Location platform includes privacy settings to help protect users' personal information.</span></span>

<span data-ttu-id="c4a5a-105">Платформа гарантирует, что данные датчиков остаются закрытыми, если требуется конфиденциальность, в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-105">The platform helps to ensure that sensor data remains private, when privacy is required, in the following ways:</span></span>

-   <span data-ttu-id="c4a5a-106">По умолчанию датчики отключены.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-106">By default, sensors are off.</span></span> <span data-ttu-id="c4a5a-107">Поскольку структура платформы предполагает, что любой датчик может предоставлять персональные данные, каждый датчик отключается до тех пор, пока пользователь не предоставит явное согласие на доступ к данным датчика.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-107">Because the platform design presumes that any sensor can provide personal data, each sensor is disabled until the user provides explicit consent to access the sensor data.</span></span>
-   <span data-ttu-id="c4a5a-108">Windows предоставляет сообщения о раскрытии и содержимое справки для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-108">Windows provides disclosure messages and Help content for the user.</span></span> <span data-ttu-id="c4a5a-109">Это содержимое помогает пользователям понять, как датчики могут влиять на конфиденциальность их персональных данных и помогают принимать взвешенные решения.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-109">This content helps users understand how sensors can affect the privacy of their personal data and helps users make informed decisions.</span></span>
-   <span data-ttu-id="c4a5a-110">Для предоставления разрешения на датчик требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-110">Providing permission for a sensor requires administrator rights.</span></span>
-   <span data-ttu-id="c4a5a-111">Если он включен, устройство датчика работает для всех программ, работающих под определенной учетной записью пользователя (или для всех учетных записей пользователей).</span><span class="sxs-lookup"><span data-stu-id="c4a5a-111">When it is enabled, a sensor device works for all programs running under a particular user account (or for all user accounts).</span></span> <span data-ttu-id="c4a5a-112">Сюда входят неинтерактивные пользователи и службы, такие как ASPNET или SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-112">This includes noninteractive users and services, such as ASPNET or SYSTEM.</span></span> <span data-ttu-id="c4a5a-113">Например, если для учетной записи пользователя включен датчик GPS, доступ к GPS будут иметь только программы, работающие под учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-113">For example, if you enable a GPS sensor for your user account, only programs running under your user account have access to the GPS.</span></span> <span data-ttu-id="c4a5a-114">Если включить GPS для всех пользователей, любая программа, работающая с любой учетной записью пользователя, имеет доступ к GPS.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-114">If you enable the GPS for all users, any program running under any user account has access to the GPS.</span></span>
-   <span data-ttu-id="c4a5a-115">Программы, использующие датчики, могут вызывать метод для открытия диалогового окна системы, предлагающего пользователям включить необходимые устройства датчиков.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-115">Programs that use sensors can call a method to open a system dialog box that prompts users to enable needed sensor devices.</span></span> <span data-ttu-id="c4a5a-116">Эта функция упрощает для разработчиков и пользователей обеспечение работы датчиков при их необходимости, сохраняя при этом пользовательский контроль над раскрытием данных датчика.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-116">This feature makes it easy for developers and users to make sure that sensors work when programs need them, while maintaining user control of disclosure of sensor data.</span></span>
-   <span data-ttu-id="c4a5a-117">Драйверы датчика используют специальный объект, который обрабатывает все запросы ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-117">Sensor drivers use a special object that processes all I/O requests.</span></span> <span data-ttu-id="c4a5a-118">Этот объект гарантирует, что доступ к данным датчика могут получить только программы, имеющие разрешение пользователя.</span><span class="sxs-lookup"><span data-stu-id="c4a5a-118">This object makes sure that only programs that have user permission can access sensor data.</span></span>

 

 



