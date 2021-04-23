---
description: Начиная с Windows Server 2008 и Windows Vista, эта политика больше не действует.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: енаблеадминтсремоте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263607"
---
# <a name="enableadmintsremote"></a><span data-ttu-id="e77d5-103">енаблеадминтсремоте</span><span class="sxs-lookup"><span data-stu-id="e77d5-103">EnableAdminTSRemote</span></span>

<span data-ttu-id="e77d5-104">Начиная с Windows Server 2008 и Windows Vista, эта политика больше не действует.</span><span class="sxs-lookup"><span data-stu-id="e77d5-104">Beginning with Windows Server 2008 and Windows Vista, this policy no longer has any effect.</span></span> <span data-ttu-id="e77d5-105">Администратор может выполнить установку из сеанса консоли сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="e77d5-105">An administrator can perform an installation from the console session of a terminal server.</span></span> <span data-ttu-id="e77d5-106">Администратор также может выполнить установку из сеанса клиента сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="e77d5-106">An administrator can also perform an installation from a client session of the terminal server.</span></span>

<span data-ttu-id="e77d5-107">Дополнительные сведения см. в статье [службы терминалов](/windows/desktop/TermServ/terminal-services-portal) в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e77d5-107">For more information, see [Terminal Services](/windows/desktop/TermServ/terminal-services-portal) in the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="e77d5-108">\* \* Операционные системы, предшествующие Windows Server 2008 и Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="e77d5-108">\*\*Operating systems earlier than Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="e77d5-109">Настройка [политики системы](system-policy.md) для компьютера позволяет администраторам выполнять установку из сеанса клиента сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="e77d5-109">Setting this per-machine [system policy](system-policy.md) enables administrators to perform installations from a client session of the terminal server.</span></span> <span data-ttu-id="e77d5-110">Если эта политика не задана, администраторы могут выполнять установку только из сеанса консоли.</span><span class="sxs-lookup"><span data-stu-id="e77d5-110">If this policy is not set, administrators can only perform installations from the console session.</span></span> <span data-ttu-id="e77d5-111">Пользователи без прав администратора не могут выполнять установку из сеанса клиента.</span><span class="sxs-lookup"><span data-stu-id="e77d5-111">Nonadministrative users can never perform installations from a client session.</span></span> <span data-ttu-id="e77d5-112">Значение по умолчанию для этой политики позволяет только администраторам выполнять установку из сеанса консоли.</span><span class="sxs-lookup"><span data-stu-id="e77d5-112">The default value for this policy allows only administrators to perform installations from the console session.</span></span> <span data-ttu-id="e77d5-113">Администраторы всегда могут выполнять [административные установки](administrative-installation.md) из сеанса клиента сервера терминалов или сеанса консоли, независимо от того, задана ли эта политика.</span><span class="sxs-lookup"><span data-stu-id="e77d5-113">Administrators can always do [Administrative installations](administrative-installation.md) from a client session of the terminal server, or from the console session, regardless of whether this policy is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="e77d5-114">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="e77d5-114">Registry Key</span></span>

<span data-ttu-id="e77d5-115">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="e77d5-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="e77d5-116">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e77d5-116">Data Type</span></span>

<span data-ttu-id="e77d5-117">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e77d5-117">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="e77d5-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e77d5-118">Remarks</span></span>

<span data-ttu-id="e77d5-119">Дополнительные сведения см. также в статье [использование установщик Windows с сервером терминалов](using-windows-installer-with-a-terminal-server.md).</span><span class="sxs-lookup"><span data-stu-id="e77d5-119">For more information see also, [Using Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).</span></span>

 

 
