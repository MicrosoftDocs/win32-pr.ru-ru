---
title: Установка метода EAP
description: Следуйте приведенным ниже инструкциям, чтобы установить реализованный пользователем метод EAP на клиентском компьютере с EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790866"
---
# <a name="installing-an-eap-method"></a><span data-ttu-id="7ac5b-103">Установка метода EAP</span><span class="sxs-lookup"><span data-stu-id="7ac5b-103">Installing an EAP Method</span></span>

<span data-ttu-id="7ac5b-104">Следуйте приведенным ниже инструкциям, чтобы установить реализованный пользователем метод EAP на клиентском компьютере с EAPHost.</span><span class="sxs-lookup"><span data-stu-id="7ac5b-104">Follow the instructions below to install a user-implemented EAP method on a client computer running EAPHost.</span></span>

-   <span data-ttu-id="7ac5b-105">Реализуйте [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) для библиотеки DLL метода EAP.</span><span class="sxs-lookup"><span data-stu-id="7ac5b-105">Implement [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) for your EAP Method DLL.</span></span> <span data-ttu-id="7ac5b-106">Эти функции добавляют и удаляют соответствующие разделы реестра для метода EAP во время установки и (удаления) процесса.</span><span class="sxs-lookup"><span data-stu-id="7ac5b-106">These functions add and remove the appropriate registry keys for your EAP method during the installation and (uninstallation) process.</span></span>

    <span data-ttu-id="7ac5b-107">Сведения о конкретных разделах реестра, связанных с установкой метода EAP, см. в разделе [Настройка реестра для методов EAP](registry-keys-for-eap-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="7ac5b-107">For information on the specific registry keys associated with the installation of an EAP method, see the [Registry Configuration for EAP Methods](registry-keys-for-eap-methods.md) topic.</span></span>

-   <span data-ttu-id="7ac5b-108">Установите библиотеку DLL, содержащую реализацию метода EAP, с помощью следующей команды консоли.</span><span class="sxs-lookup"><span data-stu-id="7ac5b-108">Install the DLL that contains the EAP method implementation with the following console command.</span></span>

    <span data-ttu-id="7ac5b-109"> *&lt; Имя &gt;regsvr32.exeDLL*</span><span class="sxs-lookup"><span data-stu-id="7ac5b-109">**regsvr32.exe** *&lt;DLL name&gt;*</span></span>

    <span data-ttu-id="7ac5b-110">Чтобы удалить библиотеку DLL, используйте следующую команду консоли:</span><span class="sxs-lookup"><span data-stu-id="7ac5b-110">To uninstall the DLL, use the following console command:</span></span>

    <span data-ttu-id="7ac5b-111">**regsvr32.exe** **/u** *&lt; имя &gt; библиотеки*</span><span class="sxs-lookup"><span data-stu-id="7ac5b-111">**regsvr32.exe** **/u** *&lt;DLL name&gt;*</span></span>

-   <span data-ttu-id="7ac5b-112">Перезапустите службу EAPHost.</span><span class="sxs-lookup"><span data-stu-id="7ac5b-112">Restart the EAPHost service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ac5b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="7ac5b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ac5b-114">Использование EAPHost</span><span class="sxs-lookup"><span data-stu-id="7ac5b-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 