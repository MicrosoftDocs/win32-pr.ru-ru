---
description: Установка для политики Трансформссекуре значения 1 информирует установщик о том, что преобразования должны быть кэшированы локально на компьютере пользователя в том месте, где у пользователя нет доступа на запись.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Политика Трансформссекуре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896670"
---
# <a name="transformssecure-policy"></a><span data-ttu-id="26b8c-103">Политика Трансформссекуре</span><span class="sxs-lookup"><span data-stu-id="26b8c-103">TransformsSecure Policy</span></span>

<span data-ttu-id="26b8c-104">Установка для политики Трансформссекуре значения 1 информирует установщик о том, что преобразования должны быть кэшированы локально на компьютере пользователя в том месте, где у пользователя нет доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="26b8c-104">Setting the TransformsSecure policy to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="26b8c-105">Установка этой политики аналогична настройке [Свойства трансформссекуре](transformssecure.md) , за исключением того, что область отличается.</span><span class="sxs-lookup"><span data-stu-id="26b8c-105">Setting this policy is the same as setting the [TRANSFORMSSECURE property](transformssecure.md) except the scope is different.</span></span> <span data-ttu-id="26b8c-106">Настройка политики Трансформссекуре применяется ко всем пакетам, установленным на данном компьютере.</span><span class="sxs-lookup"><span data-stu-id="26b8c-106">Setting TransformsSecure policy applies to all packages installed to a given computer.</span></span> <span data-ttu-id="26b8c-107">Установка свойства ТРАНСФОРМССЕКУРЕ применяется к пакету независимо от компьютера.</span><span class="sxs-lookup"><span data-stu-id="26b8c-107">Setting the TRANSFORMSSECURE property applies to the package regardless of the computer.</span></span>

<span data-ttu-id="26b8c-108">Эта политика предназначена для обеспечения безопасного хранения преобразований с помощью командировок для пользователей Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="26b8c-108">The purpose of this policy is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="26b8c-109">Начиная с Windows Server 2003, значение этой политики по умолчанию равно 1.</span><span class="sxs-lookup"><span data-stu-id="26b8c-109">Beginning with Windows Server 2003, the default value of this policy is 1.</span></span>

<span data-ttu-id="26b8c-110">Если эта политика задана, [Установка обслуживания](maintenance-installation.md) может использовать только преобразование из защищенного кэша.</span><span class="sxs-lookup"><span data-stu-id="26b8c-110">When this policy is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the secured cache.</span></span> <span data-ttu-id="26b8c-111">Если установщик обнаружит, что преобразование отсутствует на локальном компьютере, установщик попытается восстановить преобразование.</span><span class="sxs-lookup"><span data-stu-id="26b8c-111">In the event that the installer finds that the transform is missing on the local computer, the installer attempts to restore the transform.</span></span> <span data-ttu-id="26b8c-112">Чтобы установщик мог восстановить преобразование, безопасное преобразование должно находиться в списке источников установочного пакета в полномочном источнике.</span><span class="sxs-lookup"><span data-stu-id="26b8c-112">In order for the installer to restore the transform, the secure transform must reside at an authorized source in the installation package's source list.</span></span> <span data-ttu-id="26b8c-113">Дополнительные сведения см. в разделе [устойчивость источника](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="26b8c-113">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="26b8c-114">Установка обслуживания завершается сбоем, если преобразование недоступно или не может быть загружено.</span><span class="sxs-lookup"><span data-stu-id="26b8c-114">The maintenance installation fails if the transform is unavailable or cannot be loaded.</span></span>

<span data-ttu-id="26b8c-115">В Windows Server 2003, если эта политика не задана, поведение по умолчанию заключается в хранении преобразований в безопасном месте.</span><span class="sxs-lookup"><span data-stu-id="26b8c-115">On Windows Server 2003, if this policy is not set, the default behavior is to store the transforms in a secure location.</span></span> <span data-ttu-id="26b8c-116">Если политика не задана, то по умолчанию для всех версий, предшествовавших Windows Server 2003, сохраняются преобразования в профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="26b8c-116">On all versions prior to Windows Server 2003, if the policy is not set, the default behavior is to store the transforms in the users profile.</span></span>

<span data-ttu-id="26b8c-117">Дополнительные сведения см. в разделе также [безопасные преобразования](secured-transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="26b8c-117">See also [Secured Transforms](secured-transforms.md) for more information.</span></span>

<span data-ttu-id="26b8c-118">Установщик Windows интерпретирует [политику трансформсатсаурце](transformsatsource-policy.md) как ту же, что и политика трансформссекуре.</span><span class="sxs-lookup"><span data-stu-id="26b8c-118">Windows Installer interprets the [TransformsAtSource policy](transformsatsource-policy.md) to be the same as the TransformsSecure policy.</span></span>

## <a name="registry-key"></a><span data-ttu-id="26b8c-119">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="26b8c-119">Registry Key</span></span>

<span data-ttu-id="26b8c-120">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="26b8c-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="26b8c-121">Тип данных</span><span class="sxs-lookup"><span data-stu-id="26b8c-121">Data Type</span></span>

<span data-ttu-id="26b8c-122">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="26b8c-122">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="26b8c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="26b8c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26b8c-124">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="26b8c-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



