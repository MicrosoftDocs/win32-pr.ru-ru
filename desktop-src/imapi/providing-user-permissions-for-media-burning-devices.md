---
title: Предоставление пользователям разрешений для устройств записи мультимедиа
description: По умолчанию Windows Vista и Windows Server 2008 предоставляют администраторам и пользователям доступ на чтение и запись для пользователей, которые регистрируются непосредственно на компьютере (промежуточные пользователи).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "104273183"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a><span data-ttu-id="92085-103">Предоставление пользователям разрешений для устройств записи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="92085-103">Providing User Permissions for Media Burning Devices</span></span>

<span data-ttu-id="92085-104">По умолчанию Windows Vista и Windows Server 2008 предоставляют администраторам и пользователям доступ на чтение и запись для пользователей, которые регистрируются непосредственно на компьютере (промежуточные пользователи).</span><span class="sxs-lookup"><span data-stu-id="92085-104">By default, both Windows Vista and Windows Server 2008 grant read/write access to administrators and users logged directly into the machine (intermediate users).</span></span> <span data-ttu-id="92085-105">Однако в Windows XP и Windows Server 2003 администратор должен предоставить этим устройствам права на чтение и запись для других групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="92085-105">However, in Windows XP and Windows Server 2003 an administrator must grant these device read/write privileges to other user groups.</span></span>

<span data-ttu-id="92085-106">Администратор может настроить определенные разрешения устройства для опытных пользователей и интерактивных пользователей.</span><span class="sxs-lookup"><span data-stu-id="92085-106">An administrator may adjust specific device-related permissions for power users and interactive users.</span></span>

<span data-ttu-id="92085-107">Чтобы открыть соответствующую панель разрешений группы в Windows XP, нажмите кнопку **Пуск**, выберите команду **выполнить**, введите **gpedit. msc** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="92085-107">To reach the appropriate group permissions panel in Windows XP, click **Start**, click **Run**, type **gpedit.msc**, and then click **OK**.</span></span> <span data-ttu-id="92085-108">В интерфейсе групповая политика разверните узел **Конфигурация компьютера**, разверните узел **Параметры Windows**, разверните узел **Параметры безопасности**, разверните узел **Локальные политики** и дважды щелкните **Параметры безопасности**.</span><span class="sxs-lookup"><span data-stu-id="92085-108">In the Group Policy interface, expand **Computer Configuration**, expand **Windows Settings**, expand **Security Settings**, expand **Local Policies**, and double-click **Security Options**.</span></span>

![Снимок экрана, на котором показано окно "групповая политика" с политикой, выбранной на панели "политика".](images/gpolpanel.jpg)

<span data-ttu-id="92085-110">На этой панели администратор должен указать параметры двух параметров устройства, чтобы предоставить необходимые разрешения группы.</span><span class="sxs-lookup"><span data-stu-id="92085-110">At this panel, an administrator must specify the settings of two device options to provide the required group permissions:</span></span>

-   <span data-ttu-id="92085-111">Установите флажок "устройства: разрешить доступ к компакт-ДИСКам только для локального пользователя", чтобы **включить**</span><span class="sxs-lookup"><span data-stu-id="92085-111">Set "Devices: Restrict CD-ROM access to locally logged-on user only" to **Enabled**</span></span>
-   <span data-ttu-id="92085-112">Настройка "устройства: разрешено форматировать и извлекать съемные носители" для **администраторов и опытных пользователей**.</span><span class="sxs-lookup"><span data-stu-id="92085-112">Set "Devices: Allowed to format and eject removable media" to **Administrators and Power Users**.</span></span> <span data-ttu-id="92085-113">Можно также эмулировать разрешения Windows Vista, установив для этого параметра значение **Администраторы и интерактивные пользователи**.</span><span class="sxs-lookup"><span data-stu-id="92085-113">It is also possible to emulate Windows Vista permissions by setting this option to **Administrators and Interactive Users**.</span></span>

<span data-ttu-id="92085-114">Хотя конкретный пользовательский интерфейс не существует в Windows XP или Windows Server 2003 для использования [**сетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) или [Сетупдисетдевицерегистрипроперти](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), эти API-интерфейсы можно использовать для предоставления пользовательских групп разрешений на устройства.</span><span class="sxs-lookup"><span data-stu-id="92085-114">While a specific UI does not exist in Windows XP or Windows Server 2003 for the use of [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) or [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), it is possible to use these APIs to grant custom user groups device permissions.</span></span> <span data-ttu-id="92085-115">Например, вызов **сетсекуритинфо** предоставит разрешения группам пользователей.</span><span class="sxs-lookup"><span data-stu-id="92085-115">For example, a call to **SetSecurityInfo** will grant permissions to user groups.</span></span> <span data-ttu-id="92085-116">Изменения разрешений с помощью этого API являются временными и не будут сохранены при перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="92085-116">Permission changes with this API are temporary and will not persist across a reboot.</span></span> <span data-ttu-id="92085-117">Однако при вызове [сетупдисетдевицерегистрипроперти](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) будут реализованы изменения разрешений в реестре, которые будут сохраняться во время перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="92085-117">However, calling [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) will implement the permission changes in the registry, which will persist across a reboot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92085-118">См. также</span><span class="sxs-lookup"><span data-stu-id="92085-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92085-119">Использование IMAPI</span><span class="sxs-lookup"><span data-stu-id="92085-119">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="92085-120">**сетсекуритинфо**</span><span class="sxs-lookup"><span data-stu-id="92085-120">**SetSecurityInfo**</span></span>](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[<span data-ttu-id="92085-121">сетупдисетдевицерегистрипроперти</span><span class="sxs-lookup"><span data-stu-id="92085-121">SetupDiSetDeviceRegistryProperty</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 