---
description: Установка для этой системной политики на уровне компьютера значения &\# 0034; 1&\# 0034; позволяет пользователям, не обладающей правами администратора, устанавливать управляемые приложения из источников, хранящихся на носителе, например на компакт-диске.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: алловлоккдовнмедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914223"
---
# <a name="allowlockdownmedia"></a><span data-ttu-id="c752a-103">алловлоккдовнмедиа</span><span class="sxs-lookup"><span data-stu-id="c752a-103">AllowLockdownMedia</span></span>

<span data-ttu-id="c752a-104">Если задать для этой [политики системы](system-policy.md) каждого компьютера значение "1", пользователи, не являющиеся администраторами, смогут устанавливать [*управляемые приложения*](m-gly.md) из источников, хранящихся на НОСИТЕЛЕ, например на компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="c752a-104">Setting the value of this per-machine [system policy](system-policy.md) to "1", enables nonadministrative users to install [*managed applications*](m-gly.md) from sources stored on media, such as a CD-ROM.</span></span> <span data-ttu-id="c752a-105">См. раздел [устойчивость источника](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="c752a-105">See [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="c752a-106">Например, если эта политика задана, пользователь, не являющийся администратором, может использовать источник мультимедиа для установки назначенных или опубликованных приложений или приложений, устанавливаемых для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="c752a-106">For example, if this policy is set, a nonadministrative user may use a media source to install assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="c752a-107">Установка этой политики также позволяет пользователям, не обладающим правами администратора, запускать программы на правах LocalSystem во время установки с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="c752a-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="c752a-108">Значение этой политики по умолчанию равно 1 только на компьютерах, работающих под управлением Windows Vista и не присоединенных к домену.</span><span class="sxs-lookup"><span data-stu-id="c752a-108">The default value of this policy is 1 only on computers running Windows Vista and that are not joined to a domain.</span></span> <span data-ttu-id="c752a-109">По умолчанию на других компьютерах пользователи, не являющиеся администраторами, не могут устанавливать управляемые приложения из источника, расположенного на носителе.</span><span class="sxs-lookup"><span data-stu-id="c752a-109">The default on other computers is that nonadministrative users cannot install managed applications from a source located on media.</span></span>

<span data-ttu-id="c752a-110">Поскольку эта политика позволяет пользователям, которые не являются администраторами, устанавливать с привилегиями, которые они не имеют, по умолчанию, перед установкой этой политики следует определить, обеспечивает ли он соответствующий уровень безопасности для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c752a-110">Because this policy enables users that are not an administrator to install with privileges they do not have by default, before setting this policy you should consider whether it provides an appropriate level of security for your user.</span></span> <span data-ttu-id="c752a-111">Рекомендуется использовать значение по умолчанию, чтобы обеспечить безопасную среду.</span><span class="sxs-lookup"><span data-stu-id="c752a-111">The default setting is recommended to ensure a secure environment.</span></span>

<span data-ttu-id="c752a-112">Дополнительные сведения о защите установки и использовании цифровых сертификатов см. в разделе [рекомендации по созданию безопасных установок](guidelines-for-authoring-secure-installations.md) и [цифровых подписей, а также установщик Windows](digital-signatures-and-windows-installer.md) и [скачивании установки из Интернета](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="c752a-112">For more information about securing installations and using digital certificates see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="c752a-113">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="c752a-113">Registry Key</span></span>

<span data-ttu-id="c752a-114">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="c752a-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="c752a-115">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c752a-115">Data Type</span></span>

<span data-ttu-id="c752a-116">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c752a-116">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="c752a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c752a-117">Remarks</span></span>

<span data-ttu-id="c752a-118">Установка этой политики также позволяет пользователям, не обладающим правами администратора, запускать произвольные программы на правах LocalSystem, если у них есть пакет установщик Windows, который устанавливает или запускает эти программы.</span><span class="sxs-lookup"><span data-stu-id="c752a-118">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c752a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c752a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c752a-120">Отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="c752a-120">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="c752a-121">алловлоккдовнбровсе</span><span class="sxs-lookup"><span data-stu-id="c752a-121">AllowLockdownBrowse</span></span>](allowlockdownbrowse.md)
</dt> </dl>

 

 



