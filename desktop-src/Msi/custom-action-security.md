---
description: Установщик по умолчанию запускает настраиваемые действия с правами пользователя, чтобы ограничить доступ к системе настраиваемых действий.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Безопасность настраиваемых действий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7d36e0e5c6cecc61730144fb7efdeed63ba0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349762"
---
# <a name="custom-action-security"></a><span data-ttu-id="2b8de-103">Безопасность настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="2b8de-103">Custom Action Security</span></span>

<span data-ttu-id="2b8de-104">Установщик по умолчанию запускает настраиваемые действия с правами пользователя, чтобы ограничить доступ к системе настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="2b8de-104">The installer runs custom actions with user privileges by default in order to limit the access of custom actions to the system.</span></span> <span data-ttu-id="2b8de-105">Установщик может выполнять пользовательские действия с повышенными привилегиями при установке управляемого приложения или при указании системной политики для повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="2b8de-105">The installer may run custom actions with elevated privileges if a managed application is being installed or if the system policy has been specified for elevated privileges.</span></span>

<span data-ttu-id="2b8de-106">Чтобы предотвратить ведение журнала конфиденциальной информации, используемой настраиваемым действием, следует использовать свойство [**мсихидденпропертиес**](msihiddenproperties.md) и **мсидбкустомактионтипехидетаржет** .</span><span class="sxs-lookup"><span data-stu-id="2b8de-106">You should use the [**MsiHiddenProperties**](msihiddenproperties.md) property and **msidbCustomActionTypeHideTarget** to prevent logging of sensitive information used by the custom action.</span></span> <span data-ttu-id="2b8de-107">Дополнительные сведения о **мсидбкустомактионтипехидетаржет** см. в разделе [параметр скрытого целевого объекта действия](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="2b8de-107">For more information about **msidbCustomActionTypeHideTarget** see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

<span data-ttu-id="2b8de-108">Очистите свойство CustomActionData после его установки, чтобы убедиться, что конфиденциальные данные больше не доступны.</span><span class="sxs-lookup"><span data-stu-id="2b8de-108">Clear the CustomActionData property after setting it to ensure that sensitive data is no longer available.</span></span> <span data-ttu-id="2b8de-109">Ниже приведен фрагмент кода, используемый непосредственным настраиваемым действием DLL, которое настраивает данные для использования отложенным пользовательским действием с именем "Мидеферредка":</span><span class="sxs-lookup"><span data-stu-id="2b8de-109">Example code below is a snippet used by an immediate DLL custom action that is setting up data for use by a deferred custom action called "MyDeferredCA":</span></span>


```C++
#include <windows.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall MyImmediateCA(MSIHANDLE hInstall)
{
    // set up information for deferred custom action called MyDeferredCA
    const TCHAR szValue[] = TEXT("data");
    UINT uiStat = ERROR_INSTALL_FAILURE;
    if (ERROR_SUCCESS == MsiSetProperty(hInstall, TEXT("MyDeferredCA"), szValue))
    {
        uiStat = MsiDoAction(hInstall, TEXT("MyDeferredCA"));

        // clear CustomActionData property
        if (ERROR_SUCCESS != MsiSetProperty(hInstall, TEXT("MyDeferredCA"), TEXT("")))
            return ERROR_INSTALL_FAILURE;
    }

    return (uiStat == ERROR_SUCCESS) ? uiStat : ERROR_INSTALL_FAILURE;    
}
```



<span data-ttu-id="2b8de-110">Обратите внимание, что только [отложенные настраиваемые действия выполнения](deferred-execution-custom-actions.md) могут использовать атрибут **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="2b8de-110">Note that only [deferred execution custom actions](deferred-execution-custom-actions.md) can use the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="2b8de-111">Дополнительные сведения см. в разделе [настраиваемое действие In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="2b8de-111">For more information see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="2b8de-112">Если бит **msidbCustomActionTypeNoImpersonate** не задан для настраиваемого действия, установщик запускает пользовательское действие с привилегиями уровня пользователя.</span><span class="sxs-lookup"><span data-stu-id="2b8de-112">If the **msidbCustomActionTypeNoImpersonate** bit is not set for a custom action, the installer runs the custom action with user-level privileges.</span></span> <span data-ttu-id="2b8de-113">Дополнительные сведения см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="2b8de-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="2b8de-114">Если установлен бит **msidbCustomActionTypeNoImpersonate** , а управляемое приложение устанавливается с правами администратора, то установщик может запустить настраиваемое действие с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="2b8de-114">If the **msidbCustomActionTypeNoImpersonate** bit is set and a managed application is being installed with administrator permission, the installer may run the custom action with elevated privileges.</span></span> <span data-ttu-id="2b8de-115">Однако если пользователь пытается установить управляемое приложение без разрешения администратора, установщик запускает приложение с правами доступа на уровне пользователя независимо от того, задано ли **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="2b8de-115">However, if a user attempts to install the managed application without administrator permission, the installer runs the application with user level privileges regardless of whether **msidbCustomActionTypeNoImpersonate** is set.</span></span>

<span data-ttu-id="2b8de-116">Обратите внимание, что пользовательское действие может выполняться с системными привилегиями, даже если бит **msidbCustomActionTypeNoImpersonate** не установлен.</span><span class="sxs-lookup"><span data-stu-id="2b8de-116">Note that a custom action may run with system privileges even when the **msidbCustomActionTypeNoImpersonate** bit is not set.</span></span> <span data-ttu-id="2b8de-117">Это происходит, если администратор устанавливает приложение для всех пользователей на сервере, на котором запущена служба роли сервера терминалов, с помощью Windows 2000, и действие не помечено как **мсидбкустомактионтипетсаваре**.</span><span class="sxs-lookup"><span data-stu-id="2b8de-117">This occurs if an administrator installs the application for all users on a server running the Terminal Server role service using Windows 2000 and the action is not marked with **msidbCustomActionTypeTSAware**.</span></span> <span data-ttu-id="2b8de-118">Пользовательское действие может также выполняться с системными привилегиями, если установка вызывается при отсутствии контекста пользователя.</span><span class="sxs-lookup"><span data-stu-id="2b8de-118">A custom action may also run with system privileges if the installation is invoked when there is no user context.</span></span> <span data-ttu-id="2b8de-119">Например, если в данный момент во время установки, вызванного развертыванием приложения Windows 2000, пользователь не вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="2b8de-119">For example, if there is no currently logged-on user during an installation invoked by Windows 2000 Application Deployment.</span></span>

<span data-ttu-id="2b8de-120">При создании собственных настраиваемых действий всегда следует создавать пользовательские действия с помощью защищенных методов.</span><span class="sxs-lookup"><span data-stu-id="2b8de-120">When creating your own custom actions, you should always author the custom action using secure methods.</span></span> <span data-ttu-id="2b8de-121">Дополнительные сведения см. в разделе [рекомендации по защите настраиваемых действий](guidelines-for-securing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="2b8de-121">For more information, see [Guidelines for Securing Custom Actions](guidelines-for-securing-custom-actions.md).</span></span>

 

 



