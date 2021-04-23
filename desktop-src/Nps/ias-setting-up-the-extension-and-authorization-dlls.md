---
title: Настройка библиотек DLL расширения
description: При запуске NPS проверяет реестр на наличие списка DLL-библиотек сторонних производителей для вызова.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e8589f31144f12b120f9a77f281dd57a9f30ce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070323"
---
# <a name="setting-up-the-extension-dlls"></a><span data-ttu-id="1ad52-103">Настройка библиотек DLL расширения</span><span class="sxs-lookup"><span data-stu-id="1ad52-103">Setting Up the Extension DLLs</span></span>

> [!Note]  
> <span data-ttu-id="1ad52-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1ad52-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="1ad52-105">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="1ad52-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="1ad52-106">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="1ad52-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="1ad52-107">При запуске NPS проверяет реестр на наличие списка DLL-библиотек сторонних производителей для вызова.</span><span class="sxs-lookup"><span data-stu-id="1ad52-107">At startup, NPS checks the registry for a list of third-party DLLs to call.</span></span>

<span data-ttu-id="1ad52-108">Чтобы настроить библиотеку DLL проверки подлинности или авторизации на сервере NPS, перечислите пути к библиотекам DLL в разделе значения ниже следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="1ad52-108">To set up an Authentication or Authorization DLL on an NPS server, list the paths to the DLLs in values below the following registry key:</span></span>

<span data-ttu-id="1ad52-109">**\\Параметры ауссрв системы HKLM System \\ CurrentControlSet \\ Services \\ \\\\**</span><span class="sxs-lookup"><span data-stu-id="1ad52-109">**HKLM\\System\\CurrentControlSet\\Services\\AuthSrv\\Parameters\\**</span></span>

<span data-ttu-id="1ad52-110">Если ключи **ауссрв** и **Parameters** не существуют, создайте их.</span><span class="sxs-lookup"><span data-stu-id="1ad52-110">If the **AuthSrv** and **Parameters** keys do not exist, create them.</span></span>

<span data-ttu-id="1ad52-111">Ниже приведено значение, в котором перечислены библиотеки DLL расширения проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1ad52-111">The value in which to list the Authentication Extension DLLs is:</span></span>

<span data-ttu-id="1ad52-112">**екстенсиондллс**</span><span class="sxs-lookup"><span data-stu-id="1ad52-112">**ExtensionDLLs**</span></span>

<span data-ttu-id="1ad52-113">Для перечисления библиотек DLL расширения авторизации используется следующее значение:</span><span class="sxs-lookup"><span data-stu-id="1ad52-113">The value in which to list the Authorization Extension DLLs is:</span></span>

<span data-ttu-id="1ad52-114">**аусоризатиондллс**</span><span class="sxs-lookup"><span data-stu-id="1ad52-114">**AuthorizationDLLs**</span></span>

<span data-ttu-id="1ad52-115">Значения **екстенсиондллс** и **аусоризатиондллс** должны иметь тип **reg \_ Multi \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="1ad52-115">Both the **ExtensionDLLs** and **AuthorizationDLLs** values must be of type **REG\_MULTI\_SZ**.</span></span> <span data-ttu-id="1ad52-116">Этот тип позволяет перечислить несколько библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="1ad52-116">This type allows you to list multiple DLLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ad52-117">См. также</span><span class="sxs-lookup"><span data-stu-id="1ad52-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad52-118">Вызов библиотек DLL расширения</span><span class="sxs-lookup"><span data-stu-id="1ad52-118">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[<span data-ttu-id="1ad52-119">Атрибуты идентификации пользователя</span><span class="sxs-lookup"><span data-stu-id="1ad52-119">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 