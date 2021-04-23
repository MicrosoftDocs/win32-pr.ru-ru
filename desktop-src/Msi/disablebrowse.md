---
description: Установка для этой политики системы каждого компьютера значения &\# 0034; 1&\# 0034; запрещает пользователям, не использующим права администратора, использовать диалоговое окно обзора для поиска источников управляемых приложений, хранящихся на носителе, например компакт-диске.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: дисаблебровсе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650484"
---
# <a name="disablebrowse"></a><span data-ttu-id="72e05-103">дисаблебровсе</span><span class="sxs-lookup"><span data-stu-id="72e05-103">DisableBrowse</span></span>

<span data-ttu-id="72e05-104">Если задать для этой [политики системы](system-policy.md) на уровне компьютера значение "1", пользователи с правами администратора не смогут использовать [диалоговое окно обзора](browse-dialog.md) для поиска источников [*управляемых приложений*](m-gly.md) , хранящихся на носителе, например компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="72e05-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" prevents nonadministrative users from using a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md) stored on media, such as CD-ROM.</span></span> <span data-ttu-id="72e05-105">Поле со списком "использовать функцию из:" для прямого ввода заблокировано и "Browse..." кнопка отключена.</span><span class="sxs-lookup"><span data-stu-id="72e05-105">The "Use feature from:" combo box for direct input is locked and the "Browse..." button is disabled.</span></span> <span data-ttu-id="72e05-106">Дополнительные сведения о просмотре исходного кода см. в разделе [устойчивость источника](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="72e05-106">For more details on source browsing, see [source resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="72e05-107">Дисаблебровсе переопределяет Алловлоккдовнбровсе и предотвращает просмотр, даже если задано Алловлоккдовнбровсе.</span><span class="sxs-lookup"><span data-stu-id="72e05-107">DisableBrowse overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="72e05-108">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="72e05-108">Registry Key</span></span>

<span data-ttu-id="72e05-109">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="72e05-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="72e05-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="72e05-110">Data Type</span></span>

<span data-ttu-id="72e05-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="72e05-111">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="72e05-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72e05-112">Remarks</span></span>

<span data-ttu-id="72e05-113">В некоторых случаях с набором Дисаблебровсе пользователь, не являющийся администратором, может по-прежнему иметь возможность устанавливать управляемые приложения из источников на правильно помеченном носителе.</span><span class="sxs-lookup"><span data-stu-id="72e05-113">In some cases with DisableBrowse set, a nonadministrative user may still be capable of installing managed applications from sources on correctly labeled media.</span></span> <span data-ttu-id="72e05-114">Установка политики Дисаблебровсе отключает возможность просмотра только источников.</span><span class="sxs-lookup"><span data-stu-id="72e05-114">Setting the DisableBrowse policy only disables the capability to browse to sources.</span></span> <span data-ttu-id="72e05-115">Его можно использовать, чтобы запретить пользователю, не имеющему прав администратора, переход к новому источнику во время установки, переустановки или восстановления по запросу.</span><span class="sxs-lookup"><span data-stu-id="72e05-115">It can be used to prevent a nonadministrative user from browsing to a new source during an install-on-demand installation, reinstallation, or repair.</span></span> <span data-ttu-id="72e05-116">Если задано значение [алловлоккдовнмедиа](allowlockdownmedia.md) , неадминистративный пользователь по-прежнему может установить управляемое приложение с правильно помеченным носителем.</span><span class="sxs-lookup"><span data-stu-id="72e05-116">If [AllowLockdownMedia](allowlockdownmedia.md) is set, the nonadministrative user could still install a managed application from correctly labeled media.</span></span>

<span data-ttu-id="72e05-117">Дисаблебровсе запрещает пользователю, не обладающему правами администратора, переходить к новому расположению носителя или к другому исходному расположению.</span><span class="sxs-lookup"><span data-stu-id="72e05-117">DisableBrowse prevents the nonadministrative user from browsing to a new media location or any other source location.</span></span> <span data-ttu-id="72e05-118">Дополнительные сведения о защите источников мультимедиа управляемых приложений см. в статье [устойчивость источника](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="72e05-118">For details of how to secure media sources of managed applications see [Source Resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="72e05-119">Сведения о взаимодействии этой политики с источниками установки см. в разделе [Управление источниками установки](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="72e05-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

 

 



