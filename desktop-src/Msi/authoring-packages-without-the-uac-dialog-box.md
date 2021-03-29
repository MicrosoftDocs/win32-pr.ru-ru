---
description: Если для установки пакета установщик Windows не требуются повышенные привилегии, автор пакета может отключить диалоговое окно, отображаемое системой контроля учетных записей (UAC), чтобы запрашивать у пользователей разрешение на авторизацию администратора.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Создание пакетов без диалогового окна UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813329"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a><span data-ttu-id="208f7-103">Создание пакетов без диалогового окна UAC</span><span class="sxs-lookup"><span data-stu-id="208f7-103">Authoring Packages without the UAC Dialog Box</span></span>

<span data-ttu-id="208f7-104">Если для установки пакета установщик Windows не требуются повышенные привилегии, автор пакета может отключить диалоговое окно, отображаемое [*системой контроля учетных записей*](u-gly.md) (UAC), чтобы запрашивать у пользователей разрешение на авторизацию администратора.</span><span class="sxs-lookup"><span data-stu-id="208f7-104">When elevated privileges are not required to install a Windows Installer package, the author of the package can suppress the dialog box that [*User Account Control*](u-gly.md) (UAC) displays to prompt users for administrator authorization.</span></span>

<span data-ttu-id="208f7-105">Чтобы отключить отображение диалогового окна UAC при установке приложения, автор пакета должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="208f7-105">To suppress the display of the UAC dialog box when installing the application, the author of the package should do the following:</span></span>

-   <span data-ttu-id="208f7-106">Установите приложение с помощью установщика Window 4,0 или более поздней версии в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="208f7-106">Install the application using Window Installer 4.0 or later on Windows Vista.</span></span>
-   <span data-ttu-id="208f7-107">Не зависят от использования системных привилегий с повышенными правами для установки приложения на компьютере.</span><span class="sxs-lookup"><span data-stu-id="208f7-107">Do not depend on using elevated system privileges to install the application on the computer.</span></span>
-   <span data-ttu-id="208f7-108">Установите приложение в контексте для каждого пользователя и сделайте его контекстом установки по умолчанию для пакета.</span><span class="sxs-lookup"><span data-stu-id="208f7-108">Install the application in the per-user context and make this the default installation context of the package.</span></span> <span data-ttu-id="208f7-109">Если свойство [**ALLUSERS**](allusers.md) не задано, установщик устанавливает пакет в контексте для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="208f7-109">If the [**ALLUSERS**](allusers.md) property is not set, the installer installs the package in the per-user context.</span></span> <span data-ttu-id="208f7-110">Если свойство **ALLUSERS** не включено в [таблицу свойств](property-table.md), установщик не задает это свойство, и поэтому установка на уровне пользователя станет контекстом установки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="208f7-110">If you do not include the **ALLUSERS** property in the [Property table](property-table.md), the installer does not set this property and so per-user installation becomes the default installation context.</span></span> <span data-ttu-id="208f7-111">Это значение по умолчанию можно переопределить, задав свойство **ALLUSERS** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="208f7-111">You can override this default by setting the **ALLUSERS** property on the command line.</span></span>
-   <span data-ttu-id="208f7-112">Установите бит 3 в свойстве " [**Сводка слов**](word-count-summary.md) ", чтобы указать, что для установки приложения не требуются повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="208f7-112">Set Bit 3 in the [**Word Count Summary**](word-count-summary.md) property to indicate that elevated privileges are not required to install the application.</span></span>

 

 



