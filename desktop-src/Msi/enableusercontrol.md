---
description: Эту политику системы на компьютере можно использовать, чтобы указать, что установщик Windows передают все открытые свойства на серверную часть во время управляемой установки с повышенными привилегиями.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: енаблеусерконтрол
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155531"
---
# <a name="enableusercontrol"></a><span data-ttu-id="7dd02-103">енаблеусерконтрол</span><span class="sxs-lookup"><span data-stu-id="7dd02-103">EnableUserControl</span></span>

<span data-ttu-id="7dd02-104">В случае управляемой установки разработчику пакета может потребоваться ограничить количество общедоступных свойств, передаваемых на серверную часть, и изменить их может пользователь, не являющийся системным администратором.</span><span class="sxs-lookup"><span data-stu-id="7dd02-104">In the case of a managed installation, the package author may need to limit which public properties are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="7dd02-105">Некоторые ограничения обычно необходимы для обеспечения безопасной среды, когда установка требует, чтобы установщик использовал повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="7dd02-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span>

<span data-ttu-id="7dd02-106">Если для этой [системной политики](system-policy.md) на уровне компьютера задано значение "1", установщик может передавать все [открытые свойства](public-properties.md) на серверную часть во время управляемой установки с помощью повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="7dd02-106">If this per-machine [system policy](system-policy.md) is set to "1", then the installer can pass all [public properties](public-properties.md) to the server side during a managed installation using elevated privileges.</span></span> <span data-ttu-id="7dd02-107">Установка этой политики оказывает тот же результат, что и установка свойства **енаблеусерконтрол** .</span><span class="sxs-lookup"><span data-stu-id="7dd02-107">Setting this policy has the same effect as setting the **EnableUserControl** property.</span></span> <span data-ttu-id="7dd02-108">Задание этой политики позволяет передавать все открытые свойства в службу и быть изменяемыми неадминистративными пользователями.</span><span class="sxs-lookup"><span data-stu-id="7dd02-108">Setting this policy allows all public properties to be passed to the service and to be changeable by nonadministrative users.</span></span> <span data-ttu-id="7dd02-109">По умолчанию эта политика отключена. на стороне сервера передаются только ограниченные открытые свойства, которые могут быть изменены неадминистративным пользователем.</span><span class="sxs-lookup"><span data-stu-id="7dd02-109">By default, this policy is not enabled; only restricted public properties are passed to the server side and changeable by a nonadministrative user.</span></span> <span data-ttu-id="7dd02-110">Все остальные открытые свойства игнорируются.</span><span class="sxs-lookup"><span data-stu-id="7dd02-110">All other public properties are ignored.</span></span>

<span data-ttu-id="7dd02-111">Если операционной системой является Windows 2000, пользователь не является системным администратором, а приложение или продукт устанавливаются с повышенными правами, а пользователь, не являющийся системным администратором, может переопределять только утвержденный список ограниченных общих свойств.</span><span class="sxs-lookup"><span data-stu-id="7dd02-111">If the operating system is Windows 2000, the user is not a system administrator, and the application or product is being installed with elevated privileges, then a user that is not a system administrator can only override an approved list of restricted public properties.</span></span> <span data-ttu-id="7dd02-112">Дополнительные сведения см. в разделе [ограниченные открытые свойства](restricted-public-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7dd02-112">For more information see [Restricted Public Properties](restricted-public-properties.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="7dd02-113">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="7dd02-113">Registry Key</span></span>

<span data-ttu-id="7dd02-114">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="7dd02-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="7dd02-115">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7dd02-115">Data Type</span></span>

<span data-ttu-id="7dd02-116">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7dd02-116">**REG\_DWORD**</span></span>

 

 



