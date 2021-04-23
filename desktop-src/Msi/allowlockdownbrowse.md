---
description: Установка значения для этой системной политики для каждого компьютера в &\# 0034; 1&\# 0034; позволяет пользователям с правами администратора использовать диалоговое окно обзора для поиска источников управляемых приложений.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: алловлоккдовнбровсе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909116"
---
# <a name="allowlockdownbrowse"></a><span data-ttu-id="0f12e-103">алловлоккдовнбровсе</span><span class="sxs-lookup"><span data-stu-id="0f12e-103">AllowLockdownBrowse</span></span>

<span data-ttu-id="0f12e-104">Установка для этой [политики системы](system-policy.md) каждого компьютера значения "1" позволяет пользователям с правами администратора использовать [диалоговое окно обзора](browse-dialog.md) для поиска источников [*управляемых приложений*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0f12e-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" enables nonadministrative users to use a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md).</span></span> <span data-ttu-id="0f12e-105">Источники могут включать носители, такие как компакт-диски, URL-адреса и сетевые расположения.</span><span class="sxs-lookup"><span data-stu-id="0f12e-105">Sources may include media, such as CD-ROM, URLs, and network locations.</span></span> <span data-ttu-id="0f12e-106">Дополнительные сведения см. в разделе [устойчивость источника](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="0f12e-106">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="0f12e-107">По умолчанию установщик Windows в том, что пользователи, не являющиеся администраторами, не могут просматривать новые источники управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="0f12e-107">The default on Windows Installer is that nonadministrative users cannot browse for new sources of managed applications.</span></span> <span data-ttu-id="0f12e-108">Доступны только те источники, которые уже зарегистрированы в исходном списке продукта.</span><span class="sxs-lookup"><span data-stu-id="0f12e-108">The only sources available are those that are already registered in the source list of the product.</span></span> <span data-ttu-id="0f12e-109">Если эта политика задана, пользователь, не являющийся администратором, может просматривать новые источники назначенных или опубликованных приложений или приложений, устанавливаемых для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="0f12e-109">If this policy is set, a nonadministrative user may browse for new sources of assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="0f12e-110">Параметр Алловлоккдовнбровсе также позволяет пользователям, не обладающим правами администратора, запускать программы на правах LocalSystem во время установки с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="0f12e-110">Setting AllowLockdownBrowse also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="0f12e-111">Рекомендуется использовать значение по умолчанию, чтобы обеспечить безопасную среду.</span><span class="sxs-lookup"><span data-stu-id="0f12e-111">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="0f12e-112">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="0f12e-112">Registry Key</span></span>

<span data-ttu-id="0f12e-113">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="0f12e-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="0f12e-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0f12e-114">Data Type</span></span>

<span data-ttu-id="0f12e-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0f12e-115">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="0f12e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f12e-116">Remarks</span></span>

<span data-ttu-id="0f12e-117">Установка этой политики также позволяет пользователям, не обладающим правами администратора, запускать произвольные программы на правах LocalSystem, если у них есть пакет установщик Windows, который устанавливает или запускает эти программы.</span><span class="sxs-lookup"><span data-stu-id="0f12e-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

<span data-ttu-id="0f12e-118">[Дисаблебровсе](disablebrowse.md) переопределяет алловлоккдовнбровсе и предотвращает просмотр, даже если задано алловлоккдовнбровсе.</span><span class="sxs-lookup"><span data-stu-id="0f12e-118">[DisableBrowse](disablebrowse.md) overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

<span data-ttu-id="0f12e-119">Сведения о взаимодействии этой политики с источниками установки см. в разделе [Управление источниками установки](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="0f12e-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f12e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0f12e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f12e-121">Отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="0f12e-121">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="0f12e-122">алловлоккдовнмедиа</span><span class="sxs-lookup"><span data-stu-id="0f12e-122">AllowLockdownMedia</span></span>](allowlockdownmedia.md)
</dt> </dl>

 

 



