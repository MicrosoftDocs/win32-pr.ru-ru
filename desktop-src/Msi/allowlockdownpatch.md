---
description: Если эта политика системы для компьютера не задана, только администраторы могут обновить существующие продукты, которые были установлены с помощью повышенных привилегий.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: алловлоккдовнпатч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998300"
---
# <a name="allowlockdownpatch"></a><span data-ttu-id="0f1b3-103">алловлоккдовнпатч</span><span class="sxs-lookup"><span data-stu-id="0f1b3-103">AllowLockdownPatch</span></span>

<span data-ttu-id="0f1b3-104">Если эта [Политика системы](system-policy.md) для компьютера не задана, только администраторы могут обновить существующие продукты, которые были установлены с помощью повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="0f1b3-104">If this per-machine [system policy](system-policy.md) is not set, only administrators can patch existing products that were installed using elevated privileges.</span></span> <span data-ttu-id="0f1b3-105">Если для Алловлоккдовнпатч задано значение "1", пользователи, не являющиеся администраторами, могут в некоторых случаях применять исправления к продуктам при выполнении установки с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="0f1b3-105">If AllowLockdownPatch is set to "1", nonadministrative users can, in some cases, apply patches to products while running an installation using elevated privileges.</span></span> <span data-ttu-id="0f1b3-106">Установив политику, можно установить [незначительные обновления](minor-upgrades.md) при выполнении установки с повышенными привилегиями, но обновление не сможет установить [основные обновления](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="0f1b3-106">With the policy set, the patch can install [minor upgrades](minor-upgrades.md) while running an installation using elevated privileges, the patch cannot install [major upgrades](major-upgrades.md).</span></span> <span data-ttu-id="0f1b3-107">Установка этой политики также позволяет пользователям, не обладающим правами администратора, запускать программы на правах LocalSystem во время установки с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="0f1b3-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="0f1b3-108">Рекомендуется использовать значение по умолчанию, чтобы обеспечить безопасную среду.</span><span class="sxs-lookup"><span data-stu-id="0f1b3-108">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="0f1b3-109">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="0f1b3-109">Registry Key</span></span>

<span data-ttu-id="0f1b3-110">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="0f1b3-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="0f1b3-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0f1b3-111">Data Type</span></span>

<span data-ttu-id="0f1b3-112">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0f1b3-112">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="0f1b3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f1b3-113">Remarks</span></span>

<span data-ttu-id="0f1b3-114">Любой пользователь может применить исправление при неповышенной установке.</span><span class="sxs-lookup"><span data-stu-id="0f1b3-114">Any user can apply a patch during a nonelevated installation.</span></span> <span data-ttu-id="0f1b3-115">Установка для этой [системной политики](system-policy.md) для каждого компьютера значения "1" дает пользователям без прав администратора дополнительную гибкость в применении исправлений к любому продукту во время установки с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="0f1b3-115">Setting this per-machine [system policy](system-policy.md) to "1" gives nonadministrative users the additional flexibility of applying patches to any product during an elevated installation.</span></span> <span data-ttu-id="0f1b3-116">Если эта политика не задана, пользователи без прав администратора не смогут применить исправление к назначенным или опубликованным приложениям.</span><span class="sxs-lookup"><span data-stu-id="0f1b3-116">If this policy is not set, nonadministrative users cannot apply a patch to assigned or published applications.</span></span>

<span data-ttu-id="0f1b3-117">Установка этой политики также позволяет пользователям, не обладающим правами администратора, запускать произвольные программы на правах LocalSystem, если у них есть пакет исправлений установщик Windows, который устанавливает или запускает эти программы.</span><span class="sxs-lookup"><span data-stu-id="0f1b3-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer patch package that installs or launches those programs.</span></span>

 

 



